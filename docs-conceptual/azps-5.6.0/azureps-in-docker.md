---
title: Używanie Azure PowerShell w platformie Docker
description: Jak używać preinstalowanych Azure PowerShell w obrazie platformy Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101882088"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="25035-103">Używanie Azure PowerShell w platformie Docker</span><span class="sxs-lookup"><span data-stu-id="25035-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="25035-104">Publikujemy obrazy platformy Docker z preinstalowanym Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25035-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="25035-105">W tym artykule pokazano, jak rozpocząć korzystanie z Azure PowerShell w kontenerze platformy Docker.</span><span class="sxs-lookup"><span data-stu-id="25035-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="25035-106">Znajdowanie dostępnych obrazów</span><span class="sxs-lookup"><span data-stu-id="25035-106">Finding available images</span></span>

<span data-ttu-id="25035-107">Wydane obrazy wymagają platformy Docker 17,05 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="25035-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="25035-108">Oczekuje się również, że można uruchomić platformę Docker bez `sudo` lub lokalnych praw administracyjnych.</span><span class="sxs-lookup"><span data-stu-id="25035-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="25035-109">Zapoznaj się z oficjalnymi [instrukcjami][install] platformy Docker, aby poprawnie zainstalować program `docker` .</span><span class="sxs-lookup"><span data-stu-id="25035-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="25035-110">Najnowszy obraz kontenera zawiera najnowszą wersję programu PowerShell i najnowsze moduły Azure PowerShell obsługiwane przez AZ module.</span><span class="sxs-lookup"><span data-stu-id="25035-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="25035-111">Dla każdej nowej wersji AZ module zwalniamy obraz dla następujących systemów operacyjnych:</span><span class="sxs-lookup"><span data-stu-id="25035-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="25035-112">Ubuntu 18,04 (wartość domyślna)</span><span class="sxs-lookup"><span data-stu-id="25035-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="25035-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="25035-113">Debian 9</span></span>
- <span data-ttu-id="25035-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="25035-114">CentOs 7</span></span>

<span data-ttu-id="25035-115">Pełną listę dostępnych obrazów można znaleźć na naszej stronie [obrazu platformy Docker][az image] .</span><span class="sxs-lookup"><span data-stu-id="25035-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="25035-116">Używanie Azure PowerShell w kontenerze</span><span class="sxs-lookup"><span data-stu-id="25035-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="25035-117">Poniższe kroki pokazują polecenia platformy Docker wymagane do pobrania obrazu i uruchomienia interaktywnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25035-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="25035-118">Pobierz najnowszą wersję obrazu platformy Azure-PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25035-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="25035-119">Uruchom kontener Azure-PowerShell w trybie interaktywnym:</span><span class="sxs-lookup"><span data-stu-id="25035-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="25035-120">W przypadku hostów platformy Docker systemu Windows należy włączyć udostępnianie plików platformy Docker, aby zezwolić na współużytkowanie dysków lokalnych w systemie Windows z kontenerami systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="25035-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="25035-121">Aby uzyskać więcej informacji, zobacz [wprowadzenie do Docker for Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="25035-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="25035-122">Uruchamianie kontenera platformy Azure-PowerShell interaktywnie przy użyciu uwierzytelniania hosta</span><span class="sxs-lookup"><span data-stu-id="25035-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="25035-123">Jeśli masz już zainstalowaną Azure PowerShell w systemie Docker, być może masz buforowane poświadczenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="25035-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="25035-124">Tych poświadczeń można używać w sesji programu PowerShell działającej w kontenerze platformy Docker.</span><span class="sxs-lookup"><span data-stu-id="25035-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="25035-125">Domyślnie buforowane poświadczenia znajdują się w `$HOME/.Azure` katalogu na hoście.</span><span class="sxs-lookup"><span data-stu-id="25035-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="25035-126">Usługa Docker musi mieć dostęp do tej lokalizacji, aby uzyskać dostęp do poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="25035-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="25035-127">Następujące polecenie uruchamia kontener z zainstalowaną pamięcią podręczną poświadczeń i uruchamia interaktywną sesję programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25035-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="25035-128">Usuń obraz, gdy nie jest już konieczny</span><span class="sxs-lookup"><span data-stu-id="25035-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="25035-129">Następujące polecenie służy do usuwania kontenera platformy Docker, gdy nie jest już potrzebne.</span><span class="sxs-lookup"><span data-stu-id="25035-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="25035-130">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="25035-130">Next steps</span></span>

<span data-ttu-id="25035-131">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="25035-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
