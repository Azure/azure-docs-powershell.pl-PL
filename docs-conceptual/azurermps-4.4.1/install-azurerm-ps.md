---
title: Instalowanie i konfigurowanie programu Azure PowerShell | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c4aa030a7d95f5b22ceeff9438af506ced5c8cb5
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428044"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w programie PowerShell 5.x w systemie Windows przy użyciu modułu PowerShellGet. Moduł PowerShellGet i funkcja zarządzania modułami to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).

Klasyczny model wdrażania platformy Azure nie jest obsługiwany przez tę wersję programu Azure PowerShell. Aby uzyskać pomoc techniczną w przypadku wdrożeń klasycznych, postępuj zgodnie z instrukcjami na stronie [Instalowanie modułu zarządzania usługami programu Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

> [!IMPORTANT]
> Moduł AzureRM nie jest obsługiwany w systemach macOS i Linux. Aby używać poleceń cmdlet programu Azure PowerShell na tych platformach, należy [zainstalować moduł Az](/powershell/azure/install-az-ps).

## <a name="step-1-install-powershellget"></a>Krok 1. Zainstaluj moduł PowerShellGet

Instalowanie elementów z Galerii programu PowerShell wymaga modułu PowerShellGet. Upewnij się, że masz odpowiednią wersję modułu PowerShellGet oraz spełnione inne wymagania systemowe. Uruchom następujące polecenie, aby sprawdzić, czy w Twoim systemie został zainstalowany moduł PowerShellGet.


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Potrzebujesz programu PowerShellGet w wersji 1.1.2.0 lub nowszej. Aby zaktualizować program PowerShellGet, użyj następującego polecenia:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Jeśli nie masz zainstalowanego modułu PowerShellGet, zobacz sekcję [Jak uzyskać moduł PowerShellGet](#how-to-get-powershellget) w niniejszym artykule.

> [!NOTE]
> Korzystanie z modułu PowerShellGet wymaga zasad wykonania pozwalających uruchamiać skrypty. Aby uzyskać więcej informacji na temat zasad wykonania programu PowerShell, zobacz [Informacje o zasadach wykonania](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Moduł opisany w tym dokumencie (AzureRM) korzysta z programu .NET Framework. Dlatego jest on niezgodny z programem PowerShell 6.0, który korzysta z platformy .NET Core. Jeśli korzystasz z programu PowerShell 6.0, postępuj zgodnie z [instrukcjami dotyczącymi instalacji dla systemów macOS i Linux](/powershell/azure/install-az-ps).

## <a name="step-2-install-azure-powershell"></a>Krok 2. Instalowanie programu Azure PowerShell

Instalacja programu Azure PowerShell z Galerii programu PowerShell wymaga podniesionych uprawnień. Uruchom następujące polecenie z sesji programu PowerShell z podwyższonym poziomem uprawnień:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet. Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Wybierz odpowiedź „Tak” lub „Tak na wszystkie”, aby kontynuować instalację.

> [!NOTE]
> Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.

Moduł AzureRM to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager. Po zainstalowaniu modułu AzureRM każdy moduł programu Azure PowerShell, który nie został wcześniej zainstalowany, zostanie pobrany i zainstalowany z Galerii programu PowerShell.

Jeśli masz zainstalowaną poprzednią wersję programu Azure PowerShell, może wystąpić błąd. Aby rozwiązać ten problem, zobacz [Aktualizowanie do nowej wersji programu Azure PowerShell](#update-azps) w dalszej części tego artykułu.

## <a name="step-3-load-the-azurerm-module"></a>Krok 3: Załaduj moduł AzureRM

Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell. Należy to zrobić w ramach normalnej sesji programu PowerShell (bez podwyższonego poziomu uprawnień). Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Następne kroki

Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz następujące artykuły:

* [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Zgłaszanie problemów i przesyłanie opinii

Jeśli występują jakiekolwiek problemy związane z narzędziem, prześlij zgłoszenie do sekcji [Problemy](https://github.com/Azure/azure-powershell/issues) repozytorium GitHub. Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Często zadawane pytania

### <a name="how-to-get-powershellget"></a>Jak uzyskać moduł PowerShellGet

|Wersja systemu operacyjnego|Instrukcje dotyczące instalacji|
|---|---|
|Mam system Windows 10 lub Windows Server 2016|Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym|
|Chcę przeprowadzić uaktualnienie do programu PowerShell 5|[Zainstaluj najnowszą wersję platformy WMF](https://www.microsoft.com/download/details.aspx?id=54616)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/>Sprawdzanie wersji programu Azure PowerShell

Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane. Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-InstalledModule AzureRM` z wiersza polecenia.

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Obsługa klasycznych metod wdrażania

Jeśli masz wdrożenia korzystające z klasycznego modelu wdrażania, możesz zainstalować wersję zarządzania usługą programu Azure PowerShell. Aby uzyskać więcej informacji, zobacz [Instalowanie modułu Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps). Moduły Azure i AzureRM mają wspólne zależności. Jeśli korzystasz z modułów Azure i AzureRM, należy zainstalować tę samą wersję każdego pakietu.

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/>Uaktualnianie do nowej wersji programu Azure PowerShell

Jeśli masz zainstalowaną poprzednią wersję programu Azure PowerShell obejmującą moduł zarządzania usługami, może wystąpić następujący błąd:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Zgodnie z treścią komunikatu o błędzie trzeba zainstalować moduł, podając parametr -AllowClobber. Użyj następującego polecenia:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Aby uzyskać więcej informacji, zobacz temat pomocy dotyczący parametru [Install-Module](/powershell/module/powershellget/install-module).

### <a name="installing-module-versions-side-by-side"></a>Instalowanie wersji modułu obok siebie

Metoda instalacji PowerShellGet jest jedyną metodą, która obsługuje instalowanie wielu wersji. Na przykład możesz mieć skrypty napisane przy użyciu poprzedniej wersji programu Azure PowerShell, do aktualizacji której nie masz czasu lub zasobów. Następujące polecenia przedstawiają sposób instalowania wielu wersji programu Azure PowerShell:

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Tylko jedna wersja modułu może zostać załadowana w sesji programu PowerShell. Musisz otworzyć nowe okno programu PowerShell i użyć polecenia `Import-Module`, aby zaimportować określoną wersję poleceń cmdlet modułu AzureRM:

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> Wersja 2.1.0 i wersja 1.2.6 to pierwsze wersje modułu przeznaczone do instalacji i używania obok siebie. Załadowanie starszej wersji programu Azure PowerShell powoduje załadowanie niezgodnych wersji modułu **AzureRM.Profile**. W wyniku tego każde wykonanie polecenia cmdlet powoduje wyświetlenie polecenia cmdlet z monitem o zalogowanie się.

### <a name="other-installation-methods"></a>Inne metody instalacji

Aby uzyskać informacje o instalowaniu za pomocą Instalatora platformy sieci Web lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md)