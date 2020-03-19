---
title: Korzystanie z programu Azure PowerShell na platformie Docker
description: Jak używać programu Azure PowerShell wstępnie zainstalowanego w obrazie platformy Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402684"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="6649d-103">Korzystanie z programu Azure PowerShell na platformie Docker</span><span class="sxs-lookup"><span data-stu-id="6649d-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="6649d-104">Publikujemy obrazy platformy Docker z wstępnie zainstalowanym programem Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6649d-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="6649d-105">W tym artykule pokazano, jak rozpocząć korzystanie z programu Azure PowerShell w kontenerze platformy Docker.</span><span class="sxs-lookup"><span data-stu-id="6649d-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="6649d-106">Znajdowanie dostępnych obrazów</span><span class="sxs-lookup"><span data-stu-id="6649d-106">Finding available images</span></span>

<span data-ttu-id="6649d-107">Wydane obrazy wymagają platformy Docker 17.05 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="6649d-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="6649d-108">Oczekuje się również, że możesz uruchomić platformę Docker bez użycia polecenia `sudo` ani lokalnych uprawnień administracyjnych.</span><span class="sxs-lookup"><span data-stu-id="6649d-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="6649d-109">Skorzystaj z oficjalnych [instrukcji][install], aby poprawnie zainstalować platformę `docker`.</span><span class="sxs-lookup"><span data-stu-id="6649d-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="6649d-110">Wydane kontenery zostały utworzone na podstawie oficjalnych kontenerów programu PowerShell, a następnie dodano do nich moduł Az jako warstwę.</span><span class="sxs-lookup"><span data-stu-id="6649d-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="6649d-111">Najnowszy stabilny obraz obejmuje następujące składniki:</span><span class="sxs-lookup"><span data-stu-id="6649d-111">The latest stable image includes:</span></span>

- <span data-ttu-id="6649d-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="6649d-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="6649d-113">PowerShell 6.2.4</span><span class="sxs-lookup"><span data-stu-id="6649d-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="6649d-114">Najnowszy moduł Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6649d-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="6649d-115">Pełną listę dostępnych obrazów można znaleźć na naszej stronie [obrazów platformy Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="6649d-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="6649d-116">Korzystanie z programu Azure PowerShell w kontenerze</span><span class="sxs-lookup"><span data-stu-id="6649d-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="6649d-117">Poniższe kroki pokazują polecenia platformy Docker wymagane do pobrania obrazu i uruchomienia interaktywnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6649d-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="6649d-118">Pobierz najnowszy obraz azure-powershell.</span><span class="sxs-lookup"><span data-stu-id="6649d-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="6649d-119">Uruchom kontener azure-powershell w trybie interaktywnym:</span><span class="sxs-lookup"><span data-stu-id="6649d-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="6649d-120">Interaktywne uruchamianie kontenera azure-powershell przy użyciu uwierzytelniania hosta</span><span class="sxs-lookup"><span data-stu-id="6649d-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="6649d-121">Jeśli w systemie hostującym platformę Docker jest już zainstalowany program Azure PowerShell, być może masz buforowane poświadczenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6649d-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="6649d-122">Tych poświadczeń można używać w sesji programu PowerShell działającej w kontenerze platformy Docker.</span><span class="sxs-lookup"><span data-stu-id="6649d-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="6649d-123">Domyślnie buforowane poświadczenia znajdują się w katalogu `$HOME/.Azure` na hoście.</span><span class="sxs-lookup"><span data-stu-id="6649d-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="6649d-124">Usługa Docker musi mieć dostęp do tej lokalizacji, aby uzyskać dostęp do poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="6649d-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="6649d-125">Następujące polecenie uruchamia kontener z zainstalowaną pamięcią podręczną poświadczeń i uruchamia interaktywną sesję programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6649d-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="6649d-126">Usuwanie obrazu, gdy nie jest już konieczny</span><span class="sxs-lookup"><span data-stu-id="6649d-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="6649d-127">Następujące polecenie służy do usuwania kontenera platformy Docker, gdy nie jest już potrzebny.</span><span class="sxs-lookup"><span data-stu-id="6649d-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="6649d-128">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="6649d-128">Next steps</span></span>

<span data-ttu-id="6649d-129">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6649d-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell