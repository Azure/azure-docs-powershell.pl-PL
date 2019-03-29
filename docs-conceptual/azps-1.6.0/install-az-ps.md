---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475533"
---
# <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet. Te instrukcje działają na platformach Windows, macOS i Linux. W przypadku modułu Az nie są obecnie obsługiwane żadne inne metody instalacji.

## <a name="requirements"></a>Wymagania

Program Azure PowerShell działa z programem PowerShell 5.1 lub nowszym w systemie Windows albo z programem PowerShell 6 na dowolnej platformie.
Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:

```powershell-interactive
$PSVersionTable.PSVersion
```

Jeśli masz nieaktualną wersją lub musisz zainstalować program PowerShell, zobacz [Instalowanie różnych wersji programu PowerShell](/powershell/scripting/setup/installing-powershell). Ta strona zawiera linki do informacji o instalacji dla określonych platform.

Jeśli używasz programu PowerShell 5 w systemie Windows, musisz mieć również zainstalowany program .NET Framework 4.7.2. Aby uzyskać instrukcje dotyczące aktualizacji lub instalowania nowej wersji programu .NET Framework, zobacz [Przewodnik instalacji programu .NET Framework](/dotnet/framework/install).

## <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

> [!IMPORTANT]
>
> Moduły AzureRM i Az mogą być zainstalowane jednocześnie. Jeśli oba są zainstalowane, __nie włączaj aliasów__.
> Włączenie aliasów spowoduje powstanie konfliktów między poleceniami cmdlet modułu AzureRM i aliasami poleceń modułu Az, co może doprowadzić do nieoczekiwanego zachowania.
> Zalecamy, aby przed zainstalowaniem modułu Az odinstalować moduł AzureRM. Odinstalować moduł AzureRM lub włączyć aliasy możesz w dowolnym momencie. Aby dowiedzieć się więcej o aliasach poleceń AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).
> Aby uzyskać instrukcje odinstalowywania, zobacz [Odinstalowywanie modułu AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module). 

Aby zainstalować moduły w zakresie globalnym, wymagany jest podwyższony poziom uprawnień w celu zainstalowania modułów z galerii programu PowerShell. Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień (opcja „Uruchom jako Administrator” w systemie Windows lub z uprawnieniami superużytkownika w systemie macOS lub Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Jeśli nie masz dostępu do uprawnień administratora, możesz przeprowadzić instalację dla bieżącego użytkownika, dodając argument `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.

Moduł Az to zbiorczy moduł poleceń cmdlet programu Azure PowerShell. Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module Az`. Ze względu na strukturę modułu może to potrwać kilka sekund.

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualizowanie modułu programu Azure PowerShell

Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module). To polecenie __nie__ powoduje odinstalowania starszych wersji.

```powershell-interactive
Update-Module -Name Az
```

Aby dowiedzieć się, jak usunąć stare wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Korzystanie z wielu wersji programu Azure PowerShell

Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell. Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).

Określoną wersję modułu `Az` możesz zainstalować lub załadować, używając argumentu `-RequiredVersion`:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Jeśli masz zainstalowaną więcej niż jedną wersję modułu, funkcja automatycznego ładowania modułów i polecenie `Import-Module` domyślnie ładują najnowszą wersję.

## <a name="provide-feedback"></a>Przekazywanie opinii

Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).
Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Następne kroki

Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).
Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).
