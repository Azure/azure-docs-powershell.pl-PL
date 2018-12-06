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
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828573"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="4e689-103">Odinstalowywanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4e689-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="4e689-104">W tym artykule wyjaśniono, jak odinstalować starszą wersję programu Azure PowerShell lub całkowicie usunąć go z systemu.</span><span class="sxs-lookup"><span data-stu-id="4e689-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="4e689-105">Jeśli chcesz całkowicie odinstalować program Azure PowerShell, przekaż nam opinię za pomocą polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="4e689-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="4e689-106">Jeśli trafisz na usterkę, będziemy wdzięczni za [zgłoszenie problemu w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="4e689-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="4e689-107">Odinstalowywanie instalatora MSI lub instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="4e689-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="4e689-108">Jeśli zainstalowano program Azure PowerShell przy użyciu pakietu MSI lub instalatora platformy internetowej, musisz odinstalować go za pośrednictwem systemu Windows, a nie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e689-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="4e689-109">Platforma</span><span class="sxs-lookup"><span data-stu-id="4e689-109">Platform</span></span> | <span data-ttu-id="4e689-110">Instrukcje</span><span class="sxs-lookup"><span data-stu-id="4e689-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="4e689-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4e689-111">Windows 10</span></span> | <span data-ttu-id="4e689-112">Start > Ustawienia > Aplikacje</span><span class="sxs-lookup"><span data-stu-id="4e689-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="4e689-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e689-113">Windows 7</span></span> </br><span data-ttu-id="4e689-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4e689-114">Windows 8</span></span> | <span data-ttu-id="4e689-115">Start > Panel sterowania > Programy > Odinstaluj program</span><span class="sxs-lookup"><span data-stu-id="4e689-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="4e689-116">Na tym ekranie na liście programów powinna być wyświetlana pozycja „Azure PowerShell” — w tym miejscu można odinstalować program.</span><span class="sxs-lookup"><span data-stu-id="4e689-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="4e689-117">Dezinstalacja z poziomu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="4e689-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="4e689-118">Jeśli zainstalowano program Azure PowerShell za pomocą modułu PowerShellGet, można użyć polecenia cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="4e689-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="4e689-119">Jednak polecenie `Uninstall-Module` umożliwia odinstalowanie tylko jednego modułu.</span><span class="sxs-lookup"><span data-stu-id="4e689-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="4e689-120">Aby całkowicie usunąć program Azure PowerShell, musisz odinstalować każdy moduł osobno.</span><span class="sxs-lookup"><span data-stu-id="4e689-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="4e689-121">Dezinstalacja może być skomplikowana, jeśli masz wiele zainstalowanych wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e689-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="4e689-122">Poniżej przedstawiono skrypt, za pomocą którego można całkowicie usunąć jedną wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e689-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="4e689-123">Skrypt wysyła zapytanie do galerii programu PowerShell w celu uzyskania listy zależnych modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="4e689-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="4e689-124">Następnie skrypt odinstalowuje odpowiednią wersję każdego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4e689-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="4e689-125">Aby użyć tej funkcji, skopiuj kod i wklej go do sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e689-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="4e689-126">W poniższym przykładzie pokazano, jak uruchomić funkcję, aby usunąć starszą wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e689-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="4e689-127">Po uruchomieniu skryptu zostanie wyświetlona nazwa i wersja każdego odinstalowywanego modułu podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4e689-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="4e689-128">Uruchom to polecenie dla każdej wersji programu Azure PowerShell, która ma zostać odinstalowana.</span><span class="sxs-lookup"><span data-stu-id="4e689-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>