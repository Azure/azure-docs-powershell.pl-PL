---
title: Inne metody instalacji programu Azure PowerShell | Microsoft Docs
description: Informacje dotyczące instalacji programu Azure PowerShell za pomocą pakietu MSI lub Instalatora platformy sieci Web.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 73c099375cecc8abdd5d6179109513946e7e793b
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="other-installation-methods"></a><span data-ttu-id="bf756-103">Inne metody instalacji</span><span class="sxs-lookup"><span data-stu-id="bf756-103">Other installation methods</span></span>

<span data-ttu-id="bf756-104">Program Azure PowerShell można zainstalować na wiele sposobów.</span><span class="sxs-lookup"><span data-stu-id="bf756-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="bf756-105">Preferowaną metodą jest użycie modułu PowerShellGet z galerią programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf756-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="bf756-106">Program Azure PowerShell można zainstalować w systemie Windows za pomocą Instalatora platformy internetowej (WebPI) lub pliku MSI dostępnego w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="bf756-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="bf756-107">Program Azure PowerShell można również zainstalować w kontenerze Docker.</span><span class="sxs-lookup"><span data-stu-id="bf756-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="bf756-108">Instalowanie w systemie Windows za pomocą Instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="bf756-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="bf756-109">Instalowanie najnowszej wersji programu Azure PowerShell przy użyciu pakietu WebPI odbywa się tak samo jak w przypadku wcześniejszych wersji.</span><span class="sxs-lookup"><span data-stu-id="bf756-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="bf756-110">Pobierz [pakiet WebPI programu Azure PowerShell](http://aka.ms/webpi-azps) i uruchom instalację.</span><span class="sxs-lookup"><span data-stu-id="bf756-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="bf756-111">Jeśli wcześniej zainstalowano moduły platformy Azure z Galerii programu PowerShell, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="bf756-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="bf756-112">Pozwala to uprościć środowisko, w którym jest zainstalowana tylko jedna wersja programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf756-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="bf756-113">Występują jednak scenariusze, które wymagają zainstalowania wielu wersji.</span><span class="sxs-lookup"><span data-stu-id="bf756-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="bf756-114">Moduły z Galerii programu PowerShell są instalowane w folderze `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="bf756-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="bf756-115">Z kolei instalator pakietu WebPI instaluje moduły platformy Azure w folderze `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="bf756-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="bf756-116">Jeśli podczas instalacji wystąpi błąd, można ręcznie usunąć foldery Azure\* z folderu `$env:ProgramFiles\WindowsPowerShell\Modules`, a następnie ponowić próbę instalacji.</span><span class="sxs-lookup"><span data-stu-id="bf756-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="bf756-117">Po zakończeniu instalacji ustawienie `$env:PSModulePath` powinno obejmować katalogi zawierające polecenia cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf756-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="bf756-118">Poprawność instalacji programu Azure PowerShell można sprawdzić za pomocą następującego polecenia.</span><span class="sxs-lookup"><span data-stu-id="bf756-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="bf756-119">W przypadku instalacji przy użyciu pakietu WebPI może wystąpić znany problem.</span><span class="sxs-lookup"><span data-stu-id="bf756-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="bf756-120">Jeśli komputer wymaga ponownego uruchomienia ze względu na aktualizacje systemu lub inne instalacje, aktualizacje środowiska `$env:PSModulePath` mogą nie uwzględnić ścieżki, w której jest zainstalowany program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf756-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="bf756-121">Podczas próby załadowania lub wykonania poleceń cmdlet po instalacji może pojawić się następujący komunikat o błędzie:</span><span class="sxs-lookup"><span data-stu-id="bf756-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
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

<span data-ttu-id="bf756-122">Problem ten można rozwiązać przez ponowne uruchomienie komputera lub zaimportowanie modułu przy użyciu w pełni kwalifikowanej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="bf756-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="bf756-123">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="bf756-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="bf756-124">Instalowanie w systemie Windows za pomocą pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="bf756-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="bf756-125">Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="bf756-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="bf756-126">Jeśli są zainstalowane wcześniejsze wersje modułów platformy Azure, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="bf756-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="bf756-127">Pakiet MSI instaluje moduły w katalogu `$env:ProgramFiles\WindowsPowerShell\Modules`, ale nie tworzy folderów odpowiadających poszczególnym wersjom.</span><span class="sxs-lookup"><span data-stu-id="bf756-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="bf756-128">Instalowanie w kontenerze Docker</span><span class="sxs-lookup"><span data-stu-id="bf756-128">Install in a Docker container</span></span>

<span data-ttu-id="bf756-129">Utrzymujemy obraz Docker wstępnie skonfigurowany z programem Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf756-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="bf756-130">Uruchom kontener za pomocą polecenia `docker run`.</span><span class="sxs-lookup"><span data-stu-id="bf756-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="bf756-131">Ponadto utrzymujemy podzestaw poleceń cmdlet jako kontener programu PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="bf756-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="bf756-132">Dla systemu Mac/Linux użyj obrazu `latest`.</span><span class="sxs-lookup"><span data-stu-id="bf756-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="bf756-133">Dla systemu Windows użyj obrazu `nanoserver`.</span><span class="sxs-lookup"><span data-stu-id="bf756-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="bf756-134">Program Azure PowerShell jest instalowany w obrazie za pośrednictwem polecenia `Install-Module` z [galerii programu PowerShell](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="bf756-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>