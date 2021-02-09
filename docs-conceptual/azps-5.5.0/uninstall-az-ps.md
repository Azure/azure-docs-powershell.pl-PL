---
title: Odinstalowywanie programu Azure PowerShell
description: Jak w pełni odinstalować program Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012884"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="49d33-103">Jak odinstalować moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="49d33-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="49d33-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="49d33-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="49d33-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="49d33-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="49d33-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues), abyśmy mogli ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="49d33-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="49d33-107">Odinstalowywanie modułu Az</span><span class="sxs-lookup"><span data-stu-id="49d33-107">Uninstall the Az module</span></span>

<span data-ttu-id="49d33-108">Jeśli w systemie masz zainstalowany moduł Az i chcesz go odinstalować, możesz skorzystać z jednej z dwóch opcji.</span><span class="sxs-lookup"><span data-stu-id="49d33-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="49d33-109">Metoda, której należy użyć, zależy od sposobu instalacji modułu Az.</span><span class="sxs-lookup"><span data-stu-id="49d33-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="49d33-110">Jeśli nie masz pewności co do pierwotnej metody instalacji, najpierw wykonaj kroki pakietu MSI dotyczące odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="49d33-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="49d33-111">Opcja 1: Odinstalowywanie modułu Az programu PowerShell (MSI)</span><span class="sxs-lookup"><span data-stu-id="49d33-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="49d33-112">Jeśli zainstalowano moduł Az programu PowerShell przy użyciu pakietu MSI, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49d33-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="49d33-113">Platforma</span><span class="sxs-lookup"><span data-stu-id="49d33-113">Platform</span></span>         |                      <span data-ttu-id="49d33-114">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="49d33-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="49d33-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="49d33-115">Windows 10</span></span>               | <span data-ttu-id="49d33-116">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="49d33-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="49d33-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49d33-117">Windows 7</span></span> </br><span data-ttu-id="49d33-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="49d33-118">Windows 8</span></span> | <span data-ttu-id="49d33-119">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="49d33-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="49d33-120">Na tym ekranie na liście programów powinna być wyświetlana pozycja **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="49d33-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="49d33-121">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="49d33-121">This is the app to uninstall.</span></span> <span data-ttu-id="49d33-122">Jeśli nie widzisz tego programu na liście, oznacza to, że został on zainstalowany za pośrednictwem modułu PowerShellGet i musisz wykonać następny zestaw instrukcji.</span><span class="sxs-lookup"><span data-stu-id="49d33-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="49d33-123">Opcja 2: Odinstalowywanie modułu Az programu PowerShell (PowerShellGet)</span><span class="sxs-lookup"><span data-stu-id="49d33-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="49d33-124">Moduły Az można odinstalować za pomocą polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="49d33-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="49d33-125">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="49d33-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="49d33-126">Aby całkowicie usunąć moduł Az programu PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="49d33-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="49d33-127">Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49d33-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="49d33-128">Aby sprawdzić, które wersje modułu Az programu PowerShell są zainstalowane, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="49d33-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="49d33-129">Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="49d33-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="49d33-130">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="49d33-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="49d33-131">Do uruchomienia tego skryptu w zakresie innym niż **Proces** lub **Bieżący użytkownik** wymagany jest dostęp administratora.</span><span class="sxs-lookup"><span data-stu-id="49d33-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

