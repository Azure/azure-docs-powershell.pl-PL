---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973178"
---
# <span data-ttu-id="87502-101">Moduł Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="87502-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="87502-102">Opis</span><span class="sxs-lookup"><span data-stu-id="87502-102">Description</span></span>
<span data-ttu-id="87502-103">Polecenia cmdlet w module synchronizacji przestrzeni dyskowej umożliwiają zarządzanie operacjami odnoszącym się do synchronizacji plików platformy Azure w programie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="87502-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="87502-104">Az.StorageSync Cmdlet</span><span class="sxs-lookup"><span data-stu-id="87502-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="87502-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="87502-106">To polecenie wyświetla listę wszystkich punktów końcowych chmury w obrębie danej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="87502-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="87502-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="87502-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="87502-108">To polecenie zawiera listę wszystkich grup synchronizacji w ramach danej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="87502-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="87502-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="87502-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="87502-110">To polecenie zawiera listę wszystkich serwerów zarejestrowanych w danej usłudze synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="87502-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="87502-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="87502-112">To polecenie wyświetla listę wszystkich punktów końcowych serwera w obrębie danej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="87502-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="87502-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="87502-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="87502-114">To polecenie zawiera listę wszystkich usług synchronizacji przestrzeni dyskowej w obrębie danego zakresu grupy subskrypcji/zasobów.</span><span class="sxs-lookup"><span data-stu-id="87502-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="87502-115">Invoke-AzstorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="87502-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="87502-116">Za pomocą tego polecenia można ręcznie zainicjować wykrywanie zmian przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="87502-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="87502-117">Może być kierowana do całego udziału, podfolderu lub zestawu plików.</span><span class="sxs-lookup"><span data-stu-id="87502-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="87502-118">Wykrywanych może być maksymalnie 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="87502-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="87502-119">Jeśli zakres zmian jest dla Ciebie znany, ogranicz wykonywanie tego polecenia do części przestrzeni nazw, aby wykrywanie zmian można szybko zakończyć i z ograniczeniem do 10 000 zmian.</span><span class="sxs-lookup"><span data-stu-id="87502-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="87502-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="87502-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="87502-121">Sprawdza potencjalne problemy ze zgodnością między systemem a usługą Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="87502-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="87502-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="87502-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="87502-123">To polecenie przypomina wszystkie pliki warstwowe z powrotem na dysk lokalny.</span><span class="sxs-lookup"><span data-stu-id="87502-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="87502-124">New-azstorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="87502-125">To polecenie tworzy punkt końcowy chmury synchronizacji plików platformy Azure w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="87502-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="87502-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="87502-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="87502-127">To polecenie tworzy nową grupę synchronizacji w ramach określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="87502-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="87502-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="87502-129">To polecenie tworzy nowy punkt końcowy serwera na zarejestrowanym serwerze.</span><span class="sxs-lookup"><span data-stu-id="87502-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="87502-130">Dzięki temu określona ścieżka na serwerze może rozpocząć synchronizację plików z innymi punktami końcowymi w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="87502-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="87502-131">New-AzstorageSyncService</span><span class="sxs-lookup"><span data-stu-id="87502-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="87502-132">To polecenie tworzy nową usługę synchronizacji przestrzeni dyskowej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="87502-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="87502-133">Set-AzstorageSyncService</span><span class="sxs-lookup"><span data-stu-id="87502-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="87502-134">To polecenie ustawia usługę synchronizacji magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="87502-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="87502-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="87502-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="87502-136">To polecenie rejestruje serwer w usłudze synchronizacji magazynu, co tworzy relację zaufania.</span><span class="sxs-lookup"><span data-stu-id="87502-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="87502-137">Następnie można użyć programu PowerShell lub portalu Azure w celu skonfigurowania synchronizacji na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="87502-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="87502-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="87502-139">To polecenie spowoduje usunięcie określonego punktu końcowego chmury z grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="87502-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="87502-140">Bez co najmniej jednego punktu końcowego chmury żadne inne punkty końcowe serwera w tej grupie synchronizacji nie mogą być synchronizowane.</span><span class="sxs-lookup"><span data-stu-id="87502-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="87502-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="87502-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="87502-142">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="87502-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="87502-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="87502-144">To polecenie spowoduje usunięcie określonego punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="87502-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="87502-145">Synchronizacja z tą lokalizacją zostanie zatrzymana natychmiast.</span><span class="sxs-lookup"><span data-stu-id="87502-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="87502-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="87502-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="87502-147">To polecenie spowoduje usunięcie określonej usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="87502-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="87502-148">Reset-AzstorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="87502-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="87502-149">Używaj tylko do rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="87502-149">Use for troubleshooting only.</span></span> <span data-ttu-id="87502-150">To polecenie spowoduje roll the storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="87502-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="87502-151">Set-AzstorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87502-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="87502-152">To polecenie umożliwia zmiany parametrów dostosowywanych punktu końcowego serwera.</span><span class="sxs-lookup"><span data-stu-id="87502-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="87502-153">Unregister-azstorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="87502-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="87502-154">Ostrzeżenie: Wyrejestrowanie serwera spowoduje usuwanie kaskadowe wszystkich punktów końcowych serwera na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="87502-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="87502-155">To polecenie spowoduje wyrejestrowanie serwera z usługi synchronizacji przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="87502-155">This command will unregister a server from it's storage sync service.</span></span>

