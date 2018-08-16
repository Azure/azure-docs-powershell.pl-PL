---
title: Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell
description: Dowiedz się, jak używać ponownie poświadczeń platformy Azure i innych informacji w wielu sesjach programu PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 76e08c462bb34bd2b16a11f70f14c4584b72795a
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106769"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a>Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell

Program Azure PowerShell oferuje funkcję **automatycznego zapisywania kontekstu platformy Azure**, która udostępnia następujące funkcje:

- Przechowywanie informacji logowania do ponownego użycia w nowych sesjach programu PowerShell.
- Łatwiejsze korzystanie z zadań w tle w celu wykonywania długotrwałych poleceń cmdlet.
- Możliwość przełączania kont, subskrypcji i środowisk bez konieczności osobnego logowania się.
- Możliwość wykonywania zadań z użyciem różnych poświadczeń i subskrypcji jednocześnie w tej samej sesji programu PowerShell.

## <a name="azure-contexts-defined"></a>Zdefiniowane konteksty platformy Azure

*Kontekst platformy Azure* to zestaw informacji, który definiuje cel poleceń cmdlet programu Azure PowerShell. Kontekst składa się z pięciu części:

- *Konto* — nazwa użytkownika lub jednostka usługi używana do uwierzytelniania komunikacji z platformą Azure
- *Subskrypcja* — subskrypcja platformy Azure zawierająca zasoby, których dotyczą wykonywane operacje.
- *Dzierżawa* — dzierżawa usługi Azure Active Directory, która zawiera Twoją subskrypcję. Dzierżawy są ważniejsze w przypadku uwierzytelniania za pomocą jednostki usługi.
- *Środowisko* — konkretna chmura platformy Azure będąca chmurą docelową. Zwykle jest to chmura globalna platformy Azure.
  Jednak ustawienia środowiska pozwalają również wybierać jako obiekty docelowe chmury krajowe, rządowe oraz lokalne (usługa Azure Stack).
- *Poświadczenia* — informacje używane przez platformę Azure do zweryfikowania Twojej tożsamości i sprawdzenia, czy masz autoryzację do uzyskania dostępu do zasobów na platformie Azure.

W poprzednich wersjach kontekst platformy Azure musiał być tworzony każdorazowo po otwarciu nowej sesji programu PowerShell. Począwszy od wersji 4.4.0 programu Azure PowerShell można włączyć automatyczne zapisywanie i ponowne użycie kontekstów platformy Azure przy każdym otwarciu nowej sesji programu PowerShell.

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a>Automatyczne zapisywanie kontekstu na potrzeby następnego logowania

Począwszy od wersji 6.3.0, program Azure PowerShell automatycznie zachowuje informacje o kontekście między sesjami. Aby skonfigurować w programie PowerShell zapominanie kontekstu i poświadczeń, użyj polecenia `Disable-AzureRmContextAutoSave`. W takim przypadku konieczne będzie logowanie się do platformy Azure każdorazowo po otwarciu nowej sesji programu PowerShell.

Aby umożliwić programowi Azure PowerShell zapamiętywanie kontekstu po zamknięciu sesji programu PowerShell, użyj polecenia `Enable-AzureRmContextAutosave`. Informacje o kontekście i poświadczenia będą automatycznie zapisywane w specjalnym ukrytym folderze w katalogu użytkownika (`%AppData%\Roaming\Windows Azure PowerShell`).
Następnie każda nowa sesja programu PowerShell wybiera kontekst użyty w ostatniej sesji jako docelowy.

