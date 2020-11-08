---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233463"
---
# <span data-ttu-id="ce862-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="ce862-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="ce862-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce862-102">SYNOPSIS</span></span>
<span data-ttu-id="ce862-103">Umożliwia utworzenie lub zaktualizowanie połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ce862-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="ce862-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce862-104">SYNTAX</span></span>

### <span data-ttu-id="ce862-105">CreateExpandedEventHub (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ce862-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ce862-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ce862-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce862-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ce862-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ce862-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ce862-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce862-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ce862-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce862-110">Opis</span><span class="sxs-lookup"><span data-stu-id="ce862-110">DESCRIPTION</span></span>
<span data-ttu-id="ce862-111">Umożliwia utworzenie lub zaktualizowanie połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ce862-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="ce862-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce862-112">EXAMPLES</span></span>

### <span data-ttu-id="ce862-113">Przykład 1. Tworzenie nowego połączenia danych EventHub</span><span class="sxs-lookup"><span data-stu-id="ce862-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ce862-114">Powyższe polecenie tworzy nowe połączenie danych EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ce862-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ce862-115">Przykład 2: Tworzenie nowego połączenia danych programu EventGrid</span><span class="sxs-lookup"><span data-stu-id="ce862-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ce862-116">Powyższe polecenie tworzy nowe połączenie danych EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ce862-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ce862-117">Przykład 3: Tworzenie nowego połączenia danych programu IotHub</span><span class="sxs-lookup"><span data-stu-id="ce862-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ce862-118">Powyższe polecenie tworzy nowe połączenie danych IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ce862-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ce862-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce862-119">PARAMETERS</span></span>

### <span data-ttu-id="ce862-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce862-120">-AsJob</span></span>
<span data-ttu-id="ce862-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ce862-121">Run the command as a job</span></span>

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

### <span data-ttu-id="ce862-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="ce862-122">-BlobStorageEventType</span></span>
<span data-ttu-id="ce862-123">Nazwa typu zdarzenia magazynu obiektów BLOB do przetworzenia.</span><span class="sxs-lookup"><span data-stu-id="ce862-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="ce862-124">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ce862-124">-ClusterName</span></span>
<span data-ttu-id="ce862-125">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce862-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ce862-126">-Compression</span><span class="sxs-lookup"><span data-stu-id="ce862-126">-Compression</span></span>
<span data-ttu-id="ce862-127">Typ kompresji komunikaty centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ce862-127">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="ce862-128">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="ce862-128">-ConsumerGroup</span></span>
<span data-ttu-id="ce862-129">Grupa użytkowników centrum wydarzenia/IoT.</span><span class="sxs-lookup"><span data-stu-id="ce862-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="ce862-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce862-130">-DatabaseName</span></span>
<span data-ttu-id="ce862-131">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce862-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ce862-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="ce862-132">-DataFormat</span></span>
<span data-ttu-id="ce862-133">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ce862-133">The data format of the message.</span></span>
<span data-ttu-id="ce862-134">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ce862-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="ce862-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce862-135">-DefaultProfile</span></span>
<span data-ttu-id="ce862-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce862-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce862-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ce862-137">-EventHubResourceId</span></span>
<span data-ttu-id="ce862-138">Identyfikator zasobu centrum zdarzeń, który ma zostać wykorzystany do utworzenia połączenia danych/siatki zdarzeń, jest skonfigurowany w celu wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ce862-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="ce862-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="ce862-139">-EventSystemProperty</span></span>
<span data-ttu-id="ce862-140">Właściwości systemowe centrum wydarzeń/IoT.</span><span class="sxs-lookup"><span data-stu-id="ce862-140">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="ce862-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="ce862-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="ce862-142">Jeśli ustawiono wartość PRAWDA, oznacza to, że pokarmowanie powinno ignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="ce862-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="ce862-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ce862-143">-IotHubResourceId</span></span>
<span data-ttu-id="ce862-144">Identyfikator zasobu Centrum IoT, który ma zostać wykorzystany do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ce862-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="ce862-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="ce862-145">-Kind</span></span>
<span data-ttu-id="ce862-146">Rodzaj punktu końcowego połączenia danych</span><span class="sxs-lookup"><span data-stu-id="ce862-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="ce862-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ce862-147">-Location</span></span>
<span data-ttu-id="ce862-148">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ce862-148">Resource location.</span></span>

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

### <span data-ttu-id="ce862-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="ce862-149">-MappingRuleName</span></span>
<span data-ttu-id="ce862-150">Reguła mapowania, która ma być używana do spożycia danych.</span><span class="sxs-lookup"><span data-stu-id="ce862-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="ce862-151">Opcjonalnie informacje dotyczące mapowania można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ce862-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="ce862-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce862-152">-Name</span></span>
<span data-ttu-id="ce862-153">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="ce862-153">The name of the data connection.</span></span>

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

### <span data-ttu-id="ce862-154">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ce862-154">-NoWait</span></span>
<span data-ttu-id="ce862-155">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ce862-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce862-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce862-156">-ResourceGroupName</span></span>
<span data-ttu-id="ce862-157">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce862-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ce862-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="ce862-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="ce862-159">Nazwa zasad dostępu udziału.</span><span class="sxs-lookup"><span data-stu-id="ce862-159">The name of the share access policy.</span></span>

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

### <span data-ttu-id="ce862-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ce862-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="ce862-161">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="ce862-161">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="ce862-162">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ce862-162">-SubscriptionId</span></span>
<span data-ttu-id="ce862-163">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce862-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce862-164">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ce862-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ce862-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="ce862-165">-TableName</span></span>
<span data-ttu-id="ce862-166">Tabela, w której dane powinny być spożywane.</span><span class="sxs-lookup"><span data-stu-id="ce862-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="ce862-167">Opcjonalnie informacje dotyczące tabeli można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="ce862-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="ce862-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce862-168">-Confirm</span></span>
<span data-ttu-id="ce862-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce862-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce862-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce862-170">-WhatIf</span></span>
<span data-ttu-id="ce862-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce862-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce862-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce862-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce862-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce862-173">CommonParameters</span></span>
<span data-ttu-id="ce862-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce862-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce862-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce862-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce862-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce862-176">INPUTS</span></span>

## <span data-ttu-id="ce862-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce862-177">OUTPUTS</span></span>

### <span data-ttu-id="ce862-178">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="ce862-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="ce862-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce862-179">NOTES</span></span>

<span data-ttu-id="ce862-180">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ce862-180">ALIASES</span></span>

## <span data-ttu-id="ce862-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce862-181">RELATED LINKS</span></span>

