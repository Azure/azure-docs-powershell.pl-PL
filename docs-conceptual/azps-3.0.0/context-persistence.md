---
title: Poświadczenia logowania i konteksty platformy Azure
description: Dowiedz się, jak używać ponownie poświadczeń platformy Azure i innych informacji w wielu sesjach programu PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 72d1b07bb2c66f80ea6f5d37ef7012d0d0a5bbbc
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062500"
---
# <a name="azure-powershell-context-objects"></a>Obiekty kontekstu środowiska Azure PowerShell

Środowisko Azure PowerShell używa _obiektów kontekstu środowiska Azure PowerShell_ (kontekstów platformy Azure) do przechowywania informacji o subskrypcji i uwierzytelnianiu. Jeśli masz więcej niż jedną subskrypcję, konteksty platformy Azure umożliwiają wybranie subskrypcji, na której mają być uruchamiane polecenia cmdlet środowiska Azure PowerShell. Konteksty platformy Azure są również używane do przechowywania informacji logowania w wielu sesjach programu PowerShell i uruchamiania zadań w tle.

W tym artykule opisano zarządzania kontekstami platformy Azure, a nie zarządzanie subskrypcjami ani kontami. Jeśli chcesz zarządzać użytkownikami, subskrypcjami, dzierżawami lub innymi informacjami o koncie, zapoznaj się z dokumentacją usługi [Azure Active Directory](/azure/active-directory). Aby dowiedzieć się więcej o używaniu kontekstów do uruchamiania zadań w tle lub równolegle, zobacz [Używanie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell](using-psjobs.md), gdy już zapoznasz się z kontekstami platformy Azure.

## <a name="overview-of-azure-context-objects"></a>Omówienie obiektów kontekstu platformy Azure

Konteksty platformy Azure to obiekty programu PowerShell odzwierciedlające aktywną subskrypcję, w której są uruchamiane polecenia, oraz informacje uwierzytelniania wymagane do nawiązywania połączenia z chmurą platformy Azure. Dzięki kontekstom platformy Azure środowisko Azure PowerShell nie musi ponownie uwierzytelniać Twojego konta za każdym razem, gdy przełączasz subskrypcje. Składniki kontekstu platformy Azure są następujące:

