---
title: Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 198c9476b06c818fd3f7cb5ac3ac465497cac9cf
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216589"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet

W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w środowisku systemu Windows przy użyciu modułu PowerShellGet. Moduł PowerShellGet i funkcja zarządzania modułami to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).

Aby uzyskać instrukcje dotyczące instalacji programu Azure PowerShell na innych platformach, zobacz [Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux](install-azurermps-maclinux.md).

Klasyczny model wdrażania platformy Azure nie jest obsługiwany przez tę wersję programu Azure PowerShell. Aby uzyskać pomoc techniczną w przypadku wdrożeń klasycznych, postępuj zgodnie z instrukcjami na stronie [Instalowanie modułu zarządzania usługami programu Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a>Wymagania

Począwszy od programu Azure PowerShell w wersji 6.0, jest wymagany program PowerShell w wersji 5.0. Aby sprawdzić wersję programu PowerShell na maszynie, uruchom następujące polecenie:

```powershell-interactive
$PSVersionTable.PSVersion
```

Jeśli masz nieaktualną wersję, zobacz [Upgrading existing Windows PowerShell (Uaktualnianie istniejącego programu Windows PowerShell)](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

> [!IMPORTANT]
> Moduł opisany w tym dokumencie (AzureRM) korzysta z programu .NET Framework. Dlatego jest on niezgodny z programem PowerShell 6.0, który korzysta z platformy .NET Core. Jeśli korzystasz z programu PowerShell 6.0, postępuj zgodnie z [instrukcjami dotyczącymi instalacji dla systemów macOS i Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Instalacja modułu Azure PowerShell

Do zainstalowania modułów z galerii programu PowerShell jest wymagany podwyższony poziom uprawnień. Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień:

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
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

Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module AzureRM`. Ze względu na strukturę modułu może to potrwać kilka sekund.


Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz. Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aktualizowanie modułu programu Azure PowerShell

Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module). To polecenie __nie__ powoduje odinstalowania wcześniejszych wersji.

```powershell-interactive
Update-Module -Name AzureRM
```

Jeśli chcesz usunąć starsze wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Korzystanie z wielu wersji programu Azure PowerShell

Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell. Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:

```powershell-interactive
Get-Module -Name AzureRM -ListAvailable | select Name,Version
```

Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).

Obecność więcej niż jednej wersji może być potrzebna w przypadku pracy z lokalnymi zasobami usługi Azure Stack, korzystania ze starszej wersji systemu Windows lub używania klasycznego modelu wdrażania platformy Azure. Aby zainstalować starszą wersję, podaj argument `-RequiredVersion` podczas instalacji.

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
