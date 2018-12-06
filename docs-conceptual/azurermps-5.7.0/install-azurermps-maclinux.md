---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828352"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Instalowanie programu Azure PowerShell w systemie macOS lub Linux

W przypadku platform innych niż Windows program Azure PowerShell można uruchomić w programie PowerShell Core w wersji 6. Ta wersja programu PowerShell jest przeznaczona do użycia na każdej platformie, która obsługuje platformę .NET Core. Do pracy z tymi platformami jest dostępna specjalna wersja programu Azure PowerShell obsługująca platformę .NET Core.

> [!NOTE]
> W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.
> Wsparcie dla tych produktów jest ograniczone. Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.
>
> * [Problemy z programem PowerShell Core w wersji 6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemy z programem Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Instalowanie programu PowerShell Core

Instrukcje dotyczące instalacji programu PowerShell Core różnią się w przypadku systemu macOS i większości dystrybucji systemu Linux.
Szczegółowe instrukcje można znaleźć w następujących artykułach:

* [Instalowanie programu PowerShell Core w systemie macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Instalowanie programu PowerShell Core w systemie Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Instalowanie programu Azure PowerShell dla platformy .NET Core

Program PowerShell Core jest dostarczany z już zainstalowanym modułem PowerShellGet. Instalacja modułów programu PowerShell wymaga podwyższonego poziomu uprawnień, więc musisz uruchomić sesję jako superużytkownik:

```bash
sudo pwsh
```

Aby zainstalować program Azure PowerShell, uruchom następujące polecenie:

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> Moduł `AzureRM`, szczegółowo opisany w innych artykułach, nie jest przeznaczony dla platformy .NET Core i nie będzie współdziałać z programem PowerShell Core. Moduły `AzureRM` i `AzureRM.NetCore` używają tych samych nazw poleceń cmdlet, więc jedyną różnicą jest nazwa modułu zbiorczego i wersja platformy .NET, z pomocą której je utworzono.

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.

## <a name="sign-in"></a>Logowanie

Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM.Netcore` w sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure. Zaimportowanie modułu __nie__ wymaga podwyższonego poziomu uprawnień.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).
W systemach macOS i Linux należy pracować z profilem, używając zmiennej środowiskowej `$Profile`. Aby dowiedzieć się, jak można utrwalić swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="available-cmdlets"></a>Dostępne polecenia cmdlet

Moduły programu Azure PowerShell dla platformy .NET Core są ciągle w fazie opracowywania. Nie oferują one pełnego zestawu poleceń cmdlet dostępnych w modułach w wersji dla systemu Windows. Następujące funkcje są implementowane w modułach AzureRM.Netcore:

* Zarządzanie kontami
  * Logowanie się przy użyciu konta Microsoft, konta organizacji lub jednostki usługi za pośrednictwem usługi Microsoft Azure Active Directory
  * Zapisywanie poświadczeń na dysku poleceniem Save-AzureRmContext i ładowanie zapisanych poświadczeń poleceniem Import-AzureRmContext
* Środowisko
  * Pobieranie różnych gotowych środowisk platformy Microsoft Azure
  * Dodawanie/ustawianie/usuwanie dostosowanych środowisk (takich jak środowiska Azure Stack lub Windows Azure Pack)
* Polecenia cmdlet płaszczyzny zarządzania dla usług platformy Azure korzystających z interfejsów menedżera zasobów i zarządzania usługami.
  * Maszyna wirtualna
  * App Service (Websites)
  * SQL Database
  * Magazyn
  * Sieć

## <a name="next-steps"></a>Następne kroki

Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).
