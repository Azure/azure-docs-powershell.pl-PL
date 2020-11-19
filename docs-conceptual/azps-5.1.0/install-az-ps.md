---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: f7a1658cdcafd1e8d6cba51ead26f9ddaa8c4c56
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715765"
---
# <a name="install-azure-powershell"></a>Instalowanie programu Azure PowerShell

W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu [PowerShellGet](/powershell/scripting/gallery/installing-psget). Te instrukcje działają na platformach Windows, macOS i Linux.

Program Azure PowerShell jest również dostępny w usłudze Azure [Cloud Shell](/azure/cloud-shell/overview) i jest teraz wstępnie instalowany w [obrazach platformy Docker](azureps-in-docker.md).

## <a name="requirements"></a>Wymagania

> [!NOTE]
> Program PowerShell w wersji 7.x lub nowszej jest zalecaną wersją programu PowerShell do używania z programem Azure PowerShell na wszystkich platformach.

Program Azure PowerShell współpracuje z programem PowerShell 6.2.4 lub nowszym na wszystkich platformach. Jest on również obsługiwany z programem PowerShell 5.1 w systemie Windows. Zainstaluj [najnowszą wersję programu PowerShell](/powershell/scripting/install/installing-powershell) dostępną dla danego systemu operacyjnego. Program Azure PowerShell nie ma dodatkowych wymagań w przypadku uruchamiania w programie PowerShell 6.2.4 lub nowszym.

Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

Aby użyć programu Azure PowerShell w programie PowerShell 5.1 w systemie Windows:

1. Przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).
   Jeśli używasz systemu Windows 10 w wersji 1607 lub nowszej, masz już zainstalowany program PowerShell 5.1.
2. Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).
3. Upewnij się, że masz najnowszą wersję modułu PowerShellGet. Uruchom polecenie `Install-Module -Name PowerShellGet -Force`.

## <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

> [!WARNING]
> Nie obsługujemy równocześnie zainstalowanych modułów AzureRM i Az w programie PowerShell 5.1 w systemie Windows. Jeśli chcesz zachować moduł AzureRM dostępny w systemie, zainstaluj moduł Az dla programu PowerShell 6.2.4 lub nowszego.

Użycie poleceń cmdlet PowerShellGet jest preferowaną metodą instalacji. Moduł Az zainstaluj tylko dla bieżącego użytkownika. Jest to zalecany zakres instalacji. Ta metoda działa tak samo na platformach Windows, macOS i Linux. Uruchom następujące polecenie z sesji programu PowerShell:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.

Zainstalowanie modułu dla wszystkich użytkowników w systemie wymaga podniesionych uprawnień. Uruchom sesję programu PowerShell przy użyciu pozycji **Uruchom jako administrator** w systemie Windows albo polecenia `sudo` w systemie macOS lub Linux:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Moduł Az to zbiorczy moduł poleceń cmdlet programu Azure PowerShell. Po jego zainstalowaniu są pobierane wszystkie ogólnie dostępne moduły Az programu PowerShell i są udostępniane do użycia ich polecenia cmdlet.

## <a name="install-offline"></a>Instalowanie w trybie offline

W niektórych środowiskach nie jest możliwe nawiązanie połączenia z galerią programu PowerShell. W takich sytuacjach nadal możesz przeprowadzić instalację w trybie offline przy użyciu jednej z następujących metod:

* Pobierz moduły do innej lokalizacji w sieci, a następnie użyj jej jako źródłowej lokalizacji instalacji.
  Ta metoda umożliwi buforowanie modułów programu PowerShell na jednym serwerze lub w jednym udziale plików, a następnie wdrażanie ich za pomocą modułu PowerShellGet w dowolnym odłączonym systemie. Aby dowiedzieć się, jak skonfigurować lokalne repozytorium i przeprowadzić instalację w systemach rozłączonych, zobacz [Working with local PowerShellGet repositories (Praca z lokalnymi repozytoriami modułu PowerShellGet)](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Pobierz pakiet MSI programu Azure PowerShell](install-az-ps-msi.md) na maszynę połączoną z siecią, a następnie skopiuj instalator do systemów bez dostępu do galerii programu PowerShell. Pamiętaj, że instalator MSI działa tylko na potrzeby programu PowerShell 5.1 w systemie Windows.
