---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233475"
---
# <span data-ttu-id="26a1a-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="26a1a-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="26a1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="26a1a-103">Sprawdza, czy parametry połączenia danych są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="26a1a-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="26a1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26a1a-104">SYNTAX</span></span>

### <span data-ttu-id="26a1a-105">DataExpandedEventHub (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26a1a-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26a1a-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="26a1a-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26a1a-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="26a1a-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26a1a-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="26a1a-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26a1a-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="26a1a-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="26a1a-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="26a1a-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="26a1a-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="26a1a-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26a1a-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="26a1a-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26a1a-113">Opis</span><span class="sxs-lookup"><span data-stu-id="26a1a-113">DESCRIPTION</span></span>
<span data-ttu-id="26a1a-114">Sprawdza, czy parametry połączenia danych są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="26a1a-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="26a1a-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26a1a-115">EXAMPLES</span></span>

### <span data-ttu-id="26a1a-116">Przykład 1. Sprawdź parametry połączenia danych EventHub</span><span class="sxs-lookup"><span data-stu-id="26a1a-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="26a1a-117">Powyższe polecenie sprawdza poprawność połączenia danych EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="26a1a-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="26a1a-118">Przykład 2: sprawdzanie poprawności parametrów połączenia danych EventGrid</span><span class="sxs-lookup"><span data-stu-id="26a1a-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="26a1a-119">Powyższe polecenie sprawdza poprawność połączenia danych EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="26a1a-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="26a1a-120">Przykład 3: sprawdzanie poprawności parametrów połączenia danych IotHub</span><span class="sxs-lookup"><span data-stu-id="26a1a-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="26a1a-121">Powyższe polecenie sprawdza poprawność połączenia danych IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="26a1a-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="26a1a-122">Przykład 4: sprawdzanie poprawności parametrów połączenia danych EventHub za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="26a1a-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="26a1a-123">Powyższe polecenie sprawdza poprawność połączenia danych EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="26a1a-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="26a1a-124">Przykład 5: weryfikowanie parametrów połączenia danych EventGrid przy użyciu tożsamości</span><span class="sxs-lookup"><span data-stu-id="26a1a-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="26a1a-125">Powyższe polecenie sprawdza poprawność połączenia danych EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="26a1a-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="26a1a-126">Przykład 6: weryfikowanie parametrów połączenia danych IotHub przy użyciu tożsamości</span><span class="sxs-lookup"><span data-stu-id="26a1a-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="26a1a-127">Powyższe polecenie sprawdza poprawność połączenia danych IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="26a1a-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="26a1a-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26a1a-128">PARAMETERS</span></span>

### <span data-ttu-id="26a1a-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="26a1a-129">-BlobStorageEventType</span></span>
<span data-ttu-id="26a1a-130">Nazwa typu zdarzenia magazynu obiektów BLOB do przetworzenia.</span><span class="sxs-lookup"><span data-stu-id="26a1a-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="26a1a-131">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="26a1a-131">-ClusterName</span></span>
<span data-ttu-id="26a1a-132">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="26a1a-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="26a1a-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="26a1a-133">-Compression</span></span>
<span data-ttu-id="26a1a-134">Typ kompresji komunikaty centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26a1a-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="26a1a-135">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="26a1a-135">-ConsumerGroup</span></span>
<span data-ttu-id="26a1a-136">Grupa użytkowników centrum wydarzenia/IoT.</span><span class="sxs-lookup"><span data-stu-id="26a1a-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="26a1a-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26a1a-137">-DatabaseName</span></span>
<span data-ttu-id="26a1a-138">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="26a1a-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="26a1a-139">-Dataconnectionname</span><span class="sxs-lookup"><span data-stu-id="26a1a-139">-DataConnectionName</span></span>
<span data-ttu-id="26a1a-140">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="26a1a-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="26a1a-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="26a1a-141">-DataFormat</span></span>
<span data-ttu-id="26a1a-142">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="26a1a-142">The data format of the message.</span></span>
<span data-ttu-id="26a1a-143">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="26a1a-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="26a1a-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a1a-144">-DefaultProfile</span></span>
<span data-ttu-id="26a1a-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26a1a-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26a1a-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="26a1a-146">-EventHubResourceId</span></span>
<span data-ttu-id="26a1a-147">Identyfikator zasobu centrum zdarzeń, który ma zostać wykorzystany do utworzenia połączenia danych/siatki zdarzeń, jest skonfigurowany w celu wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26a1a-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="26a1a-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="26a1a-148">-EventSystemProperty</span></span>
<span data-ttu-id="26a1a-149">Właściwości systemowe centrum wydarzeń/IoT.</span><span class="sxs-lookup"><span data-stu-id="26a1a-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="26a1a-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="26a1a-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="26a1a-151">Jeśli ustawiono wartość PRAWDA, oznacza to, że pokarmowanie powinno ignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="26a1a-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="26a1a-152">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26a1a-152">-InputObject</span></span>
<span data-ttu-id="26a1a-153">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="26a1a-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="26a1a-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="26a1a-154">-IotHubResourceId</span></span>
<span data-ttu-id="26a1a-155">Identyfikator zasobu Centrum IoT, który ma zostać wykorzystany do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="26a1a-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="26a1a-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="26a1a-156">-Kind</span></span>
<span data-ttu-id="26a1a-157">Rodzaj punktu końcowego połączenia danych</span><span class="sxs-lookup"><span data-stu-id="26a1a-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="26a1a-158">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="26a1a-158">-Location</span></span>
<span data-ttu-id="26a1a-159">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="26a1a-159">Resource location.</span></span>

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

