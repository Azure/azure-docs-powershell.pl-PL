---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 66d755384e532d434811f3e6122dcba97d5c48b5
ms.sourcegitcommit: 0654679cd4141add6d12c02fb8c689efcbad428d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/12/2020
ms.locfileid: "77154762"
---
# <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet. Te instrukcje działają na platformach Windows, macOS i Linux. W przypadku modułu Az nie są obecnie obsługiwane żadne inne metody instalacji.

## <a name="requirements"></a>Wymagania

Program Azure PowerShell działa z programem PowerShell 5.1 lub nowszym w systemie Windows albo z programem PowerShell Core 6.x lub nowszym na dowolnej platformie. Jeśli nie masz pewności, czy masz program PowerShell, albo korzystasz z systemu macOS lub Linux, [zainstaluj najnowszą wersję programu PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:

```powershell-interactive
$PSVersionTable.PSVersion
```

Aby uruchomić program Azure PowerShell w programie PowerShell 5.1 w systemie Windows:

1. Jeśli to konieczne, przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell). Jeśli używasz systemu Windows 10, masz już zainstalowany program PowerShell 5.1.
2. Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).

Nie istnieją żadne dodatkowe wymagania dotyczące programu Azure PowerShell, gdy korzysta się z programu PowerShell Core.

## <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

> [!WARNING]
> __Nie możesz__ mieć równocześnie zainstalowanych modułów AzureRM i Az dla programu PowerShell 5.1 dla systemu Windows. Jeśli potrzebujesz zachować moduł AzureRM dostępny w systemie, zainstaluj moduł Az dla programu PowerShell Core w wersji 6.x lub nowszej. Aby to zrobić, [zainstaluj program PowerShell Core w wersji 6.x lub nowszej](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows), a następnie wykonaj następujące instrukcje w terminalu programu PowerShell Core.

Zaleca się przeprowadzić instalację tylko dla aktywnego użytkownika:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Jeśli chcesz przeprowadzić instalację dla wszystkich użytkowników w systemie, wymagane są uprawnienia administratora. W sesji programu PowerShell z podwyższonym poziomem uprawnień uruchom jako administrator lub za pomocą polecenia `sudo` w systemie macOS lub Linux:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
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

## <a name="install-offline"></a>Instalowanie w trybie offline

W niektórych środowiskach nie jest możliwe nawiązanie połączenia z galerią programu PowerShell. W takich sytuacjach nadal możesz przeprowadzić instalację w trybie offline przy użyciu jednej z następujących metod:

* Pobierz moduły do innej lokalizacji, a następnie użyj jej jako źródłowej lokalizacji instalacji w sieci. Może to być skomplikowany proces, ale umożliwi buforowanie modułów programu PowerShell na pojedynczym serwerze lub wdrażanie udziału plików za pomocą modułu PowerShellGet w dowolnym rozłączonym systemie. Aby dowiedzieć się, jak skonfigurować lokalne repozytorium i przeprowadzić instalację w systemach rozłączonych, zobacz [Working with local PowerShellGet repositories (Praca z lokalnymi repozytoriami modułu PowerShellGet)](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Pobierz pakiet MSI programu Azure PowerShell](install-az-ps-msi.md) na maszynę połączoną z siecią, a następnie skopiuj instalator do systemów bez dostępu do galerii programu PowerShell. Pamiętaj, że instalator MSI działa tylko na potrzeby programu PowerShell 5.1 w systemie Windows.
* Zapisz moduł za pomocą polecenia [Save-Module](/powershell/module/PowershellGet/Save-Module) w udziale plików lub zapisz go w innej lokalizacji źródłowej, a następnie ręcznie skopiuj na inne maszyny:
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Rozwiązywanie problemów

Poniżej przedstawiono niektóre typowe problemy występujące podczas instalowania modułu Azure PowerShell. Jeśli masz problem, który nie został opisany w tym miejscu, [zgłoś go w usłudze GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Serwer proxy blokuje połączenie

Jeśli widzisz błędy z polecenia `Install-Module`, które wskazują, że galeria programu PowerShell jest nieosiągalna, możesz znajdować się za serwerem proxy. Różne systemy operacyjne mają różne wymagania dotyczące konfigurowania serwera proxy dla całego systemu, które nie zostały tu szczegółowo omówione. Skontaktuj się z administratorem systemu w celu uzyskania informacji o ustawieniach serwera proxy oraz sposobie konfigurowania ich dla Twojego systemu operacyjnego.

Sam program PowerShell może nie być skonfigurowany do automatycznego korzystania z tego serwera proxy. Za pomocą programu PowerShell 5.1 lub nowszego skonfiguruj serwer proxy do użytku dla sesji programu PowerShell, używając następującego polecenia:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Jeśli poświadczenia w Twoim systemie operacyjnym są skonfigurowane poprawnie, spowoduje to kierowanie żądań programu PowerShell przez serwer proxy.
Aby to ustawienie utrzymywało się między sesjami, dodaj to polecenie do [profilu programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Aby zainstalować pakiet, Twój serwer proxy musi zezwalać na połączenia HTTPS z następującym adresem:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Jeśli wyłączono automatyczne ładowanie modułów, ręcznie zaimportuj moduł za pomocą polecenia `Import-Module Az`. Ze względu na strukturę modułu może to potrwać kilka sekund.

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualizowanie modułu programu Azure PowerShell

Jeśli pierwotnie korzystano z polecenia Install-Module, należy użyć polecenia [Update-Module](/powershell/module/powershellget/update-module), aby uzyskać najnowszą wersję. Jeśli pierwotnie korzystano z pakietu MSI, należy pobrać i zainstalować nowy pakiet MSI w celu aktualizacji. Jeśli masz problemy z aktualizowaniem lub używaniem pakietu z modułu PowershellGet, należy wykonać __ponowną instalację__ a nie __aktualizację__. Jest ona realizowana w taki sam sposób jak instalacja, ale może być konieczne dodanie argumentu `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Mimo że może to spowodować zastąpienie zainstalowanych modułów, nadal można mieć starsze wersje pozostawione w systemie.
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
