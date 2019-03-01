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
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837609"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="fdf06-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fdf06-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="fdf06-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="fdf06-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="fdf06-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="fdf06-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="fdf06-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="fdf06-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="fdf06-107">Odinstalowywanie modułu Az</span><span class="sxs-lookup"><span data-stu-id="fdf06-107">Uninstall the Az module</span></span>

<span data-ttu-id="fdf06-108">Moduły Az można odinstalować za pomocą polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="fdf06-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="fdf06-109">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="fdf06-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="fdf06-110">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="fdf06-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="fdf06-111">Dezinstalacja może być skomplikowana, jeśli masz zainstalowaną więcej niż jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fdf06-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="fdf06-112">Aby sprawdzić, jakie wersje programu Azure PowerShell są aktualnie zainstalowane, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="fdf06-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="fdf06-113">Poniższy skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="fdf06-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="fdf06-114">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="fdf06-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="fdf06-115">Aby uruchomić ten skrypt w zakresie innym niż `Process` lub `CurrentUser`, będziesz potrzebować dostępu administratora.</span><span class="sxs-lookup"><span data-stu-id="fdf06-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="fdf06-116">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fdf06-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="fdf06-117">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fdf06-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="fdf06-118">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="fdf06-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="fdf06-119">Aby uruchomić skrypt w celu zobaczenia, co zostałoby usunięte, ale niczego nie usuwać, użyj opcji `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="fdf06-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="fdf06-120">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="fdf06-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="fdf06-121">Dla ułatwienia poniższy skrypt odinstaluje wszystkie wersje modułu Az __oprócz__ najnowszej.</span><span class="sxs-lookup"><span data-stu-id="fdf06-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="fdf06-122">Odinstalowywanie modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="fdf06-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="fdf06-123">Jeśli w systemie masz zainstalowany moduł Az i chcesz odinstalować moduł AzureRM, możesz skorzystać z jednej z dwóch prostych opcji, które nie wymagają uruchamiania powyższego skryptu `Uninstall-AllModules`.</span><span class="sxs-lookup"><span data-stu-id="fdf06-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two simple options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="fdf06-124">Metoda, której należy użyć, zależy od sposobu instalacji modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="fdf06-124">Which method you follow depends on how you installed AzureRM.</span></span>
<span data-ttu-id="fdf06-125">Jeśli nie masz pewności, najpierw zobacz kroki służące do odinstalowania pakietu MSI.</span><span class="sxs-lookup"><span data-stu-id="fdf06-125">If you're not sure, check the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="fdf06-126">Odinstalowywanie pakietu MSI programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fdf06-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="fdf06-127">Jeśli moduły AzureRM programu Azure PowerShell zainstalowano przy użyciu pakietu MSI, musisz je odinstalować za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fdf06-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="fdf06-128">Platforma</span><span class="sxs-lookup"><span data-stu-id="fdf06-128">Platform</span></span> | <span data-ttu-id="fdf06-129">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="fdf06-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="fdf06-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fdf06-130">Windows 10</span></span> | <span data-ttu-id="fdf06-131">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="fdf06-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="fdf06-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fdf06-132">Windows 7</span></span> </br><span data-ttu-id="fdf06-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fdf06-133">Windows 8</span></span> | <span data-ttu-id="fdf06-134">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="fdf06-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="fdf06-135">Na tym ekranie na liście programów powinna być wyświetlana pozycja __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="fdf06-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="fdf06-136">To jest aplikacja do odinstalowania.</span><span class="sxs-lookup"><span data-stu-id="fdf06-136">This is the app to uninstall.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="fdf06-137">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="fdf06-137">Uninstall from PowerShell</span></span>

<span data-ttu-id="fdf06-138">Jeśli moduł AzureRM zainstalowano z poziomu modułu PowerShellGet, moduły możesz usunąć przy użyciu nowego polecenia `Uninstall-AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="fdf06-138">If you installed AzureRM from PowerShellGet, then you can remove the modules with the new `Uninstall-AzureRM` command.</span></span> <span data-ttu-id="fdf06-139">Spowoduje to usunięcie _wszystkich_ modułów AzureRM z Twojej maszyny, ale wymaga uprawnień administratora.</span><span class="sxs-lookup"><span data-stu-id="fdf06-139">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="fdf06-140">Jeśli nie możesz pomyślnie uruchomić polecenia `Uninstall-AzureRM`, zamiast tego użyj skryptu `Uninstall-AllModules` podanego w tym artykule.</span><span class="sxs-lookup"><span data-stu-id="fdf06-140">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>