* Zapisz moduł za pomocą polecenia [Save-Module](/powershell/module/PowershellGet/Save-Module) w udziale plików lub zapisz go w innej lokalizacji źródłowej, a następnie ręcznie skopiuj na inne maszyny:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Rozwiązywanie problemów

Poniżej przedstawiono niektóre typowe problemy występujące podczas instalowania modułu Azure PowerShell. Jeśli masz problem, który nie został opisany w tym miejscu, [zgłoś go w usłudze GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Serwer proxy blokuje połączenie

Jeśli widzisz błędy z polecenia `Install-Module`, które wskazują, że galeria programu PowerShell jest nieosiągalna, możesz znajdować się za serwerem proxy. Różne systemy operacyjne i środowiska sieciowe mają różne wymagania dotyczące konfigurowania serwera proxy dla całego systemu. Skontaktuj się z administratorem systemu w celu uzyskania informacji o ustawieniach serwera proxy oraz sposobie konfigurowania ich dla Twojego środowiska.

Sam program PowerShell może nie być skonfigurowany do automatycznego korzystania z tego serwera proxy. Za pomocą programu PowerShell 5.1 lub nowszego skonfiguruj sesję programu PowerShell do użycia serwera proxy, wydając następujące polecenia:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Jeśli poświadczenia w Twoim systemie operacyjnym są skonfigurowane poprawnie, ta konfiguracja spowoduje kierowanie żądań programu PowerShell przez serwer proxy. Aby to ustawienie utrzymywało się między sesjami, dodaj te polecenia do [profilu programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Aby zainstalować pakiet, Twój serwer proxy musi zezwalać na połączenia HTTPS z następującym adresem:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Jeśli wyłączono automatyczne ładowanie modułów, ręcznie zaimportuj moduł za pomocą polecenia `Import-Module -Name Az`.
> Ze względu na strukturę modułu może to potrwać kilka sekund.

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualizowanie modułu programu Azure PowerShell

Aby zaktualizować dowolny moduł programu PowerShell, należy użyć tej samej metody, która została użyta do zainstalowania modułu. Jeśli na przykład pierwotnie skorzystano z polecenia `Install-Module`, należy użyć polecenia [Update-Module](/powershell/module/powershellget/update-module), aby uzyskać najnowszą wersję. Jeśli pierwotnie skorzystano z pakietu MSI, należy pobrać i zainstalować nowy pakiet MSI.

Polecenia cmdlet PowerShellGet nie mogą zaktualizować modułów, które zostały zainstalowane za pomocą pakietu MSI. Pakiety MSI nie aktualizują modułów, które zostały zainstalowane przy użyciu modułu PowerShellGet. Jeśli masz problemy z aktualizacją za pomocą modułu PowerShellGet, **zainstaluj ponownie** zamiast **aktualizować**. Ponowna instalacja jest przeprowadzana w taki sam sposób jak instalacja, ale należy dodać parametr `-Force`:

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

W przeciwieństwie do instalacji opartych na pakiecie MSI instalowanie lub aktualizowanie przy użyciu modułu PowerShellGet nie powoduje usunięcia starszych wersji, które mogą istnieć w systemie. Aby usunąć stare wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md). Aby uzyskać więcej informacji na temat instalacji opartych na pakiecie MSI, zobacz [Instalowanie programu Azure PowerShell za pomocą pakietu MSI](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Korzystanie z wielu wersji programu Azure PowerShell

Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell. Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).

Jeśli masz zainstalowaną więcej niż jedną wersję modułu, funkcja automatycznego ładowania modułów i polecenie `Import-Module` domyślnie ładują najnowszą wersję.

Określoną wersję modułu `Az` możesz zainstalować lub załadować, używając parametru `-RequiredVersion`:

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a>Używanie wielu repozytoriów z modułem PowerShellGet

Parametr **Repozytorium** jest wymagany, jeśli do modułu PowerShellGet w systemie dodano dodatkowe repozytoria, a moduł Az znajduje się w więcej niż jednym z nich.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a>Przekazywanie opinii

Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues). Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Next Steps

Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md). Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).