Polecenia cmdlet, które umożliwiają zarządzanie kontekstami platformy Azure, umożliwiają także szczegółowe kontrolowanie. Dzięki nim można określić, czy zmiany mają obowiązywać tylko w bieżącej sesji programu PowerShell (zakres `Process`), czy każdej sesji programu PowerShell (zakres `CurrentUser`). Te opcje są szczegółowo omówione w temacie [Korzystanie z zakresów kontekstu](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Uruchamianie poleceń cmdlet programu PowerShell platformy Azure jako zadań w tle

Funkcja **automatycznego zapisywania kontekstu platformy Azure** umożliwia udostępnianie kontekstu użytkownika zadaniom programu PowerShell wykonywanym w tle. Program PowerShell umożliwia uruchamianie i monitorowanie długo wykonywanych zadań jako zadań w tle bez konieczności oczekiwania na zakończenie tych zadań. Użytkownik może udostępniać poświadczenia zadaniom w tle na dwa sposoby:

- Przekazując kontekst jako argument

  Większość poleceń cmdlet usługi AzureRM umożliwia przekazanie kontekstu w postaci parametru do polecenia cmdlet. Kontekst można przekazać do zadania w tle w sposób przedstawiony w poniższym przykładzie:

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- Używając domyślnego kontekstu z włączoną funkcją automatycznego zapisywania

  Jeśli włączono funkcję **automatycznego zapisywania kontekstu**, wówczas zadania w tle automatycznie używają domyślnego zapisanego kontekstu.

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

Jeśli chcesz poznać wynik zadania w tle, użyj polecenia `Get-Job`, aby sprawdzić stan zadania, oraz polecenia `Wait-Job`, aby poczekać na zakończenie zadania. Aby przechwycić lub wyświetlić wynik zadania w tle, użyj polecenia `Receive-Job`. Aby uzyskać więcej informacji, zobacz opis polecenia [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Tworzenie, wybieranie i usuwanie kontekstów oraz zmiana ich nazw

Aby utworzyć kontekst, musisz zalogować się do platformy Azure. Polecenie cmdlet `Connect-AzureRmAccount` (lub jego alias — `Login-AzureRmAccount`) ustawia domyślny kontekst używany przez następujące po nim polecenia cmdlet programu Azure PowerShell i pozwala użytkownikowi na dostęp do dowolnych dzierżaw lub subskrypcji, na które pozwalają poświadczenia.

Aby dodać nowy kontekst po zalogowaniu, użyj polecenia `Set-AzureRmContext` (lub jego aliasu — `Select-AzureRmSubscription`).

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

Poprzedni przykład dodaje nowy kontekst, którego obiektem docelowym jest „Contoso Subscription 1”, z użyciem bieżących poświadczeń użytkownika. Nowy kontekst ma nazwę „Contoso1”. Jeśli nie podasz nazwy dla tego kontekstu, będzie używana nazwa domyślna zawierająca identyfikator konta i identyfikator subskrypcji.

Aby zmienić nazwę istniejącego kontekstu, użyj polecenia cmdlet `Rename-AzureRmContext`. Na przykład:

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Ten przykład zmienia nazwę kontekstu o nazwie automatycznej `[user1@contoso.org; 123456-7890-1234-564321]` na prostą nazwę „Contoso2”. Polecenia cmdlet, które zarządzają kontekstami, używają również wypełniania po naciśnięciu klawisza TAB, dzięki czemu możliwe jest szybkie wybieranie kontekstu.

Aby na koniec usunąć kontekst, użyj polecenia cmdlet `Remove-AzureRmContext`.  Na przykład:

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

Powoduje zapomnienie kontekstu o nazwie „Contoso2”. Ten sam kontekst można odtworzyć za pomocą polecenia `Set-AzureRmContext`

## <a name="removing-credentials"></a>Usuwanie poświadczeń

Można usunąć wszystkie poświadczenia i skojarzone konteksty dla użytkownika lub jednostki usługi przy użyciu polecenia `Disconnect-AzureRmAccount` (znanego również jako `Logout-AzureRmAccount`). Polecenie cmdlet `Disconnect-AzureRmAccount` wykonywane bez parametrów usuwa wszystkie poświadczenia i konteksty skojarzone z użytkownikiem lub jednostką usługi w bieżącym kontekście. Możesz przekazać nazwę użytkownika, jednostkę usługi lub kontekst do konkretnego docelowego podmiotu zabezpieczeń.

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Korzystanie z zakresów kontekstu

W niektórych okolicznościach kontekst można wybrać, zmienić lub usunąć w sesji programu PowerShell bez wpływu na pozostałe sesje. Aby zmienić domyślne zachowanie poleceń cmdlet kontekstu, użyj parametru `Scope`. Zakres `Process` zastępuje domyślne działanie tego parametru, sprawiając, że dotyczy tylko bieżącej sesji. Z drugiej strony zakres `CurrentUser` zmienia kontekst we wszystkich sesjach, a nie tylko w bieżącej.

Aby na przykład zmienić kontekst domyślny w bieżącej sesji programu PowerShell bez wpływu na inne okna albo na kontekst używany przy następnym otwarciu sesji, użyj następujących poleceń:

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Jak zapamiętywane jest ustawienie automatycznego zapisywania kontekstu

Ustawienie automatycznego zapisywania kontekstu jest zapisywane q katalogu użytkownika programu Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`). Niektóre rodzaje kont komputerów mogą nie mieć dostępu do tego katalogu. W przypadku takich scenariuszy można użyć zmiennej środowiskowej

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Jeśli zostanie ustawiona na wartość „true”, kontekst będzie zapisywany automatycznie. Jeśli zostanie ustawiona na wartość „false”, kontekst nie będzie zapisywany.

## <a name="changes-to-the-azurermprofile-module"></a>Zmiany w module AzureRM.Profile

Nowe polecenia cmdlet do zarządzania kontekstem

- [Enable-AzureRmContextAutosave][enable] — umożliwia zapisywanie kontekstu między sesjami programu Powershell.
  Wszelkie zmiany powodują zmianę kontekstu globalnego.
- [Disable-AzureRmContextAutosave][disable] — wyłącza automatyczne zapisywanie kontekstu. W każdej nowej sesji programu PowerShell konieczne będzie ponowne logowanie się.
- [Select-AzureRmContext][select] — umożliwia wybór kontekstu domyślnego. Wszystkie kolejne polecenia cmdlet będą używać poświadczeń z tego kontekstu do uwierzytelniania.
- [Disconnect-AzureRmAccount][remove-cred] — usuwa wszystkie poświadczenia i konteksty skojarzone z danym kontem.
- [Remove-AzureRmContext][remove-context] — usuwa nazwany kontekst.
- [Rename-AzureRmContext][rename] — zmienia nazwę istniejącego kontekstu.

Zmiany istniejących poleceń cmdlet dotyczących profilu

- [Add-AzureRmAccount][login] — umożliwia określenie zakresu logowania do procesu lub bieżącego użytkownika.
  Pozwala na nazwanie domyślnego kontekstu po uwierzytelnieniu się.
- [Import-AzureRmContext][import] — umożliwia określenie zakresu logowania do procesu lub bieżącego użytkownika.
- [Set-AzureRmContext][set-context] — umożliwia wybór istniejących nazwanych kontekstów oraz określenie zakresu zmian kontekstu do procesu lub bieżącego użytkownika.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
