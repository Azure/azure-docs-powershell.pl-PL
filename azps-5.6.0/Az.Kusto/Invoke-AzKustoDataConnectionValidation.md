---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: c12c38227c4d0a3d0a6b58685c1b8b5233c161ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959626"
---
# <span data-ttu-id="ea00e-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="ea00e-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="ea00e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea00e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea00e-103">Sprawdza, czy parametry połączenia danych są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="ea00e-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="ea00e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea00e-104">SYNTAX</span></span>

### <span data-ttu-id="ea00e-105">DataExpandedEventHub (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea00e-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea00e-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ea00e-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea00e-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ea00e-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea00e-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ea00e-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea00e-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="ea00e-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ea00e-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ea00e-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ea00e-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ea00e-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea00e-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ea00e-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea00e-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea00e-113">DESCRIPTION</span></span>
<span data-ttu-id="ea00e-114">Sprawdza, czy parametry połączenia danych są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="ea00e-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="ea00e-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea00e-115">EXAMPLES</span></span>

### <span data-ttu-id="ea00e-116">Przykład 1. Sprawdzanie poprawności parametrów połączenia danych aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="ea00e-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ea00e-117">Powyższe polecenie sprawdza połączenie danych aplikacji EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ea00e-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ea00e-118">Przykład 2. Sprawdzanie poprawności parametrów połączenia danych z siecią EventGrid</span><span class="sxs-lookup"><span data-stu-id="ea00e-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ea00e-119">Powyższe polecenie sprawdza połączenie danych aplikacji EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ea00e-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ea00e-120">Przykład 3. Sprawdzanie poprawności parametrów połączenia danych aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="ea00e-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ea00e-121">Powyższe polecenie sprawdza połączenie danych aplikacji IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ea00e-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ea00e-122">Przykład 4. Sprawdzanie poprawności parametrów połączenia danych aplikacji EventHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="ea00e-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ea00e-123">Powyższe polecenie sprawdza połączenie danych aplikacji EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ea00e-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ea00e-124">Przykład 5. Sprawdzanie poprawności parametrów połączenia danych z aplikacji EventGrid za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="ea00e-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ea00e-125">Powyższe polecenie sprawdza połączenie danych aplikacji EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ea00e-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ea00e-126">Przykład 6. Sprawdzanie poprawności parametrów połączenia danych aplikacji IotHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="ea00e-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ea00e-127">Powyższe polecenie sprawdza połączenie danych aplikacji IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ea00e-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ea00e-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea00e-128">PARAMETERS</span></span>

### <span data-ttu-id="ea00e-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="ea00e-129">-BlobStorageEventType</span></span>
<span data-ttu-id="ea00e-130">Nazwa typu zdarzenia magazynu obiektów blob do przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="ea00e-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="ea00e-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ea00e-131">-ClusterName</span></span>
<span data-ttu-id="ea00e-132">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-133">- Compression</span><span class="sxs-lookup"><span data-stu-id="ea00e-133">-Compression</span></span>
<span data-ttu-id="ea00e-134">Typ kompresji komunikatów centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ea00e-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-135">- ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ea00e-135">-ConsumerGroup</span></span>
<span data-ttu-id="ea00e-136">Grupa klientów z centrum zdarzeń/centrum wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="ea00e-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="ea00e-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea00e-137">-DatabaseName</span></span>
<span data-ttu-id="ea00e-138">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="ea00e-139">-DataConnectionName</span></span>
<span data-ttu-id="ea00e-140">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ea00e-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="ea00e-141">- DataFormat</span><span class="sxs-lookup"><span data-stu-id="ea00e-141">-DataFormat</span></span>
<span data-ttu-id="ea00e-142">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ea00e-142">The data format of the message.</span></span>
<span data-ttu-id="ea00e-143">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ea00e-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="ea00e-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea00e-144">-DefaultProfile</span></span>
<span data-ttu-id="ea00e-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea00e-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea00e-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ea00e-146">-EventHubResourceId</span></span>
<span data-ttu-id="ea00e-147">Identyfikator zasobu centrum zdarzeń używany do tworzenia połączenia danych/siatki zdarzeń jest skonfigurowany do wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ea00e-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="ea00e-148">-EventSystemProperty</span></span>
<span data-ttu-id="ea00e-149">Właściwości systemowe centrum zdarzeń/iot.</span><span class="sxs-lookup"><span data-stu-id="ea00e-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="ea00e-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="ea00e-151">Jeśli ta wartość jest ustawiona na prawda, oznacza, że ingestion powinien zignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="ea00e-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="ea00e-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea00e-152">-InputObject</span></span>
<span data-ttu-id="ea00e-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ea00e-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ea00e-154">-IotHubResourceId</span></span>
<span data-ttu-id="ea00e-155">Identyfikator zasobu centrum Iot, który ma zostać użyty do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ea00e-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-156">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="ea00e-156">-Kind</span></span>
<span data-ttu-id="ea00e-157">Rodzaj punktu końcowego dla połączenia danych</span><span class="sxs-lookup"><span data-stu-id="ea00e-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="ea00e-158">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea00e-158">-Location</span></span>
<span data-ttu-id="ea00e-159">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea00e-159">Resource location.</span></span>

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

