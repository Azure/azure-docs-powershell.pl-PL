---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351514"
---
# <span data-ttu-id="6c869-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="6c869-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="6c869-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c869-102">SYNOPSIS</span></span>
<span data-ttu-id="6c869-103">Umożliwia utworzenie lub zaktualizowanie połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="6c869-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="6c869-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c869-104">SYNTAX</span></span>

### <span data-ttu-id="6c869-105">CreateExpandedEventHub (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c869-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6c869-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="6c869-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c869-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="6c869-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6c869-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="6c869-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c869-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="6c869-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c869-110">Opis</span><span class="sxs-lookup"><span data-stu-id="6c869-110">DESCRIPTION</span></span>
<span data-ttu-id="6c869-111">Umożliwia utworzenie lub zaktualizowanie połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="6c869-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="6c869-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c869-112">EXAMPLES</span></span>

### <span data-ttu-id="6c869-113">Przykład 1. Tworzenie nowego połączenia danych EventHub</span><span class="sxs-lookup"><span data-stu-id="6c869-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="6c869-114">Powyższe polecenie tworzy nowe połączenie danych EventHub o nazwie "myeventhubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="6c869-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="6c869-115">Przykład 2: Tworzenie nowego połączenia danych programu EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c869-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="6c869-116">Powyższe polecenie tworzy nowe połączenie danych EventGrid o nazwie "myeventgriddc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="6c869-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="6c869-117">Przykład 3: Tworzenie nowego połączenia danych programu IotHub</span><span class="sxs-lookup"><span data-stu-id="6c869-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="6c869-118">Powyższe polecenie tworzy nowe połączenie danych IotHub o nazwie "myiothubdc" dla bazy danych "mykustodatabase" w klastrze "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="6c869-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="6c869-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c869-119">PARAMETERS</span></span>

### <span data-ttu-id="6c869-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c869-120">-AsJob</span></span>
<span data-ttu-id="6c869-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6c869-121">Run the command as a job</span></span>

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

### <span data-ttu-id="6c869-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="6c869-122">-BlobStorageEventType</span></span>
<span data-ttu-id="6c869-123">Nazwa typu zdarzenia magazynu obiektów BLOB do przetworzenia.</span><span class="sxs-lookup"><span data-stu-id="6c869-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="6c869-124">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="6c869-124">-ClusterName</span></span>
<span data-ttu-id="6c869-125">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="6c869-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6c869-126">-Compression</span><span class="sxs-lookup"><span data-stu-id="6c869-126">-Compression</span></span>
<span data-ttu-id="6c869-127">Typ kompresji komunikaty centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6c869-127">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="6c869-128">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="6c869-128">-ConsumerGroup</span></span>
<span data-ttu-id="6c869-129">Grupa użytkowników centrum wydarzenia/IoT.</span><span class="sxs-lookup"><span data-stu-id="6c869-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="6c869-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c869-130">-DatabaseName</span></span>
<span data-ttu-id="6c869-131">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="6c869-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="6c869-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="6c869-132">-DataFormat</span></span>
<span data-ttu-id="6c869-133">Format danych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6c869-133">The data format of the message.</span></span>
<span data-ttu-id="6c869-134">Opcjonalnie można dodać format danych do każdej wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6c869-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="6c869-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c869-135">-DefaultProfile</span></span>
<span data-ttu-id="6c869-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c869-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c869-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6c869-137">-EventHubResourceId</span></span>
<span data-ttu-id="6c869-138">Identyfikator zasobu centrum zdarzeń, który ma zostać wykorzystany do utworzenia połączenia danych/siatki zdarzeń, jest skonfigurowany w celu wysyłania zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6c869-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="6c869-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="6c869-139">-EventSystemProperty</span></span>
<span data-ttu-id="6c869-140">Właściwości systemowe centrum wydarzeń/IoT.</span><span class="sxs-lookup"><span data-stu-id="6c869-140">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="6c869-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="6c869-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="6c869-142">Jeśli ustawiono wartość PRAWDA, oznacza to, że pokarmowanie powinno ignorować pierwszy rekord każdego pliku.</span><span class="sxs-lookup"><span data-stu-id="6c869-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="6c869-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6c869-143">-IotHubResourceId</span></span>
<span data-ttu-id="6c869-144">Identyfikator zasobu Centrum IoT, który ma zostać wykorzystany do utworzenia połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="6c869-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="6c869-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="6c869-145">-Kind</span></span>
<span data-ttu-id="6c869-146">Rodzaj punktu końcowego połączenia danych</span><span class="sxs-lookup"><span data-stu-id="6c869-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="6c869-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6c869-147">-Location</span></span>
<span data-ttu-id="6c869-148">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="6c869-148">Resource location.</span></span>

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

### <span data-ttu-id="6c869-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="6c869-149">-MappingRuleName</span></span>
<span data-ttu-id="6c869-150">Reguła mapowania, która ma być używana do spożycia danych.</span><span class="sxs-lookup"><span data-stu-id="6c869-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="6c869-151">Opcjonalnie informacje dotyczące mapowania można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6c869-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="6c869-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c869-152">-Name</span></span>
<span data-ttu-id="6c869-153">Nazwa połączenia danych.</span><span class="sxs-lookup"><span data-stu-id="6c869-153">The name of the data connection.</span></span>

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

### <span data-ttu-id="6c869-154">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6c869-154">-NoWait</span></span>
<span data-ttu-id="6c869-155">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6c869-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6c869-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c869-156">-ResourceGroupName</span></span>
<span data-ttu-id="6c869-157">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="6c869-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6c869-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="6c869-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="6c869-159">Nazwa zasad dostępu udziału.</span><span class="sxs-lookup"><span data-stu-id="6c869-159">The name of the share access policy.</span></span>

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

### <span data-ttu-id="6c869-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6c869-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="6c869-161">Identyfikator zasobu konta magazynu, w którym znajdują się dane.</span><span class="sxs-lookup"><span data-stu-id="6c869-161">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="6c869-162">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6c869-162">-SubscriptionId</span></span>
<span data-ttu-id="6c869-163">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6c869-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6c869-164">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6c869-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6c869-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="6c869-165">-TableName</span></span>
<span data-ttu-id="6c869-166">Tabela, w której dane powinny być spożywane.</span><span class="sxs-lookup"><span data-stu-id="6c869-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="6c869-167">Opcjonalnie informacje dotyczące tabeli można dodawać do poszczególnych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6c869-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="6c869-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c869-168">-Confirm</span></span>
<span data-ttu-id="6c869-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c869-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c869-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c869-170">-WhatIf</span></span>
<span data-ttu-id="6c869-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c869-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c869-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c869-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c869-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c869-173">CommonParameters</span></span>
<span data-ttu-id="6c869-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c869-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c869-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c869-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c869-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c869-176">INPUTS</span></span>

## <span data-ttu-id="6c869-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c869-177">OUTPUTS</span></span>

### <span data-ttu-id="6c869-178">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="6c869-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="6c869-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c869-179">NOTES</span></span>

<span data-ttu-id="6c869-180">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6c869-180">ALIASES</span></span>

## <span data-ttu-id="6c869-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c869-181">RELATED LINKS</span></span>

