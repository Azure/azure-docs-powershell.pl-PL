---
title: Uruchamianie programu Azure PowerShell w kontenerze platformy Docker
description: Dowiedz się, jak uruchomić program Azure PowerShell w kontenerze platformy Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425265"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="998d5-103">Uruchamianie programu Azure PowerShell w kontenerze platformy Docker</span><span class="sxs-lookup"><span data-stu-id="998d5-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="998d5-104">Firma Microsoft publikuje obrazy platformy Docker zawierające wstępnie zainstalowany program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="998d5-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="998d5-105">Obrazy te umożliwiają eksperymentowanie z programem Azure PowerShell lub uruchamianie go w środowisku izolowanym.</span><span class="sxs-lookup"><span data-stu-id="998d5-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="998d5-106">Nie ma obrazów zawierających zarówno program PowerShell Core, jak i program PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="998d5-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="998d5-107">Środowisko</span><span class="sxs-lookup"><span data-stu-id="998d5-107">Environment</span></span> | <span data-ttu-id="998d5-108">Obraz platformy Docker</span><span class="sxs-lookup"><span data-stu-id="998d5-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="998d5-109">Program PowerShell w systemie Windows</span><span class="sxs-lookup"><span data-stu-id="998d5-109">PowerShell on Windows</span></span> | [<span data-ttu-id="998d5-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="998d5-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="998d5-111">Program PowerShell Core w systemie Windows</span><span class="sxs-lookup"><span data-stu-id="998d5-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="998d5-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="998d5-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="998d5-113">Program PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="998d5-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="998d5-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="998d5-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="998d5-115">Aby uruchomić dowolne z tych kontenerów, użyj polecenia `docker run -it $ImageName` w celu otworzenia interakcyjnego terminalu.</span><span class="sxs-lookup"><span data-stu-id="998d5-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="998d5-116">Na przykład aby uruchomić kontener systemu Linux z programem PowerShell Core:</span><span class="sxs-lookup"><span data-stu-id="998d5-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="998d5-117">Aby uruchomić kontener systemu Windows na platformie Docker, host musi mieć system operacyjny Windows, a platforma Docker musi być skonfigurowana do uruchamiania kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="998d5-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="998d5-118">Aby dowiedzieć się więcej o przełączaniu między środowiskami Windows i Linux na platformie Docker, zobacz dokumentację platformy Docker: [Switch between Windows and Linux containers (Przełączanie między kontenerami systemu Windows i Linux)](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="998d5-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="998d5-119">Używanie kontenera programu PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="998d5-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="998d5-120">Kontenery programu PowerShell Core są udostępniane z preinstalowanym programem PowerShell Core w wersji 6 i modułem `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="998d5-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="998d5-121">Uruchom polecenie cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), a następnie zaloguj się przy użyciu konta platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="998d5-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="998d5-122">Używanie kontenera systemu Windows z programem PowerShell</span><span class="sxs-lookup"><span data-stu-id="998d5-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="998d5-123">Kontener systemu Windows ma preinstalowany moduł `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="998d5-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="998d5-124">Uruchom polecenie cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), a następnie zaloguj się przy użyciu konta platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="998d5-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
