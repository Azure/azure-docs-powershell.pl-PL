---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: ed697798694063c516621d25fb43e153b7a23dbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503347"
---
# <span data-ttu-id="070d8-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="070d8-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="070d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="070d8-102">SYNOPSIS</span></span>
<span data-ttu-id="070d8-103">Umożliwia zaktualizowanie połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-103">Updates a data connection.</span></span>

## <span data-ttu-id="070d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="070d8-104">SYNTAX</span></span>

### <span data-ttu-id="070d8-105">UpdateExpandedEventHub (domyślny)</span><span class="sxs-lookup"><span data-stu-id="070d8-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="070d8-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="070d8-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="070d8-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="070d8-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="070d8-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="070d8-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="070d8-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="070d8-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="070d8-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="070d8-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="070d8-111">Opis</span><span class="sxs-lookup"><span data-stu-id="070d8-111">DESCRIPTION</span></span>
<span data-ttu-id="070d8-112">Umożliwia zaktualizowanie połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-112">Updates a data connection.</span></span>

## <span data-ttu-id="070d8-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="070d8-113">EXAMPLES</span></span>

### <span data-ttu-id="070d8-114">Przykład 1: Aktualizowanie istniejącego połączenia danych EventHub</span><span class="sxs-lookup"><span data-stu-id="070d8-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="070d8-115">Powyższe polecenie aktualizuje istniejące połączenie danych EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="070d8-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="070d8-116">Przykład 2: Aktualizowanie istniejącego połączenia danych programu EventGrid</span><span class="sxs-lookup"><span data-stu-id="070d8-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="070d8-117">Powyższe polecenie aktualizuje istniejące połączenie danych programu EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="070d8-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="070d8-118">Przykład 3: Aktualizowanie istniejącego połączenia danych programu IotHub</span><span class="sxs-lookup"><span data-stu-id="070d8-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="070d8-119">Powyższe polecenie aktualizuje istniejące połączenie danych programu IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="070d8-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="070d8-120">Przykład 4: Aktualizowanie istniejącego połączenia danych EventHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="070d8-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="070d8-121">Powyższe polecenie aktualizuje istniejące połączenie danych EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="070d8-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="070d8-122">Przykład 5: Aktualizowanie istniejącego połączenia danych EventGrid przy użyciu tożsamości</span><span class="sxs-lookup"><span data-stu-id="070d8-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="070d8-123">Powyższe polecenie aktualizuje istniejące połączenie danych programu EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="070d8-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="070d8-124">Przykład 6: Aktualizowanie istniejącego połączenia danych IotHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="070d8-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="070d8-125">Powyższe polecenie aktualizuje istniejące połączenie danych programu IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="070d8-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="070d8-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="070d8-126">PARAMETERS</span></span>

