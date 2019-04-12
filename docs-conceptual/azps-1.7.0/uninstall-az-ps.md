---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6a34ac1821c3cec359d0d64664d3f1689621b304
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363740"
---
# <a name="uninstall-the-azure-powershell-module"></a>Odinstalowywanie modułu programu Azure PowerShell

W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu. Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-the-az-module"></a>Odinstalowywanie modułu Az

Moduły Az można odinstalować za pomocą polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu. Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno. Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.

Aby sprawdzić, jakie wersje programu Azure PowerShell są aktualnie zainstalowane, uruchom następujące polecenie:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych. Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego. Aby uruchomić ten skrypt w zakresie innym niż `Process` lub `CurrentUser`, będziesz potrzebować dostępu administratora.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell. W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego. Aby uruchomić skrypt w celu zobaczenia, co zostałoby usunięte, ale niczego nie usuwać, użyj opcji `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana. Dla ułatwienia poniższy skrypt odinstaluje wszystkie wersje modułu Az __oprócz__ najnowszej.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Odinstalowywanie modułu AzureRM

Jeśli w systemie masz zainstalowany moduł Az i chcesz odinstalować moduł AzureRM, możesz skorzystać z jednej z dwóch opcji, które nie wymagają uruchamiania powyższego skryptu `Uninstall-AllModules`. Metoda, której należy użyć, zależy od sposobu instalacji modułu AzureRM.
Jeśli nie masz pewności, najpierw wykonaj kroki służące do odinstalowania pakietu MSI.

### <a name="uninstall-azure-powershell-msi"></a>Odinstalowywanie pakietu MSI programu Azure PowerShell

Jeśli moduły AzureRM programu Azure PowerShell zainstalowano przy użyciu pakietu MSI, musisz je odinstalować za pośrednictwem systemu Windows, a nie programu PowerShell.

| Platforma | Instrukcje |
|----------|--------------|
| Windows 10 | Start > Ustawienia > Aplikacje |
| Windows 7 </br>Windows 8 | Start > Panel sterowania > Programy > Odinstaluj program |

Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__. To jest aplikacja do odinstalowania. Jeśli nie widzisz tego programu na liście, oznacza to, że został on zainstalowany za pośrednictwem modułu PowerShellGet i musisz wykonać następny zestaw instrukcji.

### <a name="uninstall-from-powershell"></a>Dezinstalacja z poziomu programu PowerShell

Jeśli moduł AzureRM został zainstalowany przy użyciu modułu PowerShellGet, możesz usunąć moduły za pomocą polecenia [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) dostępnego w module `Az.Accounts`. Spowoduje to usunięcie _wszystkich_ modułów AzureRM z Twojej maszyny, ale wymaga uprawnień administratora.

```powershell-interactive
Uninstall-AzureRm
```

Jeśli nie możesz pomyślnie uruchomić polecenia `Uninstall-AzureRM`, zamiast tego użyj skryptu `Uninstall-AllModules` podanego w tym artykule.