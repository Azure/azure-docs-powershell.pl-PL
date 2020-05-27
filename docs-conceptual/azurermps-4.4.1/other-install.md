---
title: Inne metody instalacji programu Azure PowerShell | Microsoft Docs
description: Informacje dotyczące instalacji programu Azure PowerShell za pomocą pakietu MSI lub Instalatora platformy sieci Web.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 3f8963c98b26f971c1259dc89d5da1f35ce3015a
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386701"
---
# <a name="other-installation-methods"></a><span data-ttu-id="f30f1-103">Inne metody instalacji</span><span class="sxs-lookup"><span data-stu-id="f30f1-103">Other installation methods</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="f30f1-104">Program Azure PowerShell można zainstalować na wiele sposobów.</span><span class="sxs-lookup"><span data-stu-id="f30f1-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="f30f1-105">Preferowaną metodą jest użycie modułu PowerShellGet z galerią programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f30f1-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="f30f1-106">Program Azure PowerShell można zainstalować w systemie Windows za pomocą Instalatora platformy internetowej (WebPI) lub pliku MSI dostępnego w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="f30f1-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="f30f1-107">Instalowanie w systemie Windows za pomocą Instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="f30f1-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="f30f1-108">Instalowanie najnowszej wersji programu Azure PowerShell przy użyciu pakietu WebPI odbywa się tak samo jak w przypadku wcześniejszych wersji.</span><span class="sxs-lookup"><span data-stu-id="f30f1-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="f30f1-109">Pobierz [pakiet WebPI programu Azure PowerShell](https://aka.ms/webpi-azps) i uruchom instalację.</span><span class="sxs-lookup"><span data-stu-id="f30f1-109">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="f30f1-110">Jeśli wcześniej zainstalowano moduły platformy Azure z Galerii programu PowerShell, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="f30f1-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="f30f1-111">Pozwala to uprościć środowisko, w którym jest zainstalowana tylko jedna wersja programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f30f1-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="f30f1-112">Występują jednak scenariusze, które wymagają zainstalowania wielu wersji.</span><span class="sxs-lookup"><span data-stu-id="f30f1-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="f30f1-113">Moduły z Galerii programu PowerShell są instalowane w folderze `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="f30f1-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="f30f1-114">Z kolei instalator pakietu WebPI instaluje moduły platformy Azure w folderze `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="f30f1-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="f30f1-115">Jeśli podczas instalacji wystąpi błąd, można ręcznie usunąć foldery Azure`$env:ProgramFiles\WindowsPowerShell\Modules` z folderu \*, a następnie ponowić próbę instalacji.</span><span class="sxs-lookup"><span data-stu-id="f30f1-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="f30f1-116">Po zakończeniu instalacji ustawienie `$env:PSModulePath` powinno obejmować katalogi zawierające polecenia cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f30f1-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f30f1-117">Poprawność instalacji programu Azure PowerShell można sprawdzić za pomocą następującego polecenia.</span><span class="sxs-lookup"><span data-stu-id="f30f1-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="f30f1-118">W przypadku instalacji przy użyciu pakietu WebPI może wystąpić znany problem.</span><span class="sxs-lookup"><span data-stu-id="f30f1-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="f30f1-119">Jeśli komputer wymaga ponownego uruchomienia ze względu na aktualizacje systemu lub inne instalacje, aktualizacje środowiska `$env:PSModulePath` mogą nie uwzględnić ścieżki, w której jest zainstalowany program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f30f1-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="f30f1-120">Podczas próby załadowania lub wykonania poleceń cmdlet po instalacji może pojawić się następujący komunikat o błędzie:</span><span class="sxs-lookup"><span data-stu-id="f30f1-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="f30f1-121">Problem ten można rozwiązać przez ponowne uruchomienie komputera lub zaimportowanie modułu przy użyciu w pełni kwalifikowanej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="f30f1-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="f30f1-122">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f30f1-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="f30f1-123">Instalowanie w systemie Windows za pomocą pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="f30f1-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="f30f1-124">Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="f30f1-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="f30f1-125">Jeśli są zainstalowane wcześniejsze wersje modułów platformy Azure, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="f30f1-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="f30f1-126">Pakiet MSI instaluje moduły w katalogu `$env:ProgramFiles\WindowsPowerShell\Modules`, ale nie tworzy folderów odpowiadających poszczególnym wersjom.</span><span class="sxs-lookup"><span data-stu-id="f30f1-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

