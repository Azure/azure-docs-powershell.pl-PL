---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221265"
---
# <span data-ttu-id="e7ddd-101">AZ. Moduł migracji datamigration</span><span class="sxs-lookup"><span data-stu-id="e7ddd-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="e7ddd-102">Opis</span><span class="sxs-lookup"><span data-stu-id="e7ddd-102">Description</span></span>
<span data-ttu-id="e7ddd-103">{{Moduł usługi Azure datamigration Service}}</span><span class="sxs-lookup"><span data-stu-id="e7ddd-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="e7ddd-104">AZ. polecenia cmdlet migracji datamigration</span><span class="sxs-lookup"><span data-stu-id="e7ddd-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="e7ddd-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e7ddd-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="e7ddd-106">Pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="e7ddd-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7ddd-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="e7ddd-108">Pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="e7ddd-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e7ddd-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="e7ddd-110">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="e7ddd-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="e7ddd-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="e7ddd-112">Tworzy nowe polecenie do wykonania na istniejącym zadaniu DMS.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="e7ddd-113">Nowe — AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e7ddd-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="e7ddd-114">Tworzy nowy obiekt informacji o połączeniu określający typ serwera i nazwę dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="e7ddd-115">Nowe — AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="e7ddd-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="e7ddd-116">Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych platformy Azure, która określa źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="e7ddd-117">Nowe — AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="e7ddd-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="e7ddd-118">Tworzy obiekt udostępnionego udziału w usłudze migracji bazy danych platformy Azure, który określa lokalny udział sieciowy do wykonania kopii zapasowych źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="e7ddd-119">Nowe — AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e7ddd-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="e7ddd-120">Tworzy nowy projekt usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="e7ddd-121">Nowe — AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e7ddd-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="e7ddd-122">Tworzy obiekt wejściowy bazy danych, który zawiera informacje dotyczące źródłowej i docelowej bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="e7ddd-123">Nowe — AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7ddd-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="e7ddd-124">Tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="e7ddd-125">Nowe — AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e7ddd-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="e7ddd-126">Umożliwia utworzenie obiektu informacyjnego bazy danych określonego dla scenariusza synchronizacji, który ma być wykorzystywany do wykonania zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="e7ddd-127">Nowe — AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e7ddd-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="e7ddd-128">Tworzy i rozpoczyna zadanie migracji danych w usłudze migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="e7ddd-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e7ddd-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="e7ddd-130">Usuwa projekt usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="e7ddd-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7ddd-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="e7ddd-132">Usuwa wystąpienie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="e7ddd-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e7ddd-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="e7ddd-134">Usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="e7ddd-135">Start — AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7ddd-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="e7ddd-136">Powoduje uruchomienie wystąpienia usługi migracji bazy danych platformy Azure w stanie zatrzymanym.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="e7ddd-137">Zatrzymaj — AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e7ddd-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="e7ddd-138">Zatrzymuje wystąpienie usługi migracji bazy danych platformy Azure, która jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="e7ddd-139">Zatrzymaj — AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e7ddd-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="e7ddd-140">Zatrzymuje zadanie usługi migracji bazy danych platformy Azure, które jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e7ddd-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

