---
title: Korzystanie z programu Azure PowerShell na platformie Docker
description: Jak używać programu Azure PowerShell wstępnie zainstalowanego w obrazie platformy Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012916"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="eb5ad-103">Korzystanie z programu Azure PowerShell na platformie Docker</span><span class="sxs-lookup"><span data-stu-id="eb5ad-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="eb5ad-104">Publikujemy obrazy platformy Docker z wstępnie zainstalowanym programem Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="eb5ad-105">W tym artykule pokazano, jak rozpocząć korzystanie z programu Azure PowerShell w kontenerze platformy Docker.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="eb5ad-106">Znajdowanie dostępnych obrazów</span><span class="sxs-lookup"><span data-stu-id="eb5ad-106">Finding available images</span></span>

<span data-ttu-id="eb5ad-107">Wydane obrazy wymagają platformy Docker 17.05 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="eb5ad-108">Oczekuje się również, że możesz uruchomić platformę Docker bez użycia polecenia `sudo` ani lokalnych uprawnień administracyjnych.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="eb5ad-109">Skorzystaj z oficjalnych [instrukcji][install], aby poprawnie zainstalować platformę `docker`.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="eb5ad-110">Najnowszy obraz kontenera zawiera najnowszą wersję programu PowerShell i najnowsze moduły Azure PowerShell obsługiwane przez moduł Az.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="eb5ad-111">Z każdą nową wersją modułu Az wydajemy obraz dla następujących systemów operacyjnych:</span><span class="sxs-lookup"><span data-stu-id="eb5ad-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="eb5ad-112">Ubuntu 18.04 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb5ad-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="eb5ad-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="eb5ad-113">Debian 9</span></span>
- <span data-ttu-id="eb5ad-114">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="eb5ad-114">CentOs 7</span></span>

<span data-ttu-id="eb5ad-115">Pełną listę dostępnych obrazów można znaleźć na naszej stronie [obrazów platformy Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="eb5ad-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="eb5ad-116">Korzystanie z programu Azure PowerShell w kontenerze</span><span class="sxs-lookup"><span data-stu-id="eb5ad-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="eb5ad-117">Poniższe kroki pokazują polecenia platformy Docker wymagane do pobrania obrazu i uruchomienia interaktywnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="eb5ad-118">Pobierz najnowszy obraz azure-powershell.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="eb5ad-119">Uruchom kontener azure-powershell w trybie interaktywnym:</span><span class="sxs-lookup"><span data-stu-id="eb5ad-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="eb5ad-120">W przypadku hostów platformy Docker z systemem Windows musisz włączyć udostępnianie plików platformy Docker, aby umożliwić udostępnienie lokalnych dysków systemu Windows dla kontenerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="eb5ad-121">Aby uzyskać więcej informacji, zobacz [Wprowadzenie do programu Docker for Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="eb5ad-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="eb5ad-122">Interaktywne uruchamianie kontenera azure-powershell przy użyciu uwierzytelniania hosta</span><span class="sxs-lookup"><span data-stu-id="eb5ad-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="eb5ad-123">Jeśli w systemie hostującym platformę Docker jest już zainstalowany program Azure PowerShell, być może masz buforowane poświadczenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="eb5ad-124">Tych poświadczeń można używać w sesji programu PowerShell działającej w kontenerze platformy Docker.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="eb5ad-125">Domyślnie buforowane poświadczenia znajdują się w katalogu `$HOME/.Azure` na hoście.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="eb5ad-126">Usługa Docker musi mieć dostęp do tej lokalizacji, aby uzyskać dostęp do poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="eb5ad-127">Następujące polecenie uruchamia kontener z zainstalowaną pamięcią podręczną poświadczeń i uruchamia interaktywną sesję programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="eb5ad-128">Usuwanie obrazu, gdy nie jest już konieczny</span><span class="sxs-lookup"><span data-stu-id="eb5ad-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="eb5ad-129">Następujące polecenie służy do usuwania kontenera platformy Docker, gdy nie jest już potrzebny.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="eb5ad-130">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="eb5ad-130">Next steps</span></span>

<span data-ttu-id="eb5ad-131">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="eb5ad-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
