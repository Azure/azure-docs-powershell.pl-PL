---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: ab58d679e9fc3ad62baeded8622b81a0cb8b2f95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203802"
---
# <span data-ttu-id="9dd26-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="9dd26-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="9dd26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd26-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd26-103">Tworzy lub aktualizuje połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="9dd26-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="9dd26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9dd26-104">SYNTAX</span></span>

### <span data-ttu-id="9dd26-105">CreateExpandedEventHub (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9dd26-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9dd26-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9dd26-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9dd26-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="9dd26-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9dd26-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9dd26-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9dd26-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9dd26-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9dd26-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="9dd26-110">DESCRIPTION</span></span>
<span data-ttu-id="9dd26-111">Tworzy lub aktualizuje połączenie danych.</span><span class="sxs-lookup"><span data-stu-id="9dd26-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="9dd26-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9dd26-112">EXAMPLES</span></span>

### <span data-ttu-id="9dd26-113">Przykład 1. Tworzenie nowego połączenia danych aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="9dd26-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="9dd26-114">Powyższe polecenie tworzy nowe połączenie danych aplikacji EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9dd26-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9dd26-115">Przykład 2. Tworzenie nowego połączenia danych z platformą EventGrid</span><span class="sxs-lookup"><span data-stu-id="9dd26-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="9dd26-116">Powyższe polecenie tworzy nowe połączenie danych aplikacji EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9dd26-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9dd26-117">Przykład 3. Tworzenie nowego połączenia danych aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="9dd26-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="9dd26-118">Powyższe polecenie tworzy nowe połączenie danych aplikacji IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9dd26-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9dd26-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dd26-119">PARAMETERS</span></span>

### <span data-ttu-id="9dd26-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9dd26-120">-AsJob</span></span>
<span data-ttu-id="9dd26-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9dd26-121">Run the command as a job</span></span>

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

### <span data-ttu-id="9dd26-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="9dd26-122">-BlobStorageEventType</span></span>
<span data-ttu-id="9dd26-123">Nazwa typu zdarzenia magazynu obiektów blob do przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="9dd26-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="9dd26-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9dd26-124">-ClusterName</span></span>
<span data-ttu-id="9dd26-125">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="9dd26-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9dd26-126">- Compression</span><span class="sxs-lookup"><span data-stu-id="9dd26-126">-Compression</span></span>
<span data-ttu-id="9dd26-127">Typ kompresji komunikatów centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9dd26-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-128">- ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9dd26-128">-ConsumerGroup</span></span>
<span data-ttu-id="9dd26-129">Grupa klientów z centrum zdarzeń/centrum wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="9dd26-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="9dd26-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dd26-130">-DatabaseName</span></span>
<span data-ttu-id="9dd26-131">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="9dd26-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="9dd26-132">- DataFormat</span><span class="sxs-lookup"><span data-stu-id="9dd26-132">-DataFormat</span></span>
<span data-ttu-id="9dd26-133">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="9dd26-133">The data format of the message.</span></span>
<span data-ttu-id="9dd26-134">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="9dd26-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="9dd26-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd26-135">-DefaultProfile</span></span>
<span data-ttu-id="9dd26-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd26-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd26-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd26-137">-EventHubResourceId</span></span>
<span data-ttu-id="9dd26-138">Identyfikator zasobu centrum zdarzeń używany do tworzenia połączenia danych/siatki zdarzeń jest skonfigurowany do wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9dd26-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="9dd26-139">-EventSystemProperty</span></span>
<span data-ttu-id="9dd26-140">Właściwości systemowe centrum zdarzeń/iot.</span><span class="sxs-lookup"><span data-stu-id="9dd26-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="9dd26-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="9dd26-142">Jeśli ta wartość jest ustawiona na prawda, oznacza, że ingestion powinien zignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="9dd26-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="9dd26-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd26-143">-IotHubResourceId</span></span>
<span data-ttu-id="9dd26-144">Identyfikator zasobu centrum Iot, który ma zostać użyty do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="9dd26-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-145">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="9dd26-145">-Kind</span></span>
<span data-ttu-id="9dd26-146">Rodzaj punktu końcowego dla połączenia danych</span><span class="sxs-lookup"><span data-stu-id="9dd26-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="9dd26-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9dd26-147">-Location</span></span>
<span data-ttu-id="9dd26-148">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="9dd26-148">Resource location.</span></span>

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

### <span data-ttu-id="9dd26-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="9dd26-149">-MappingRuleName</span></span>
<span data-ttu-id="9dd26-150">Reguła mapowania, która ma być używana do pozysowywania danych.</span><span class="sxs-lookup"><span data-stu-id="9dd26-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="9dd26-151">Opcjonalnie informacje o mapowaniu można dodać do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="9dd26-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="9dd26-152">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9dd26-152">-Name</span></span>
<span data-ttu-id="9dd26-153">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="9dd26-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9dd26-154">-NoWait</span></span>
<span data-ttu-id="9dd26-155">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9dd26-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9dd26-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd26-156">-ResourceGroupName</span></span>
<span data-ttu-id="9dd26-157">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9dd26-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9dd26-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="9dd26-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="9dd26-159">Nazwa zasad dostępu do udostępniania.</span><span class="sxs-lookup"><span data-stu-id="9dd26-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd26-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="9dd26-161">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="9dd26-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-162">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9dd26-162">-SubscriptionId</span></span>
<span data-ttu-id="9dd26-163">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd26-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9dd26-164">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9dd26-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd26-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="9dd26-165">-TableName</span></span>
<span data-ttu-id="9dd26-166">Tabela, w której powinny być zbierane dane.</span><span class="sxs-lookup"><span data-stu-id="9dd26-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="9dd26-167">Opcjonalnie do każdej wiadomości można dodać informacje z tabeli.</span><span class="sxs-lookup"><span data-stu-id="9dd26-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="9dd26-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9dd26-168">-Confirm</span></span>
<span data-ttu-id="9dd26-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9dd26-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd26-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd26-170">-WhatIf</span></span>
<span data-ttu-id="9dd26-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dd26-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd26-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9dd26-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd26-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd26-173">CommonParameters</span></span>
<span data-ttu-id="9dd26-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd26-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd26-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dd26-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd26-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dd26-176">INPUTS</span></span>

## <span data-ttu-id="9dd26-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd26-177">OUTPUTS</span></span>

### <span data-ttu-id="9dd26-178">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iDataConnection</span><span class="sxs-lookup"><span data-stu-id="9dd26-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="9dd26-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9dd26-179">NOTES</span></span>

<span data-ttu-id="9dd26-180">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9dd26-180">ALIASES</span></span>

## <span data-ttu-id="9dd26-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9dd26-181">RELATED LINKS</span></span>