### <span data-ttu-id="070d8-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="070d8-127">-AsJob</span></span>
<span data-ttu-id="070d8-128">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="070d8-128">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="070d8-129">-BlobStorageEventType</span></span>
<span data-ttu-id="070d8-130">Nazwa typu zdarzenia magazynu obiektów BLOB do przetworzenia.</span><span class="sxs-lookup"><span data-stu-id="070d8-130">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-131">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="070d8-131">-ClusterName</span></span>
<span data-ttu-id="070d8-132">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="070d8-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="070d8-133">-Compression</span></span>
<span data-ttu-id="070d8-134">Typ kompresji komunikaty centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="070d8-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-135">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="070d8-135">-ConsumerGroup</span></span>
<span data-ttu-id="070d8-136">Grupa użytkowników centrum wydarzenia/IoT.</span><span class="sxs-lookup"><span data-stu-id="070d8-136">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="070d8-137">-DatabaseName</span></span>
<span data-ttu-id="070d8-138">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="070d8-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="070d8-139">-DataFormat</span></span>
<span data-ttu-id="070d8-140">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="070d8-140">The data format of the message.</span></span>
<span data-ttu-id="070d8-141">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="070d8-141">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="070d8-142">-DefaultProfile</span></span>
<span data-ttu-id="070d8-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="070d8-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="070d8-144">-EventHubResourceId</span></span>
<span data-ttu-id="070d8-145">Identyfikator zasobu centrum zdarzeń, który ma zostać wykorzystany do utworzenia połączenia danych/siatki zdarzeń, jest skonfigurowany w celu wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="070d8-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="070d8-146">-EventSystemProperty</span></span>
<span data-ttu-id="070d8-147">Właściwości systemowe centrum wydarzeń/IoT.</span><span class="sxs-lookup"><span data-stu-id="070d8-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="070d8-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="070d8-149">Jeśli ustawiono wartość PRAWDA, oznacza to, że pokarmowanie powinno ignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="070d8-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-150">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="070d8-150">-InputObject</span></span>
<span data-ttu-id="070d8-151">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="070d8-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="070d8-152">-IotHubResourceId</span></span>
<span data-ttu-id="070d8-153">Identyfikator zasobu Centrum IoT, który ma zostać wykorzystany do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="070d8-154">-Kind</span></span>
<span data-ttu-id="070d8-155">Rodzaj punktu końcowego połączenia danych</span><span class="sxs-lookup"><span data-stu-id="070d8-155">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-156">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="070d8-156">-Location</span></span>
<span data-ttu-id="070d8-157">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="070d8-157">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="070d8-158">-MappingRuleName</span></span>
<span data-ttu-id="070d8-159">Reguła mapowania, która ma być używana do spożycia danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="070d8-160">Opcjonalnie informacje dotyczące mapowania można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="070d8-160">Optionally the mapping information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-161">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="070d8-161">-Name</span></span>
<span data-ttu-id="070d8-162">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-163">-Nowait</span><span class="sxs-lookup"><span data-stu-id="070d8-163">-NoWait</span></span>
<span data-ttu-id="070d8-164">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="070d8-164">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="070d8-165">-ResourceGroupName</span></span>
<span data-ttu-id="070d8-166">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="070d8-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="070d8-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="070d8-168">Nazwa zasad dostępu udziału.</span><span class="sxs-lookup"><span data-stu-id="070d8-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="070d8-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="070d8-170">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="070d8-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-171">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="070d8-171">-SubscriptionId</span></span>
<span data-ttu-id="070d8-172">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="070d8-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="070d8-173">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="070d8-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="070d8-174">-TableName</span></span>
<span data-ttu-id="070d8-175">Tabela, w której dane powinny być spożywane.</span><span class="sxs-lookup"><span data-stu-id="070d8-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="070d8-176">Opcjonalnie informacje dotyczące tabeli można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="070d8-176">Optionally the table information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-177">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="070d8-177">-Confirm</span></span>
<span data-ttu-id="070d8-178">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="070d8-178">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="070d8-179">-WhatIf</span></span>
<span data-ttu-id="070d8-180">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="070d8-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="070d8-181">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="070d8-181">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070d8-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="070d8-182">CommonParameters</span></span>
<span data-ttu-id="070d8-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="070d8-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="070d8-184">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="070d8-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="070d8-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="070d8-185">INPUTS</span></span>

### <span data-ttu-id="070d8-186">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="070d8-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="070d8-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="070d8-187">OUTPUTS</span></span>

### <span data-ttu-id="070d8-188">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="070d8-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="070d8-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="070d8-189">NOTES</span></span>

<span data-ttu-id="070d8-190">PISUJE</span><span class="sxs-lookup"><span data-stu-id="070d8-190">ALIASES</span></span>

<span data-ttu-id="070d8-191">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="070d8-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="070d8-192">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="070d8-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="070d8-193">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="070d8-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="070d8-194">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="070d8-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="070d8-195">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="070d8-196">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="070d8-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="070d8-197">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="070d8-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="070d8-198">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="070d8-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="070d8-199">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="070d8-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="070d8-200">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="070d8-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="070d8-201">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="070d8-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="070d8-202">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="070d8-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="070d8-203">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="070d8-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="070d8-204">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="070d8-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="070d8-205">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="070d8-205">RELATED LINKS</span></span>

