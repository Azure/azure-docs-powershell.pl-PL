---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 94a0764b61b32ce55ff4d9aca06a22d67b1edc96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008986"
---
# <span data-ttu-id="445c8-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="445c8-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="445c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445c8-102">SYNOPSIS</span></span>
<span data-ttu-id="445c8-103">Aktualizuje połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-103">Updates a data connection.</span></span>

## <span data-ttu-id="445c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="445c8-104">SYNTAX</span></span>

### <span data-ttu-id="445c8-105">UpdateExpandedEventHub (domyślne)</span><span class="sxs-lookup"><span data-stu-id="445c8-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="445c8-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="445c8-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="445c8-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="445c8-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="445c8-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="445c8-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="445c8-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="445c8-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="445c8-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="445c8-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="445c8-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="445c8-111">DESCRIPTION</span></span>
<span data-ttu-id="445c8-112">Aktualizuje połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-112">Updates a data connection.</span></span>

## <span data-ttu-id="445c8-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="445c8-113">EXAMPLES</span></span>

### <span data-ttu-id="445c8-114">Przykład 1. Aktualizowanie istniejącego połączenia danych aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="445c8-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="445c8-115">Powyższe polecenie aktualizuje istniejące połączenie danych aplikacji EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="445c8-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="445c8-116">Przykład 2. Aktualizowanie istniejącego połączenia danych z siecią EventGrid</span><span class="sxs-lookup"><span data-stu-id="445c8-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="445c8-117">Powyższe polecenie aktualizuje istniejące połączenie danych aplikacji EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="445c8-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="445c8-118">Przykład 3. Aktualizowanie istniejącego połączenia danych aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="445c8-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="445c8-119">Powyższe polecenie aktualizuje istniejące połączenie danych aplikacji IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="445c8-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="445c8-120">Przykład 4. Aktualizowanie istniejącego połączenia danych aplikacji EventHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="445c8-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="445c8-121">Powyższe polecenie aktualizuje istniejące połączenie danych aplikacji EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="445c8-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="445c8-122">Przykład 5. Aktualizowanie istniejącego połączenia danych z siecią EventGrid za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="445c8-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="445c8-123">Powyższe polecenie aktualizuje istniejące połączenie danych aplikacji EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="445c8-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="445c8-124">Przykład 6. Aktualizowanie istniejącego połączenia danych aplikacji IotHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="445c8-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="445c8-125">Powyższe polecenie aktualizuje istniejące połączenie danych aplikacji IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="445c8-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="445c8-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="445c8-126">PARAMETERS</span></span>

### <span data-ttu-id="445c8-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="445c8-127">-AsJob</span></span>
<span data-ttu-id="445c8-128">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="445c8-128">Run the command as a job</span></span>

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

### <span data-ttu-id="445c8-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="445c8-129">-BlobStorageEventType</span></span>
<span data-ttu-id="445c8-130">Nazwa typu zdarzenia magazynu obiektów blob do przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="445c8-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="445c8-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="445c8-131">-ClusterName</span></span>
<span data-ttu-id="445c8-132">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="445c8-133">- Compression</span><span class="sxs-lookup"><span data-stu-id="445c8-133">-Compression</span></span>
<span data-ttu-id="445c8-134">Typ kompresji komunikatów centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="445c8-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="445c8-135">- ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="445c8-135">-ConsumerGroup</span></span>
<span data-ttu-id="445c8-136">Grupa klientów z centrum zdarzeń/centrum wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="445c8-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="445c8-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="445c8-137">-DatabaseName</span></span>
<span data-ttu-id="445c8-138">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="445c8-139">- DataFormat</span><span class="sxs-lookup"><span data-stu-id="445c8-139">-DataFormat</span></span>
<span data-ttu-id="445c8-140">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="445c8-140">The data format of the message.</span></span>
<span data-ttu-id="445c8-141">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="445c8-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="445c8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445c8-142">-DefaultProfile</span></span>
<span data-ttu-id="445c8-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="445c8-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="445c8-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="445c8-144">-EventHubResourceId</span></span>
<span data-ttu-id="445c8-145">Identyfikator zasobu centrum zdarzeń używany do tworzenia połączenia danych/siatki zdarzeń jest skonfigurowany do wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="445c8-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="445c8-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="445c8-146">-EventSystemProperty</span></span>
<span data-ttu-id="445c8-147">Właściwości systemowe centrum zdarzeń/iot.</span><span class="sxs-lookup"><span data-stu-id="445c8-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="445c8-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="445c8-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="445c8-149">Jeśli ta wartość jest ustawiona na prawda, oznacza, że ingestion powinien zignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="445c8-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="445c8-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="445c8-150">-InputObject</span></span>
<span data-ttu-id="445c8-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="445c8-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="445c8-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="445c8-152">-IotHubResourceId</span></span>
<span data-ttu-id="445c8-153">Identyfikator zasobu centrum Iot, który ma zostać użyty do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="445c8-154">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="445c8-154">-Kind</span></span>
<span data-ttu-id="445c8-155">Rodzaj punktu końcowego dla połączenia danych</span><span class="sxs-lookup"><span data-stu-id="445c8-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="445c8-156">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="445c8-156">-Location</span></span>
<span data-ttu-id="445c8-157">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="445c8-157">Resource location.</span></span>

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

