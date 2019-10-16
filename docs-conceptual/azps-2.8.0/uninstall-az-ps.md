---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: e71b4d0d662b29a32610fecb36351532040428e4
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370196"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="52def-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="52def-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="52def-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="52def-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="52def-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="52def-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="52def-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues), abyśmy mogli ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="52def-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="52def-107">Odinstalowywanie modułu Az</span><span class="sxs-lookup"><span data-stu-id="52def-107">Uninstall the Az module</span></span>

<span data-ttu-id="52def-108">Moduły Az można odinstalować za pomocą polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="52def-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="52def-109">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="52def-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="52def-110">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="52def-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="52def-111">Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52def-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="52def-112">Aby sprawdzić, jakie wersje programu Azure PowerShell są aktualnie zainstalowane, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="52def-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="52def-113">Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="52def-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="52def-114">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="52def-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="52def-115">Aby uruchomić ten skrypt w zakresie innym niż `Process` lub `CurrentUser`, będziesz potrzebować dostępu administratora.</span><span class="sxs-lookup"><span data-stu-id="52def-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="52def-116">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52def-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="52def-117">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52def-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="52def-118">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="52def-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="52def-119">Aby uruchomić skrypt w celu zobaczenia, co zostałoby usunięte, ale niczego nie usuwać, użyj opcji `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="52def-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="52def-120">Jeśli ten skrypt nie może być dokładnie zgodny z zależnością w tej samej wersji do odinstalowania, nie spowoduje odinstalowania _żadnej_ wersji tej zależności.</span><span class="sxs-lookup"><span data-stu-id="52def-120">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="52def-121">Jest to spowodowane tym, że w systemie mogą istnieć inne wersje modułu docelowego oparte na tych zależnościach.</span><span class="sxs-lookup"><span data-stu-id="52def-121">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="52def-122">W tym przypadku są wyświetlane dostępne wersje zależności.</span><span class="sxs-lookup"><span data-stu-id="52def-122">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="52def-123">Możesz usunąć wszystkie starsze wersje ręcznie za pomocą polecenia `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="52def-123">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="52def-124">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="52def-124">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="52def-125">Dla ułatwienia poniższy skrypt odinstaluje wszystkie wersje modułu Az __oprócz__ najnowszej.</span><span class="sxs-lookup"><span data-stu-id="52def-125">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="52def-126">Odinstalowywanie modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="52def-126">Uninstall the AzureRM module</span></span>

<span data-ttu-id="52def-127">Jeśli w systemie masz zainstalowany moduł Az i chcesz odinstalować moduł AzureRM, możesz skorzystać z jednej z dwóch opcji, które nie wymagają uruchamiania powyższego skryptu `Uninstall-AllModules`.</span><span class="sxs-lookup"><span data-stu-id="52def-127">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="52def-128">Metoda, której należy użyć, zależy od sposobu instalacji modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="52def-128">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="52def-129">Jeśli nie masz pewności co do pierwotnej metody instalacji, najpierw wykonaj kroki służące do odinstalowania pakietu MSI.</span><span class="sxs-lookup"><span data-stu-id="52def-129">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="52def-130">Odinstalowywanie pakietu MSI programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="52def-130">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="52def-131">Jeśli moduły AzureRM programu Azure PowerShell zainstalowano przy użyciu pakietu MSI, musisz je odinstalować za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52def-131">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="52def-132">Platforma</span><span class="sxs-lookup"><span data-stu-id="52def-132">Platform</span></span> | <span data-ttu-id="52def-133">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="52def-133">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="52def-134">Windows 10</span><span class="sxs-lookup"><span data-stu-id="52def-134">Windows 10</span></span> | <span data-ttu-id="52def-135">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="52def-135">Start > Settings > Apps</span></span> |
| <span data-ttu-id="52def-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52def-136">Windows 7</span></span> </br><span data-ttu-id="52def-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52def-137">Windows 8</span></span> | <span data-ttu-id="52def-138">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="52def-138">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="52def-139">Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="52def-139">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="52def-140">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="52def-140">This is the app to uninstall.</span></span> <span data-ttu-id="52def-141">Jeśli nie widzisz tego programu na liście, oznacza to, że został on zainstalowany za pośrednictwem modułu PowerShellGet i musisz wykonać następny zestaw instrukcji.</span><span class="sxs-lookup"><span data-stu-id="52def-141">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="52def-142">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="52def-142">Uninstall from PowerShell</span></span>

<span data-ttu-id="52def-143">Jeśli moduł AzureRM został zainstalowany przy użyciu modułu PowerShellGet, możesz usunąć moduły za pomocą polecenia [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) dostępnego w module `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="52def-143">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="52def-144">Spowoduje to usunięcie _wszystkich_ modułów AzureRM z Twojej maszyny, ale wymaga uprawnień administratora.</span><span class="sxs-lookup"><span data-stu-id="52def-144">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="52def-145">Jeśli nie możesz pomyślnie uruchomić polecenia `Uninstall-AzureRM`, zamiast tego uruchom [skrypt `Uninstall-AllModules`](#uninstall-script) podany w tym artykule, korzystając z następującego wywołania:</span><span class="sxs-lookup"><span data-stu-id="52def-145">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```