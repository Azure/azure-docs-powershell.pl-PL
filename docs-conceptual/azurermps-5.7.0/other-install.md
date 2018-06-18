---
title: Inne metody instalacji programu Azure PowerShell
description: Informacje dotyczące instalacji programu Azure PowerShell za pomocą pakietu MSI lub Instalatora platformy sieci Web.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323275"
---
# <a name="other-installation-methods"></a><span data-ttu-id="b9fd4-103">Inne metody instalacji</span><span class="sxs-lookup"><span data-stu-id="b9fd4-103">Other installation methods</span></span>

<span data-ttu-id="b9fd4-104">W tym artykule opisano sposób instalowania programu Azure PowerShell przy użyciu pliku MSI lub Instalatora platformy internetowej (WebPI).</span><span class="sxs-lookup"><span data-stu-id="b9fd4-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="b9fd4-105">Program Azure PowerShell można również uruchamiać z poziomu kontenera Docker.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="b9fd4-106">Tych metod instalacji należy używać tylko wtedy, gdy są one niezbędne w danym systemie.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="b9fd4-107">Standardowym sposobem instalowania programu Azure PowerShell jest użycie modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="b9fd4-108">Aby uzyskać instrukcje dotyczące instalowania programu Azure PowerShell przy użyciu modułu PowerShellGet, zobacz [Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="b9fd4-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="b9fd4-109">Aby zainstalować w środowiskach Linux lub macOS, zobacz [Instalowanie programu Azure PowerShell w systemie macOS lub Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="b9fd4-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="b9fd4-110">Instalowanie lub aktualizowanie w systemie Windows za pomocą Instalatora platformy internetowej</span><span class="sxs-lookup"><span data-stu-id="b9fd4-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="b9fd4-111">Instalowanie najnowszej wersji programu Azure PowerShell przy użyciu pakietu WebPI odbywa się tak samo jak w przypadku wcześniejszych wersji.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="b9fd4-112">Pobierz [pakiet WebPI programu Azure PowerShell](http://aka.ms/webpi-azps) i uruchom instalację.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="b9fd4-113">Jeśli wcześniej zainstalowano moduły platformy Azure z Galerii programu PowerShell, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="b9fd4-114">Pozwala to uprościć środowisko, w którym jest zainstalowana tylko jedna wersja programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="b9fd4-115">Występują jednak scenariusze, które wymagają zainstalowania wielu wersji.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="b9fd4-116">Moduły z Galerii programu PowerShell są instalowane w folderze `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="b9fd4-117">Z kolei instalator pakietu WebPI instaluje moduły platformy Azure w folderze `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="b9fd4-118">Jeśli podczas instalacji wystąpi błąd, można ręcznie usunąć foldery `Azure*` z folderu `$env:ProgramFiles\WindowsPowerShell\Modules`, a następnie ponowić próbę instalacji.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="b9fd4-119">Po zakończeniu instalacji ustawienie `$env:PSModulePath` powinno obejmować katalogi zawierające polecenia cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b9fd4-120">Poprawność instalacji programu Azure PowerShell można sprawdzić za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="b9fd4-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="b9fd4-121">W przypadku instalacji przy użyciu pakietu WebPI może wystąpić znany problem.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="b9fd4-122">Jeśli komputer wymaga ponownego uruchomienia ze względu na aktualizacje systemu lub inne instalacje, aktualizacje środowiska `$env:PSModulePath` mogą nie uwzględnić ścieżki, w której jest zainstalowany program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="b9fd4-123">Podczas próby załadowania lub wykonania poleceń cmdlet po instalacji może pojawić się następujący komunikat o błędzie:</span><span class="sxs-lookup"><span data-stu-id="b9fd4-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="b9fd4-124">Problem ten można rozwiązać przez ponowne uruchomienie komputera lub zaimportowanie modułu przy użyciu w pełni kwalifikowanej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="b9fd4-125">Instalowanie lub aktualizowanie w systemie Windows za pomocą pakietu MSI</span><span class="sxs-lookup"><span data-stu-id="b9fd4-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="b9fd4-126">Program Azure PowerShell można zainstalować za pomocą pliku MSI dostępnego w witrynie [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="b9fd4-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="b9fd4-127">Jeśli są zainstalowane wcześniejsze wersje modułów platformy Azure, instalator automatycznie je usuwa.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="b9fd4-128">Pakiet MSI instaluje moduły w katalogu `$env:ProgramFiles\WindowsPowerShell\Modules`, ale nie tworzy folderów odpowiadających poszczególnym wersjom.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="b9fd4-129">Uruchamianie w kontenerze Docker</span><span class="sxs-lookup"><span data-stu-id="b9fd4-129">Run in a Docker container</span></span>

<span data-ttu-id="b9fd4-130">Utrzymujemy zestaw obrazów Docker wstępnie skonfigurowanych z programem Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="b9fd4-131">Dostępne są dwa typy kontenerów: kontenery z tradycyjnym programem PowerShell działającym w systemie Windows i kontenery z programem PowerShell Core działającym w systemie Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="b9fd4-132">Środowisko</span><span class="sxs-lookup"><span data-stu-id="b9fd4-132">Environment</span></span> | <span data-ttu-id="b9fd4-133">Obraz platformy Docker</span><span class="sxs-lookup"><span data-stu-id="b9fd4-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="b9fd4-134">Program PowerShell w systemie Windows</span><span class="sxs-lookup"><span data-stu-id="b9fd4-134">PowerShell on Windows</span></span> | [<span data-ttu-id="b9fd4-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="b9fd4-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="b9fd4-136">Program PowerShell Core w systemie Windows</span><span class="sxs-lookup"><span data-stu-id="b9fd4-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="b9fd4-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="b9fd4-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="b9fd4-138">Program PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="b9fd4-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="b9fd4-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="b9fd4-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="b9fd4-140">Aby uruchomić dowolne z tych kontenerów, należy użyć polecenia `docker run -it $ImageName` w celu otworzenia interakcyjnego terminalu.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="b9fd4-141">Aby na przykład uruchomić kontener z programem PowerShell Core w systemie Linux, użyj polecenia:</span><span class="sxs-lookup"><span data-stu-id="b9fd4-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="b9fd4-142">Aby uruchomić kontener systemu Windows na platformie Docker, host musi mieć system operacyjny Windows, a platforma Docker musi być skonfigurowana do uruchamiania kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="b9fd4-143">Aby dowiedzieć się więcej o przełączaniu między środowiskami Windows i Linux na platformie Docker, zobacz dokumentację platformy Docker: [Switch between Windows and Linux containers (Przełączanie między kontenerami systemu Windows i Linux)](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="b9fd4-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>