---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: fcec2c713d1967a5a70df9b13aa30d9ff4625e9d
ms.sourcegitcommit: 0b5b0434fba7a752b0199256e04fa34f06aaf33a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/21/2019
ms.locfileid: "56464897"
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

Jeśli w systemie masz zainstalowany moduł Az i chcesz odinstalować moduł AzureRM, możesz skorzystać z jednej z dwóch prostych opcji, które nie wymagają uruchamiania powyższego skryptu `Uninstall-AllModules`. Metoda, której należy użyć, zależy od sposobu instalacji modułu AzureRM.
Jeśli nie masz pewności, najpierw zobacz kroki służące do odinstalowania pakietu MSI.

### <a name="uninstall-azure-powershell-msi"></a>Odinstalowywanie pakietu MSI programu Azure PowerShell

Jeśli moduły AzureRM programu Azure PowerShell zainstalowano przy użyciu pakietu MSI, musisz je odinstalować za pośrednictwem systemu Windows, a nie programu PowerShell.

| Platforma | Instrukcje |
|----------|--------------|
| Windows 10 | Start > Ustawienia > Aplikacje |
| Windows 7 </br>Windows 8 | Start > Panel sterowania > Programy > Odinstaluj program |

Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__. Jest to aplikacja do odinstalowania.

### <a name="uninstall-from-powershell"></a>Dezinstalacja z poziomu programu PowerShell

Jeśli moduł AzureRM zainstalowano z poziomu modułu PowerShellGet, moduły możesz usunąć przy użyciu nowego polecenia `Uninstall-AzureRM`. Spowoduje to usunięcie _wszystkich_ modułów AzureRM z Twojej maszyny, ale wymaga uprawnień administratora.

```powershell-interactive
Uninstall-AzureRm
```

Jeśli nie możesz pomyślnie uruchomić polecenia `Uninstall-AzureRM`, zamiast tego użyj skryptu `Uninstall-AllModules` podanego w tym artykule.
