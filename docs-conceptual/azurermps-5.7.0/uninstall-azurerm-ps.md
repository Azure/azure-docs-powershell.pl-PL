---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6fc8ff8af0355ab705007f5df81d2aba8444c266
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/14/2020
ms.locfileid: "83388010"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="4f6b8-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f6b8-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="4f6b8-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="4f6b8-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="4f6b8-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="4f6b8-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="4f6b8-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="4f6b8-107">Odinstalowywanie instalatora MSI lub instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="4f6b8-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="4f6b8-108">Jeśli zainstalowano program Azure PowerShell przy użyciu pakietu MSI lub instalatora platformy internetowej, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="4f6b8-109">Platforma</span><span class="sxs-lookup"><span data-stu-id="4f6b8-109">Platform</span></span> | <span data-ttu-id="4f6b8-110">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="4f6b8-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="4f6b8-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4f6b8-111">Windows 10</span></span> | <span data-ttu-id="4f6b8-112">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="4f6b8-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="4f6b8-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f6b8-113">Windows 7</span></span> </br><span data-ttu-id="4f6b8-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f6b8-114">Windows 8</span></span> | <span data-ttu-id="4f6b8-115">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="4f6b8-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="4f6b8-116">Na tym ekranie na liście programów powinna być wyświetlana pozycja „Azure PowerShell” — w tym miejscu można odinstalować program.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="4f6b8-117">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f6b8-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="4f6b8-118">Jeśli zainstalowano program Azure PowerShell za pomocą modułu PowerShellGet, można użyć polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="4f6b8-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="4f6b8-119">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="4f6b8-120">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="4f6b8-121">Dezinstalacja może być skomplikowana, jeśli masz wiele zainstalowanych wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="4f6b8-122">Poniżej przedstawiono skrypt, za pomocą którego można całkowicie usunąć jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="4f6b8-123">Skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="4f6b8-124">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="4f6b8-125">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="4f6b8-126">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="4f6b8-127">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="4f6b8-128">Aby uruchomić skrypt w celu zobaczenia, co zostałoby usunięte, ale niczego nie usuwać, użyj opcji `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="4f6b8-129">Jeśli ten skrypt nie może być dokładnie zgodny z zależnością w tej samej wersji do odinstalowania, nie spowoduje odinstalowania _żadnej_ wersji tej zależności.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="4f6b8-130">Jest to spowodowane tym, że w systemie mogą istnieć inne wersje modułu docelowego oparte na tych zależnościach.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="4f6b8-131">W tym przypadku są wyświetlane dostępne wersje zależności.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="4f6b8-132">Możesz usunąć wszystkie starsze wersje ręcznie za pomocą polecenia `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="4f6b8-133">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="4f6b8-134">Dla ułatwienia poniższy skrypt zainstaluje wszystkie wersje usługi AzureRM __oprócz__ najnowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="4f6b8-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
