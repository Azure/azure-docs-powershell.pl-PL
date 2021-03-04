---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: c73e82285a848c9ff6abf197eb3352cf708a2f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958753"
---
# <span data-ttu-id="11407-101">Moduł Az.DataMigration</span><span class="sxs-lookup"><span data-stu-id="11407-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="11407-102">Opis</span><span class="sxs-lookup"><span data-stu-id="11407-102">Description</span></span>
<span data-ttu-id="11407-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="11407-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="11407-104">Az.DataMigration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11407-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="11407-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="11407-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="11407-106">Pobiera właściwości projektu migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="11407-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="11407-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="11407-108">Pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="11407-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="11407-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="11407-110">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="11407-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="11407-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="11407-112">Tworzy nowe polecenie do wykonania dla istniejącego zadania DMS.</span><span class="sxs-lookup"><span data-stu-id="11407-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="11407-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="11407-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="11407-114">Tworzy nowy obiekt Informacje o połączeniu określający typ serwera i nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="11407-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="11407-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="11407-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="11407-116">Tworzy obiekt DatabaseInfo dla usługi Azure Database Migration Service, określającą źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="11407-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="11407-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="11407-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="11407-118">Tworzy obiekt FileShare dla usługi Azure Database Migration Service, określającą lokalny udział sieciowy do wykonywania kopii zapasowych źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="11407-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="11407-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="11407-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="11407-120">Tworzy nowy projekt usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="11407-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="11407-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="11407-122">Tworzy obiekt wejściowy bazy danych zawierający informacje o źródłowych i docelowych bazach danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="11407-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="11407-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="11407-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="11407-124">Tworzy nowe wystąpienie usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="11407-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="11407-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="11407-126">Tworzy obiekt informacyjny bazy danych specyficzny dla scenariusza synchronizacji, który ma być używany do zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="11407-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="11407-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="11407-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="11407-128">Tworzy i uruchamia zadanie migracji danych w usłudze migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="11407-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="11407-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="11407-130">Usuwa projekt usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="11407-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="11407-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="11407-132">Usuwa wystąpienie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="11407-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="11407-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="11407-134">Usuwa zadanie usługi migracji bazy danych Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11407-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="11407-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="11407-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="11407-136">Uruchamia wystąpienie usługi migracji bazy danych Azure w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="11407-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="11407-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="11407-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="11407-138">Zatrzymuje wystąpienie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="11407-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="11407-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="11407-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="11407-140">Zatrzymuje zadanie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="11407-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

