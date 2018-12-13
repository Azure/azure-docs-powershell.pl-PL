---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 3828a6f9d60a68c2837cc201a50d8707324f4f0a
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217239"
---
# <a name="uninstall-the-azure-powershell-module"></a>Odinstalowywanie modułu programu Azure PowerShell

W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu. Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi-or-web-platform-installer"></a>Odinstalowywanie instalatora MSI lub instalatora platformy internetowej

Jeśli zainstalowano program Azure PowerShell przy użyciu pakietu MSI lub instalatora platformy internetowej, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.

| Platforma | Instrukcje |
|----------|--------------|
| Windows 10 | Start > Ustawienia > Aplikacje |
| Windows 7 </br>Windows 8 | Start > Panel sterowania > Programy > Odinstaluj program |

Na tym ekranie na liście programów powinna być wyświetlana pozycja „Azure PowerShell” — w tym miejscu można odinstalować program.

## <a name="uninstall-from-powershell"></a>Dezinstalacja z poziomu programu PowerShell

Jeśli zainstalowano program Azure PowerShell za pomocą modułu PowerShellGet, można użyć polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu. Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno. Dezinstalacja może być skomplikowana, jeśli masz wiele zainstalowanych wersji programu Azure PowerShell.

Poniżej przedstawiono skrypt, za pomocą którego można całkowicie usunąć jedną wersję programu Azure PowerShell. Skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych. Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell. W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.