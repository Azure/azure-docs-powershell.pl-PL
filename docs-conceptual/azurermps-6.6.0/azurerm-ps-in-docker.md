---
title: Uruchamianie programu Azure PowerShell w kontenerze platformy Docker
description: Dowiedz się, jak uruchomić program Azure PowerShell w kontenerze platformy Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/02/2018
ms.locfileid: "39367909"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="a4bae-103">Uruchamianie programu Azure PowerShell w kontenerze platformy Docker</span><span class="sxs-lookup"><span data-stu-id="a4bae-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="a4bae-104">Jest dostępny zestaw obrazów platformy Docker wstępnie skonfigurowanych z programem Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4bae-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="a4bae-105">Dostępne są dwa typy kontenerów: kontenery z tradycyjnym programem PowerShell działającym w systemie Windows i kontenery z programem PowerShell Core działającym w systemie Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="a4bae-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="a4bae-106">Środowisko</span><span class="sxs-lookup"><span data-stu-id="a4bae-106">Environment</span></span> | <span data-ttu-id="a4bae-107">Obraz platformy Docker</span><span class="sxs-lookup"><span data-stu-id="a4bae-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="a4bae-108">Program PowerShell w systemie Windows</span><span class="sxs-lookup"><span data-stu-id="a4bae-108">PowerShell on Windows</span></span> | [<span data-ttu-id="a4bae-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="a4bae-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="a4bae-110">Program PowerShell Core w systemie Windows</span><span class="sxs-lookup"><span data-stu-id="a4bae-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="a4bae-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="a4bae-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="a4bae-112">Program PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="a4bae-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="a4bae-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="a4bae-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="a4bae-114">Aby uruchomić dowolne z tych kontenerów, należy użyć polecenia `docker run -it $ImageName` w celu otworzenia interakcyjnego terminalu.</span><span class="sxs-lookup"><span data-stu-id="a4bae-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="a4bae-115">Aby na przykład uruchomić kontener z programem PowerShell Core w systemie Linux, użyj polecenia:</span><span class="sxs-lookup"><span data-stu-id="a4bae-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="a4bae-116">Aby uruchomić kontener systemu Windows na platformie Docker, host musi mieć system operacyjny Windows, a platforma Docker musi być skonfigurowana do uruchamiania kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="a4bae-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="a4bae-117">Aby dowiedzieć się więcej o przełączaniu między środowiskami Windows i Linux na platformie Docker, zobacz dokumentację platformy Docker: [Switch between Windows and Linux containers (Przełączanie między kontenerami systemu Windows i Linux)](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="a4bae-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="a4bae-118">Używanie kontenera programu PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="a4bae-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="a4bae-119">Kontenery programu PowerShell Core są udostępniane z preinstalowanym programem PowerShell Core w wersji 6 i modułem `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="a4bae-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="a4bae-120">Uruchom polecenie cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), a następnie zaloguj się przy użyciu konta platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="a4bae-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="a4bae-121">Używanie kontenera systemu Windows z programem PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4bae-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="a4bae-122">Kontener systemu Windows ma preinstalowany moduł `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="a4bae-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="a4bae-123">Uruchom polecenie cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), a następnie zaloguj się przy użyciu konta platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="a4bae-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```