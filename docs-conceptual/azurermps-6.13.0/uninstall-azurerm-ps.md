---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: bf1f81b4929ec066eeb888da4ba1303430f026b4
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586585"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="f3600-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3600-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="f3600-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="f3600-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="f3600-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="f3600-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="f3600-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="f3600-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="f3600-107">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3600-107">Uninstall from PowerShell</span></span>

<span data-ttu-id="f3600-108">Jeśli zainstalowano program Azure PowerShell za pomocą modułu PowerShellGet, można użyć polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="f3600-108">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="f3600-109">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="f3600-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="f3600-110">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="f3600-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="f3600-111">Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3600-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="f3600-112">Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="f3600-112">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="f3600-113">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f3600-113">Then, the script uninstalls the correct version of each submodule.</span></span>

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
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.minimumVersion}
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

<span data-ttu-id="f3600-114">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3600-114">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="f3600-115">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3600-115">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="f3600-116">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f3600-116">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="f3600-117">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="f3600-117">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="f3600-118">Dla ułatwienia poniższy skrypt zainstaluje wszystkie wersje usługi AzureRM __oprócz__ najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="f3600-118">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

## <a name="uninstall-msi"></a><span data-ttu-id="f3600-119">Odinstalowywanie pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="f3600-119">Uninstall MSI</span></span>

<span data-ttu-id="f3600-120">Jeśli zainstalowano program Azure PowerShell przy użyciu pakietu MSI, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3600-120">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="f3600-121">Platforma</span><span class="sxs-lookup"><span data-stu-id="f3600-121">Platform</span></span> | <span data-ttu-id="f3600-122">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="f3600-122">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="f3600-123">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3600-123">Windows 10</span></span> | <span data-ttu-id="f3600-124">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="f3600-124">Start > Settings > Apps</span></span> |
| <span data-ttu-id="f3600-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3600-125">Windows 7</span></span> </br><span data-ttu-id="f3600-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f3600-126">Windows 8</span></span> | <span data-ttu-id="f3600-127">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="f3600-127">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="f3600-128">Na tym ekranie na liście programów powinna być wyświetlana pozycja „Azure PowerShell” — w tym miejscu można odinstalować program.</span><span class="sxs-lookup"><span data-stu-id="f3600-128">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>
