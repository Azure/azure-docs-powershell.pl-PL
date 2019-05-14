---
title: Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: afa858975a38fe0e35c9e27667fbd1ac4c3300e9
ms.sourcegitcommit: b37b8bb6f8e39ecea5b50ceec48601eed313add7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/09/2019
ms.locfileid: "65511573"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w programie PowerShell 5.x w systemie Windows przy użyciu modułu PowerShellGet. Moduł PowerShellGet i funkcja zarządzania modułami to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).

Klasyczny model wdrażania platformy Azure nie jest obsługiwany przez tę wersję programu Azure PowerShell. Aby uzyskać pomoc techniczną w przypadku wdrożeń klasycznych, postępuj zgodnie z instrukcjami na stronie [Instalowanie modułu zarządzania usługami programu Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

> [!IMPORTANT]
> Moduł AzureRM nie jest obsługiwany w systemach macOS i Linux. Aby używać poleceń cmdlet programu Azure PowerShell na tych platformach, należy [zainstalować moduł Az](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Wymagania

Do zainstalowania programu Azure PowerShell jest wymagany moduł PowerShellGet w wersji 1.1.2.0 lub nowszej. Aby sprawdzić, czy jest on dostępny w systemie, uruchom następujące polecenie:

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Aby zaktualizować instalację modułu PowerShellGet, uruchom następujące polecenie:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Jeśli nie masz zainstalowanego modułu PowerShellGet, postępuj zgodnie z instrukcjami w poniższej tabeli dotyczącymi Twojego systemu.

|Scenariusz|Instrukcje dotyczące instalacji|
|---|---|
|Windows 10<br/>Windows Server 2016|Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym|
|Uaktualnienie do programu PowerShell 5| <ol><li>[Zainstaluj najnowszą wersję platformy WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Uruchom następujące polecenie:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|System Windows z programem PowerShell 3 lub PowerShell 4|<ol><il>[Pobierz moduły PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Uruchom następujące polecenie:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> Korzystanie z modułu PowerShellGet wymaga zasad wykonania pozwalających uruchamiać skrypty. Aby uzyskać więcej informacji na temat zasad wykonania programu PowerShell, zobacz [Informacje o zasadach wykonania](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Moduł opisany w tym dokumencie (AzureRM) korzysta z programu .NET Framework. Dlatego jest on niezgodny z programem PowerShell 6.0, który korzysta z platformy .NET Core. Jeśli korzystasz z programu PowerShell 6.0, postępuj zgodnie z [instrukcjami dotyczącymi instalacji dla systemów macOS i Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

Do zainstalowania modułów z galerii programu PowerShell jest wymagany podwyższony poziom uprawnień. Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień:

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.

Moduł `AzureRM` to zbiorczy moduł poleceń cmdlet programu Azure PowerShell. Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM` w bieżącej sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).
Aby dowiedzieć się, jak można utrwalić swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualizowanie modułu programu Azure PowerShell

Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module). To polecenie __nie__ powoduje odinstalowania wcześniejszych wersji.

```powershell-interactive
Update-Module -Name AzureRM
```

Jeśli chcesz usunąć starsze wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Korzystanie z wielu wersji programu Azure PowerShell

Jest możliwe zainstalowanie wielu wersji programu Azure PowerShell. Obecność więcej niż jednej wersji może być potrzebna w przypadku pracy z lokalnymi zasobami usługi Azure Stack, korzystania ze starszej wersji systemu Windows, której nie można zaktualizować do programu PowerShell 5.0, lub używania klasycznego modelu wdrażania platformy Azure. Aby zainstalować starszą wersję, podaj argument `-RequiredVersion` podczas instalacji.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Podczas ładowania modułu Azure PowerShell jest domyślnie ładowana najnowsza wersja. Aby załadować inną wersję, podaj argument `-RequiredVersion`.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Przekazywanie opinii

Jeśli znajdziesz błąd podczas korzystania z programu Azure Powershell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).
Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Następne kroki

Aby zacząć korzystać z programu Azure PowerShell i dowiedzieć się więcej o module i jego funkcjach, zobacz [Rozpoczęcie korzystania z programu Azure PowerShell](get-started-azureps.md).