### <span data-ttu-id="ea00e-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="ea00e-160">-MappingRuleName</span></span>
<span data-ttu-id="ea00e-161">Reguła mapowania, która ma być używana do pozysowywania danych.</span><span class="sxs-lookup"><span data-stu-id="ea00e-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="ea00e-162">Opcjonalnie informacje o mapowaniu można dodać do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ea00e-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="ea00e-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea00e-163">-ResourceGroupName</span></span>
<span data-ttu-id="ea00e-164">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="ea00e-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="ea00e-166">Nazwa zasad dostępu do udostępniania.</span><span class="sxs-lookup"><span data-stu-id="ea00e-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ea00e-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="ea00e-168">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="ea00e-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-169">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea00e-169">-SubscriptionId</span></span>
<span data-ttu-id="ea00e-170">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea00e-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea00e-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ea00e-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea00e-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="ea00e-172">-TableName</span></span>
<span data-ttu-id="ea00e-173">Tabela, w której powinny być zbierane dane.</span><span class="sxs-lookup"><span data-stu-id="ea00e-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="ea00e-174">Opcjonalnie do każdej wiadomości można dodać informacje z tabeli.</span><span class="sxs-lookup"><span data-stu-id="ea00e-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="ea00e-175">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea00e-175">-Confirm</span></span>
<span data-ttu-id="ea00e-176">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea00e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea00e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea00e-177">-WhatIf</span></span>
<span data-ttu-id="ea00e-178">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea00e-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea00e-179">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea00e-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea00e-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea00e-180">CommonParameters</span></span>
<span data-ttu-id="ea00e-181">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea00e-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea00e-182">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea00e-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea00e-183">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea00e-183">INPUTS</span></span>

### <span data-ttu-id="ea00e-184">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ea00e-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ea00e-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea00e-185">OUTPUTS</span></span>

### <span data-ttu-id="ea00e-186">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="ea00e-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="ea00e-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea00e-187">NOTES</span></span>

<span data-ttu-id="ea00e-188">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ea00e-188">ALIASES</span></span>

<span data-ttu-id="ea00e-189">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea00e-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea00e-190">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ea00e-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea00e-191">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea00e-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea00e-192">INPUTOBJECT: <IKustoIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ea00e-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea00e-193">`[AttachedDatabaseConfigurationName <String>]`: nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ea00e-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ea00e-194">`[ClusterName <String>]`: nazwa klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ea00e-195">`[DataConnectionName <String>]`: nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ea00e-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ea00e-196">`[DatabaseName <String>]`: nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ea00e-197">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ea00e-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea00e-198">`[Location <String>]`: lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ea00e-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ea00e-199">`[PrincipalAssignmentName <String>]`: nazwa dopisu głównego kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ea00e-200">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ea00e-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ea00e-201">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea00e-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ea00e-202">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="ea00e-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ea00e-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea00e-203">RELATED LINKS</span></span>