### <span data-ttu-id="26a1a-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="26a1a-160">-MappingRuleName</span></span>
<span data-ttu-id="26a1a-161">Reguła mapowania, która ma być używana do spożycia danych.</span><span class="sxs-lookup"><span data-stu-id="26a1a-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="26a1a-162">Opcjonalnie informacje dotyczące mapowania można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="26a1a-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="26a1a-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a1a-163">-ResourceGroupName</span></span>
<span data-ttu-id="26a1a-164">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="26a1a-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="26a1a-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="26a1a-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="26a1a-166">Nazwa zasad dostępu udziału.</span><span class="sxs-lookup"><span data-stu-id="26a1a-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="26a1a-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="26a1a-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="26a1a-168">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="26a1a-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="26a1a-169">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="26a1a-169">-SubscriptionId</span></span>
<span data-ttu-id="26a1a-170">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="26a1a-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="26a1a-171">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="26a1a-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="26a1a-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="26a1a-172">-TableName</span></span>
<span data-ttu-id="26a1a-173">Tabela, w której dane powinny być spożywane.</span><span class="sxs-lookup"><span data-stu-id="26a1a-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="26a1a-174">Opcjonalnie informacje dotyczące tabeli można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="26a1a-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="26a1a-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26a1a-175">-Confirm</span></span>
<span data-ttu-id="26a1a-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a1a-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a1a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a1a-177">-WhatIf</span></span>
<span data-ttu-id="26a1a-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a1a-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a1a-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26a1a-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a1a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a1a-180">CommonParameters</span></span>
<span data-ttu-id="26a1a-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a1a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a1a-182">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26a1a-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a1a-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a1a-183">INPUTS</span></span>

### <span data-ttu-id="26a1a-184">Microsoft. Azure. PowerShell. polecenia. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="26a1a-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="26a1a-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26a1a-185">OUTPUTS</span></span>

### <span data-ttu-id="26a1a-186">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="26a1a-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="26a1a-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26a1a-187">NOTES</span></span>

<span data-ttu-id="26a1a-188">PISUJE</span><span class="sxs-lookup"><span data-stu-id="26a1a-188">ALIASES</span></span>

<span data-ttu-id="26a1a-189">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26a1a-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26a1a-190">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="26a1a-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26a1a-191">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26a1a-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26a1a-192">INPUTobject <IKustoIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="26a1a-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26a1a-193">`[AttachedDatabaseConfigurationName <String>]`: Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="26a1a-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="26a1a-194">`[ClusterName <String>]`: Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="26a1a-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="26a1a-195">`[DataConnectionName <String>]`: Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="26a1a-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="26a1a-196">`[DatabaseName <String>]`: Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="26a1a-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="26a1a-197">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="26a1a-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26a1a-198">`[Location <String>]`: Lokalizacja platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26a1a-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="26a1a-199">`[PrincipalAssignmentName <String>]`: Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="26a1a-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="26a1a-200">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="26a1a-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="26a1a-201">`[SubscriptionId <String>]`: Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="26a1a-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="26a1a-202">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="26a1a-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="26a1a-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26a1a-203">RELATED LINKS</span></span>

