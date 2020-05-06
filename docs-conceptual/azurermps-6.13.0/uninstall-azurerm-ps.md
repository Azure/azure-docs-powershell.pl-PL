---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 17197b77e26ccf0e41b5faf3cbbde34338b28167
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037725"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="09351-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="09351-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="09351-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="09351-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="09351-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="09351-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="09351-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="09351-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="09351-107">Odinstalowywanie pakietu MSI programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="09351-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="09351-108">Jeśli zainstalowano program Azure PowerShell przy użyciu pakietu MSI, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09351-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="09351-109">Platforma</span><span class="sxs-lookup"><span data-stu-id="09351-109">Platform</span></span> | <span data-ttu-id="09351-110">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="09351-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="09351-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="09351-111">Windows 10</span></span> | <span data-ttu-id="09351-112">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="09351-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="09351-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09351-113">Windows 7</span></span> </br><span data-ttu-id="09351-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09351-114">Windows 8</span></span> | <span data-ttu-id="09351-115">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="09351-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="09351-116">Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="09351-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="09351-117">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="09351-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="09351-118">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="09351-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="09351-119">Jeśli zainstalowano program Azure PowerShell za pomocą modułu PowerShellGet, można użyć polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="09351-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="09351-120">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="09351-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="09351-121">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="09351-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="09351-122">Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09351-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="09351-123">Aby sprawdzić, jakie wersje programu Azure PowerShell są aktualnie zainstalowane, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="09351-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="09351-124">Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="09351-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="09351-125">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="09351-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="09351-126">Aby uruchomić ten skrypt w zakresie innym niż `Process` lub `CurrentUser`, będziesz potrzebować dostępu administratora.</span><span class="sxs-lookup"><span data-stu-id="09351-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

<span data-ttu-id="09351-127">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09351-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="09351-128">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09351-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="09351-129">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="09351-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="09351-130">Aby uruchomić skrypt w celu zobaczenia, co zostałoby usunięte, ale niczego nie usuwać, użyj opcji `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="09351-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="09351-131">Jeśli ten skrypt nie może być dokładnie zgodny z zależnością w tej samej wersji do odinstalowania, nie spowoduje odinstalowania _żadnej_ wersji tej zależności.</span><span class="sxs-lookup"><span data-stu-id="09351-131">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="09351-132">Jest to spowodowane tym, że w systemie mogą istnieć inne wersje modułu docelowego oparte na tych zależnościach.</span><span class="sxs-lookup"><span data-stu-id="09351-132">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="09351-133">W tym przypadku są wyświetlane dostępne wersje zależności.</span><span class="sxs-lookup"><span data-stu-id="09351-133">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="09351-134">Możesz usunąć wszystkie starsze wersje ręcznie za pomocą polecenia `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="09351-134">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="09351-135">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="09351-135">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="09351-136">Dla ułatwienia poniższy skrypt zainstaluje wszystkie wersje usługi AzureRM __oprócz__ najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="09351-136">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
