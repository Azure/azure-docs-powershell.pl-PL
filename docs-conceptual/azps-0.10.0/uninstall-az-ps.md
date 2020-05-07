---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 10/22/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 37f152fb43e23c361544db4a738d58911099da1f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445972"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="04a32-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="04a32-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="04a32-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="04a32-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="04a32-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="04a32-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="04a32-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues), abyśmy mogli ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="04a32-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="04a32-107">Odinstalowywanie programu Azure PowerShell za pomocą instalatora MSI</span><span class="sxs-lookup"><span data-stu-id="04a32-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="04a32-108">Jeśli zainstalowano program Azure PowerShell przy użyciu pakietu MSI, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a32-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="04a32-109">Platforma</span><span class="sxs-lookup"><span data-stu-id="04a32-109">Platform</span></span> | <span data-ttu-id="04a32-110">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="04a32-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="04a32-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="04a32-111">Windows 10</span></span> | <span data-ttu-id="04a32-112">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="04a32-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="04a32-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04a32-113">Windows 7</span></span> </br><span data-ttu-id="04a32-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04a32-114">Windows 8</span></span> | <span data-ttu-id="04a32-115">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="04a32-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="04a32-116">Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="04a32-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="04a32-117">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="04a32-117">This is the app to uninstall.</span></span> <span data-ttu-id="04a32-118">Jeśli nie widzisz tego programu na liście, oznacza to, że został on zainstalowany za pośrednictwem modułu PowerShellGet i musisz wykonać następny zestaw instrukcji.</span><span class="sxs-lookup"><span data-stu-id="04a32-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="04a32-119">Odinstalowywanie programu Azure PowerShell za pomocą modułu PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="04a32-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="04a32-120">Moduły Az można odinstalować za pomocą polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="04a32-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="04a32-121">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="04a32-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="04a32-122">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="04a32-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="04a32-123">Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a32-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="04a32-124">Aby sprawdzić, jakie wersje programu Azure PowerShell są aktualnie zainstalowane, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="04a32-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

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

<span data-ttu-id="04a32-125">Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="04a32-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="04a32-126">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="04a32-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="04a32-127">Aby uruchomić ten skrypt w zakresie innym niż `Process` lub `CurrentUser`, będziesz potrzebować dostępu administratora.</span><span class="sxs-lookup"><span data-stu-id="04a32-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="04a32-128">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a32-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="04a32-129">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a32-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="04a32-130">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="04a32-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="04a32-131">Aby uruchomić skrypt w celu zobaczenia, co zostałoby usunięte, ale niczego nie usuwać, użyj opcji `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="04a32-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="04a32-132">Jeśli ten skrypt nie może być dokładnie zgodny z zależnością w tej samej wersji do odinstalowania, nie spowoduje odinstalowania _żadnej_ wersji tej zależności.</span><span class="sxs-lookup"><span data-stu-id="04a32-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="04a32-133">Jest to spowodowane tym, że w systemie mogą istnieć inne wersje modułu docelowego oparte na tych zależnościach.</span><span class="sxs-lookup"><span data-stu-id="04a32-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="04a32-134">W tym przypadku są wyświetlane dostępne wersje zależności.</span><span class="sxs-lookup"><span data-stu-id="04a32-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="04a32-135">Możesz usunąć wszystkie starsze wersje ręcznie za pomocą polecenia `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="04a32-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="04a32-136">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="04a32-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="04a32-137">Dla ułatwienia poniższy skrypt odinstaluje wszystkie wersje modułu Az __oprócz__ najnowszej.</span><span class="sxs-lookup"><span data-stu-id="04a32-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="04a32-138">Odinstalowywanie modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="04a32-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="04a32-139">Jeśli w systemie masz zainstalowany moduł Az i chcesz odinstalować moduł AzureRM, możesz skorzystać z jednej z dwóch opcji, które nie wymagają uruchamiania powyższego skryptu `Uninstall-AllModules`.</span><span class="sxs-lookup"><span data-stu-id="04a32-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="04a32-140">Metoda, której należy użyć, zależy od sposobu instalacji modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="04a32-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="04a32-141">Jeśli nie masz pewności co do pierwotnej metody instalacji, najpierw wykonaj kroki służące do odinstalowania pakietu MSI.</span><span class="sxs-lookup"><span data-stu-id="04a32-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="04a32-142">Odinstalowywanie pakietu MSI programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="04a32-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="04a32-143">Jeśli moduły AzureRM programu Azure PowerShell zainstalowano przy użyciu pakietu MSI, musisz je odinstalować za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a32-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="04a32-144">Platforma</span><span class="sxs-lookup"><span data-stu-id="04a32-144">Platform</span></span> | <span data-ttu-id="04a32-145">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="04a32-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="04a32-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="04a32-146">Windows 10</span></span> | <span data-ttu-id="04a32-147">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="04a32-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="04a32-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04a32-148">Windows 7</span></span> </br><span data-ttu-id="04a32-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04a32-149">Windows 8</span></span> | <span data-ttu-id="04a32-150">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="04a32-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="04a32-151">Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__ lub __Microsoft Azure PowerShell — miesiąc rok__.</span><span class="sxs-lookup"><span data-stu-id="04a32-151">Once on this screen you should see __Azure PowerShell__ or __Microsoft Azure PowerShell - Month Year__ in the program listing.</span></span> <span data-ttu-id="04a32-152">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="04a32-152">This is the app to uninstall.</span></span> <span data-ttu-id="04a32-153">Jeśli nie widzisz tego programu na liście, oznacza to, że został on zainstalowany za pośrednictwem modułu PowerShellGet i musisz wykonać następny zestaw instrukcji.</span><span class="sxs-lookup"><span data-stu-id="04a32-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="04a32-154">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="04a32-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="04a32-155">Jeśli moduł AzureRM został zainstalowany przy użyciu modułu PowerShellGet, możesz usunąć moduły za pomocą polecenia [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) dostępnego w module `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="04a32-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="04a32-156">Spowoduje to usunięcie _wszystkich_ modułów AzureRM z Twojej maszyny, ale wymaga uprawnień administratora.</span><span class="sxs-lookup"><span data-stu-id="04a32-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
<span data-ttu-id="04a32-157">lub</span><span class="sxs-lookup"><span data-stu-id="04a32-157">or</span></span>
```powershell-interactive
Uninstall-Module AzureRm
```

<span data-ttu-id="04a32-158">Jeśli nie możesz pomyślnie uruchomić polecenia `Uninstall-AzureRM`, zamiast tego uruchom [skrypt `Uninstall-AllModules`](#uninstall-script) podany w tym artykule, korzystając z następującego wywołania:</span><span class="sxs-lookup"><span data-stu-id="04a32-158">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
<span data-ttu-id="04a32-159">lub</span><span class="sxs-lookup"><span data-stu-id="04a32-159">or</span></span>
```powershell-interactive
foreach ($module in (Get-Module -ListAvailable AzureRM*).Name |Get-Unique) {
   write-host "Removing Module $module"
   Uninstall-module $module
}
```