### <span data-ttu-id="445c8-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="445c8-158">-MappingRuleName</span></span>
<span data-ttu-id="445c8-159">Reguła mapowania, która ma być używana do pozysowywania danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="445c8-160">Opcjonalnie informacje o mapowaniu można dodać do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="445c8-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="445c8-161">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="445c8-161">-Name</span></span>
<span data-ttu-id="445c8-162">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="445c8-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="445c8-163">-NoWait</span></span>
<span data-ttu-id="445c8-164">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="445c8-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="445c8-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="445c8-165">-ResourceGroupName</span></span>
<span data-ttu-id="445c8-166">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="445c8-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="445c8-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="445c8-168">Nazwa zasad dostępu do udostępniania.</span><span class="sxs-lookup"><span data-stu-id="445c8-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="445c8-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="445c8-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="445c8-170">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="445c8-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="445c8-171">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="445c8-171">-SubscriptionId</span></span>
<span data-ttu-id="445c8-172">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="445c8-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="445c8-173">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="445c8-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="445c8-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="445c8-174">-TableName</span></span>
<span data-ttu-id="445c8-175">Tabela, w której powinny być zbierane dane.</span><span class="sxs-lookup"><span data-stu-id="445c8-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="445c8-176">Opcjonalnie do każdej wiadomości można dodać informacje z tabeli.</span><span class="sxs-lookup"><span data-stu-id="445c8-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="445c8-177">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="445c8-177">-Confirm</span></span>
<span data-ttu-id="445c8-178">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="445c8-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445c8-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445c8-179">-WhatIf</span></span>
<span data-ttu-id="445c8-180">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="445c8-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445c8-181">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="445c8-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445c8-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445c8-182">CommonParameters</span></span>
<span data-ttu-id="445c8-183">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="445c8-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445c8-184">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="445c8-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445c8-185">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="445c8-185">INPUTS</span></span>

### <span data-ttu-id="445c8-186">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="445c8-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="445c8-187">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="445c8-187">OUTPUTS</span></span>

### <span data-ttu-id="445c8-188">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iDataConnection</span><span class="sxs-lookup"><span data-stu-id="445c8-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="445c8-189">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="445c8-189">NOTES</span></span>

<span data-ttu-id="445c8-190">ALIASY</span><span class="sxs-lookup"><span data-stu-id="445c8-190">ALIASES</span></span>

<span data-ttu-id="445c8-191">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="445c8-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="445c8-192">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="445c8-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="445c8-193">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="445c8-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="445c8-194">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="445c8-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="445c8-195">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="445c8-196">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="445c8-197">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="445c8-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="445c8-198">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="445c8-199">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="445c8-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="445c8-200">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="445c8-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="445c8-201">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="445c8-202">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="445c8-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="445c8-203">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="445c8-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="445c8-204">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="445c8-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="445c8-205">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="445c8-205">RELATED LINKS</span></span>

