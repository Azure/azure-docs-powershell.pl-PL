---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93704332"
---
# <span data-ttu-id="15a51-101">AZ. StorageSync, moduł</span><span class="sxs-lookup"><span data-stu-id="15a51-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="15a51-102">Opis</span><span class="sxs-lookup"><span data-stu-id="15a51-102">Description</span></span>
<span data-ttu-id="15a51-103">Polecenia cmdlet w module synchronizacji magazynu umożliwiają zarządzanie operacjami związanymi z synchronizacją plików Azure w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15a51-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="15a51-104">AZ. StorageSync polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="15a51-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="15a51-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="15a51-106">To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15a51-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="15a51-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="15a51-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="15a51-108">To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="15a51-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="15a51-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="15a51-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="15a51-110">To polecenie wyświetla listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="15a51-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="15a51-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="15a51-112">To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15a51-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="15a51-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="15a51-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="15a51-114">To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="15a51-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="15a51-115">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="15a51-115">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="15a51-116">Sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="15a51-116">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="15a51-117">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="15a51-117">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="15a51-118">To polecenie ponownie wywołuje wszystkie pliki warstw z powrotem na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="15a51-118">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="15a51-119">Nowe — AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-119">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="15a51-120">To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15a51-120">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="15a51-121">Nowe — AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="15a51-121">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="15a51-122">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="15a51-122">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="15a51-123">Nowe — AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-123">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="15a51-124">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="15a51-124">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="15a51-125">Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="15a51-125">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="15a51-126">Nowe — AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="15a51-126">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="15a51-127">To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="15a51-127">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="15a51-128">Rejestr — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="15a51-128">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="15a51-129">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, która tworzy relację zaufania.</span><span class="sxs-lookup"><span data-stu-id="15a51-129">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="15a51-130">Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="15a51-130">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="15a51-131">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-131">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="15a51-132">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15a51-132">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="15a51-133">Bez co najmniej jednego punktu końcowego w chmurze nie można zsynchronizować innych punktów końcowych serwera w tej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15a51-133">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="15a51-134">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="15a51-134">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="15a51-135">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="15a51-135">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="15a51-136">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-136">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="15a51-137">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="15a51-137">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="15a51-138">Synchronizacja z tą lokalizacją zostanie natychmiast zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="15a51-138">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="15a51-139">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="15a51-139">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="15a51-140">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="15a51-140">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="15a51-141">Resetowanie — AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="15a51-141">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="15a51-142">Służy tylko do rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="15a51-142">Use for troubleshooting only.</span></span> <span data-ttu-id="15a51-143">To polecenie spowoduje wywrócenie certyfikatu serwera synchronizacji magazynu użytego do opisania tożsamości serwera w usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="15a51-143">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="15a51-144">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a51-144">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="15a51-145">To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.</span><span class="sxs-lookup"><span data-stu-id="15a51-145">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="15a51-146">Wyrejestrowanie — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="15a51-146">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="15a51-147">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="15a51-147">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="15a51-148">To polecenie spowoduje Wyrejestrowanie serwera z usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="15a51-148">This command will unregister a server from it's storage sync service.</span></span>