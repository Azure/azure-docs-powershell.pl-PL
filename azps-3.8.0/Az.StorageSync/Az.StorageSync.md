---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051417"
---
# <span data-ttu-id="9b1d0-101">AZ. StorageSync, moduł</span><span class="sxs-lookup"><span data-stu-id="9b1d0-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="9b1d0-102">Opis</span><span class="sxs-lookup"><span data-stu-id="9b1d0-102">Description</span></span>
<span data-ttu-id="9b1d0-103">Polecenia cmdlet w module synchronizacji magazynu umożliwiają zarządzanie operacjami związanymi z synchronizacją plików Azure w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="9b1d0-104">AZ. StorageSync polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b1d0-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="9b1d0-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="9b1d0-106">To polecenie umożliwia wyświetlenie wszystkich chmurowych punktów końcowych w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="9b1d0-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9b1d0-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="9b1d0-108">To polecenie wyświetla listę wszystkich grup synchronizacji w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="9b1d0-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9b1d0-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="9b1d0-110">To polecenie wyświetla listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="9b1d0-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9b1d0-112">To polecenie wyświetla listę wszystkich punktów końcowych serwera w danej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="9b1d0-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9b1d0-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="9b1d0-114">To polecenie wyświetla listę wszystkich usług synchronizacji magazynu w danym zakresie grupy abonament/Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="9b1d0-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="9b1d0-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="9b1d0-116">Za pomocą tego polecenia można ręcznie inicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="9b1d0-117">Można go kierować do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="9b1d0-118">Można wykryć maksymalnie 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="9b1d0-119">Jeśli zakres zmian jest dla Ciebie znany, Ogranicz wykonanie tego polecenia do części obszaru nazw, dzięki czemu funkcja wykrywania zmian może zakończyć się szybko i w granicach 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="9b1d0-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="9b1d0-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="9b1d0-121">Sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="9b1d0-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="9b1d0-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="9b1d0-123">To polecenie ponownie wywołuje wszystkie pliki warstw z powrotem na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="9b1d0-124">Nowe — AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="9b1d0-125">To polecenie umożliwia utworzenie punktu końcowego chmurowej synchronizacji plików platformy Azure w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="9b1d0-126">Nowe — AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9b1d0-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="9b1d0-127">To polecenie tworzy nową grupę synchronizacji w określonej usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="9b1d0-128">Nowe — AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9b1d0-129">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="9b1d0-130">Spowoduje to włączenie określonej ścieżki na serwerze w celu zsynchronizowania plików z innymi punktami końcowymi w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="9b1d0-131">Nowe — AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9b1d0-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="9b1d0-132">To polecenie tworzy nową usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="9b1d0-133">Rejestr — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9b1d0-133">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="9b1d0-134">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, która tworzy relację zaufania.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-134">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="9b1d0-135">Za pomocą programu PowerShell lub portalu Azure można skonfigurować synchronizację na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-135">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="9b1d0-136">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-136">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="9b1d0-137">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-137">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="9b1d0-138">Bez co najmniej jednego punktu końcowego w chmurze nie można zsynchronizować innych punktów końcowych serwera w tej grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-138">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="9b1d0-139">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9b1d0-139">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="9b1d0-140">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-140">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="9b1d0-141">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-141">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9b1d0-142">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-142">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="9b1d0-143">Synchronizacja z tą lokalizacją zostanie natychmiast zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-143">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="9b1d0-144">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9b1d0-144">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="9b1d0-145">To polecenie spowoduje usunięcie określonej usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-145">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="9b1d0-146">Resetowanie — AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="9b1d0-146">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="9b1d0-147">Służy tylko do rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-147">Use for troubleshooting only.</span></span> <span data-ttu-id="9b1d0-148">To polecenie spowoduje wywrócenie certyfikatu serwera synchronizacji magazynu użytego do opisania tożsamości serwera w usłudze synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-148">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="9b1d0-149">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b1d0-149">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9b1d0-150">To polecenie umożliwia wprowadzanie zmian w parametrach regulowanych w punkcie końcowym serwera.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-150">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="9b1d0-151">Wyrejestrowanie — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9b1d0-151">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="9b1d0-152">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usunięcie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-152">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="9b1d0-153">To polecenie spowoduje Wyrejestrowanie serwera z usługi synchronizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-153">This command will unregister a server from it's storage sync service.</span></span>