* _Konto_ użyte do zalogowania się do platformy Azure za pomocą polecenia [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Konteksty platformy Azure traktują użytkowników, identyfikatory aplikacji i jednostki usług tak samo z perspektywy konta.
* Aktywna _subskrypcja_, umowa serwisowa z firmą Microsoft na tworzenie i uruchamianie zasobów platformy Azure, które są skojarzone z _dzierżawą_. Dzierżawy są często określane jako _organizacje_ w dokumentacji lub podczas pracy z usługą Active Directory.
* Odwołanie do _pamięci podręcznej tokenu_, przechowywanego tokenu uwierzytelniania na potrzeby uzyskiwania dostępu do chmury platformy Azure. Miejsce, w którym ten token jest przechowywany, oraz czas jego trwania jest określany przez [ustawienia automatycznego zapisywania kontekstu](#save-azure-contexts-across-powershell-sessions).

Aby uzyskać więcej informacji o tych terminach, zobacz [Terminologia usługi Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Tokeny uwierzytelniania używane przez konteksty platformy Azure są takie same jak inne przechowywane tokeny będące składnikami sesji trwałej. 

Po zalogowaniu się przy użyciu polecenia `Connect-AzAccount` dla domyślnej subskrypcji zostanie utworzony co najmniej jeden kontekst platformy Azure. Obiekt zwrócony przez polecenie `Connect-AzAccount` jest domyślnym kontekstem platformy Azure używanym przez pozostałą część sesji programu PowerShell.

## <a name="get-azure-contexts"></a>Pobieranie kontekstów platformy Azure

Dostępne konteksty platformy Azure są pobierane za pomocą polecenia cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext). Wyświetl listę wszystkich dostępnych kontekstów, używając parametru `-ListAvailable`:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Lub pobierz kontekst według nazwy:

```azurepowershell-interactive
$context = Get-Context -Name "mycontext"
```

Nazwy kontekstów mogą być inne od nazwy skojarzonej subskrypcji.

> [!IMPORTANT]
> Dostępne konteksty platformy Azure to __nie zawsze są__ Twoje dostępne subskrypcje. Konteksty platformy Azure odzwierciedlają tylko lokalnie przechowywane informacje. Subskrypcje można pobrać przy użyciu polecenia cmdlet [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).

## <a name="create-a-new-azure-context-from-subscription-information"></a>Tworzenie nowego kontekstu platformy Azure na podstawie informacji o subskrypcji

Polecenie cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) służy zarówno do tworzenia nowych kontekstów platformy Azure, jak i ustawiania ich jako aktywnego kontekstu.
Najprostszy sposób na utworzenie nowego kontekstu platformy Azure to użycie informacji o istniejącej subskrypcji. Polecenie cmdlet ma za zadanie pobranie obiektu wyjściowego z polecenia `Get-AzSubscription` jako wartości w postaci potoku i skonfigurowanie nowego kontekstu platformy Azure:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Lub podania w razie potrzeby identyfikatora albo nazwy subskrypcji oraz identyfikatora dzierżawy:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Jeśli argument `-Name` zostanie pominięty, jako nazwa kontekstu będzie używany identyfikator i nazwa subskrypcji w formacie `Subscription Name (subscription-id)`.

## <a name="change-the-active-azure-context"></a>Zmienianie aktywnego kontekstu platformy Azure

Aby zmienić aktywny kontekst platformy Azure, można użyć zarówno polecenia `Set-AzContext`, jak i [Select-AzContext](/powershell/module/az.accounts/set-azcontext). Tak jak opisano w sekcji [Tworzenie nowego kontekstu platformy Azure](#create-a-new-azure-context-from-subscription-information), polecenie `Set-AzContext` tworzy nowy kontekst platformy Azure dla subskrypcji, jeśli taki nie istnieje, a następnie przełącza się na używanie tego kontekstu jako aktywnego.

Polecenie `Select-AzContext` powinno być używane tylko z istniejącymi kontekstami platformy Azure i działa podobnie do stosowania polecenia `Set-AzContext -Context`, ale jest przeznaczone do używania z potokowaniem:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Podobnie jak wiele innych poleceń zarządzania kontem i kontekstem w środowisku Azure PowerShell, polecenia `Set-AzContext` i `Select-AzContext` obsługują argument `-Scope`, co pozwala kontrolować czas aktywności kontekstu. Argument `-Scope` pozwala na zmianę aktywnego kontekstu pojedynczej sesji bez zmieniania domyślnego:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Aby uniknąć przełączania kontekstów dla całej sesji programu PowerShell, wszystkie polecenia środowiska Azure PowerShell można uruchamiać względem danego kontekstu z argumentem `-AzContext`:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

Innym głównym zastosowaniem kontekstów z poleceniami cmdlet środowiska Azure PowerShell jest uruchamianie poleceń w tle. Aby dowiedzieć się więcej o uruchamianiu zadań programu PowerShell przy użyciu środowiska Azure PowerShell, zobacz [Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Zapisywanie kontekstów platformy Azure w różnych sesjach programu PowerShell

Domyślnie konteksty platformy Azure są zapisywane w celu używania ich między sesjami programu PowerShell. To zachowanie można zmienić w następujący sposób:

* Zaloguj się przy użyciu polecenia `-Scope Process` z parametrem `Connect-AzAccount`.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Kontekst platformy Azure zwrócony jako część tego logowania jest prawidłowy _tylko_ dla bieżącej sesji i nie zostanie automatycznie zapisany, niezależnie od ustawienia automatycznego zapisywania kontekstu środowiska Azure PowerShell.
* Wyłącz automatyczne zapisywanie kontekstu środowiska Azure PowerShell przy użyciu polecenia cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).
  Wyłączenie automatycznego zapisywania kontekstu __nie__ powoduje wyczyszczenia żadnych przechowywanych tokenów. Aby dowiedzieć się, jak wyczyścić przechowywane informacje o kontekście platformy Azure, zobacz [Usuwanie poświadczeń i kontekstów platformy Azure](#remove-azure-contexts-and-stored-credentials).
* Jawnie włącz automatyczne zapisywanie kontekstu platformy Azure przy użyciu polecenia cmdlet [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave). Gdy automatyczne zapisywanie jest włączone, wszystkie konteksty użytkownika są przechowywane lokalnie na potrzeby przyszłych sesji programu PowerShell.
* Za pomocą polecenia [Save-AzContext](/powershell/module/az.accounts/save-azcontext) ręcznie zapisz konteksty do używania w przyszłych sesjach programu PowerShell, w których mogą być one ładowane za pomocą polecenia [Import-AzContext](/powershell/module/az.accounts/import-azcontext):

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> Wyłączenie automatycznego zapisywania kontekstu __nie__ powoduje wyczyszczenia żadnych zapisanych informacji o kontekście. Aby usunąć przechowywane informacje, użyj polecenia cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Aby uzyskać więcej informacji na temat usuwania zapisanych kontekstów, zobacz sekcję [Usuwanie kontekstów i poświadczeń](#remove-azure-contexts-and-stored-credentials).

Każde z tych poleceń obsługuje parametr `-Scope`, który może przyjmować wartość `Process` do stosowania tylko do obecnie uruchomionego procesu. Aby na przykład zapewnić, że nowo utworzone konteksty nie są zapisywane po zakończeniu sesji programu PowerShell:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Informacje o kontekście i tokeny są przechowywane w katalogu `$env:USERPROFILE\.Azure` w systemie Windows oraz w katalogu `$HOME/.Azure` na innych platformach. Informacje poufne, takie jak identyfikatory subskrypcji i identyfikatory dzierżawy, mogą być nadal ujawnione w przechowywanych informacjach za pośrednictwem dzienników lub zapisanych kontekstów. Aby dowiedzieć się, jak wyczyścić przechowywane informacje, zobacz sekcję [Usuwanie kontekstów i poświadczeń](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Usuwanie przechowywanych poświadczeń i kontekstów platformy Azure

Aby wyczyścić poświadczenia i konteksty platformy Azure:

* Wyloguj się z konta przy użyciu polecenia [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).
  Możesz wylogować się z dowolnego konta według konta lub kontekstu:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  Rozłączenie zawsze powoduje usunięcie przechowywanych tokenów uwierzytelniania i wyczyszczenie zapisanych kontekstów skojarzonych z odłączonym użytkownikiem lub kontekstem.
* Użyj polecenia [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). To polecenie cmdlet zawsze gwarantuje usunięcie przechowywanych kontekstów i tokenów uwierzytelniania, a także wyloguje Cię.
* Usuń kontekst za pomocą polecenia [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Jeśli usuniesz aktywny kontekst, nastąpi odłączenie od platformy Azure i będzie konieczne ponowne uwierzytelnienie przy użyciu polecenia `Connect-AzAccount`.

## <a name="see-also"></a>Zobacz też

* [Uruchamianie poleceń cmdlet środowiska Azure PowerShell w zadaniach programu PowerShell](using-psjobs.md)
* [Terminologia usługi Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Dokumentacja modułu Az.Accounts](/powershell/module/az.accounts)