<span data-ttu-id="49d33-132">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49d33-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="49d33-133">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję modułu Az programu PowerShell wraz z modułami podrzędnymi.</span><span class="sxs-lookup"><span data-stu-id="49d33-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="49d33-134">Po uruchomieniu skryptu zostaną wyświetlone właściwości **Name** (Nazwa), **Version** (Wersja) i **State** (Stan) każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="49d33-134">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="49d33-135">Aby uruchomić skrypt w celu sprawdzenia, co zostałoby usunięte, ale niczego nie usuwać, określ parametr `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="49d33-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> <span data-ttu-id="49d33-136">Jeśli ten skrypt nie może być dokładnie zgodny z zależnością w tej samej wersji do odinstalowania, nie spowoduje odinstalowania _żadnej_ wersji tej zależności.</span><span class="sxs-lookup"><span data-stu-id="49d33-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="49d33-137">Jest to spowodowane tym, że w systemie mogą istnieć inne wersje modułu docelowego oparte na tych zależnościach.</span><span class="sxs-lookup"><span data-stu-id="49d33-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="49d33-138">Uruchom poniższe przykładowe polecenie dla każdej wersji modułu Az programu PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="49d33-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="49d33-139">Dla ułatwienia poniższy skrypt odinstalowuje wszystkie wersje modułu Az **oprócz** najnowszej.</span><span class="sxs-lookup"><span data-stu-id="49d33-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="49d33-140">Odinstalowywanie modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="49d33-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="49d33-141">Jeśli w systemie masz zainstalowany moduł Az i chcesz odinstalować moduł AzureRM, możesz skorzystać z jednej z dwóch opcji.</span><span class="sxs-lookup"><span data-stu-id="49d33-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="49d33-142">Metoda, której należy użyć, zależy od sposobu instalacji modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="49d33-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="49d33-143">Jeśli nie masz pewności co do pierwotnej metody instalacji, najpierw wykonaj kroki pakietu MSI dotyczące odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="49d33-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="49d33-144">Opcja 1: Odinstalowywanie modułu AzureRM programu PowerShell (MSI)</span><span class="sxs-lookup"><span data-stu-id="49d33-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="49d33-145">Jeśli zainstalowano moduł AzureRM programu PowerShell przy użyciu pakietu MSI, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49d33-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="49d33-146">Platforma</span><span class="sxs-lookup"><span data-stu-id="49d33-146">Platform</span></span>         |                      <span data-ttu-id="49d33-147">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="49d33-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="49d33-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="49d33-148">Windows 10</span></span>               | <span data-ttu-id="49d33-149">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="49d33-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="49d33-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49d33-150">Windows 7</span></span> </br><span data-ttu-id="49d33-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="49d33-151">Windows 8</span></span> | <span data-ttu-id="49d33-152">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="49d33-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="49d33-153">Na tym ekranie na liście programów powinna być wyświetlana pozycja **Azure PowerShell** lub **Microsoft Azure PowerShell — miesiąc rok**.</span><span class="sxs-lookup"><span data-stu-id="49d33-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="49d33-154">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="49d33-154">This is the app to uninstall.</span></span> <span data-ttu-id="49d33-155">Jeśli nie widzisz tego programu na liście, oznacza to, że został on zainstalowany za pośrednictwem modułu PowerShellGet i musisz wykonać następny zestaw instrukcji.</span><span class="sxs-lookup"><span data-stu-id="49d33-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="49d33-156">Opcja 2: Odinstalowywanie modułu AzureRM programu PowerShell (PowerShellGet)</span><span class="sxs-lookup"><span data-stu-id="49d33-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="49d33-157">Jeśli moduł AzureRM został zainstalowany przy użyciu modułu PowerShellGet, możesz usunąć moduły za pomocą polecenia cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) dostępnego w module `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="49d33-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="49d33-158">Aby korzystać z modułu `Az.Accounts`, konieczne jest zainstalowanie modułu Az.</span><span class="sxs-lookup"><span data-stu-id="49d33-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="49d33-159">Równoczesne zainstalowanie modułów AzureRM i AZ nie jest obsługiwane, jednak moduł Az może służyć do natychmiastowego odinstalowania modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="49d33-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="49d33-160">Możesz zainstalować moduł Az i ominąć ostrzeżenie modułu AzureRM za pomocą następującego polecenia, jeśli nie masz jeszcze zainstalowanego modułu Az:</span><span class="sxs-lookup"><span data-stu-id="49d33-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="49d33-161">Po zainstalowaniu modułu Az następujące polecenie powoduje usunięcie _wszystkich_ modułów AzureRM z Twojej maszyny.</span><span class="sxs-lookup"><span data-stu-id="49d33-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="49d33-162">Wymaga ono uprawnień administratora.</span><span class="sxs-lookup"><span data-stu-id="49d33-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
