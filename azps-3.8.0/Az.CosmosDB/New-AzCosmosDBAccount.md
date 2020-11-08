---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051531"
---
# <span data-ttu-id="e8bb1-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e8bb1-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e8bb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bb1-103">Utwórz nowe konto CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="e8bb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8bb1-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8bb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bb1-106">Utwórz nowe konto usługi CosmosDB w danym przystawce zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="e8bb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="e8bb1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8bb1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="e8bb1-109">Nowe konto CosmosDB o nazwie databaseAccountName jest tworzone w resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="e8bb1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8bb1-110">PARAMETERS</span></span>

### <span data-ttu-id="e8bb1-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="e8bb1-111">-ApiKind</span></span>
<span data-ttu-id="e8bb1-112">Typ konta bazy danych Cosmos DB, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="e8bb1-113">Akceptowane wartości: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="e8bb1-114">Wartość domyślna: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="e8bb1-114">Default value: GlobalDocumentDB</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8bb1-115">-AsJob</span></span>
<span data-ttu-id="e8bb1-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e8bb1-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8bb1-117">-Confirm</span></span>
<span data-ttu-id="e8bb1-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="e8bb1-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="e8bb1-120">Domyślny poziom spójności konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="e8bb1-121">Akceptowane wartości: BoundedStaleness, ConsistentPrefix, on, Session, silne</span><span class="sxs-lookup"><span data-stu-id="e8bb1-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bb1-122">-DefaultProfile</span></span>
<span data-ttu-id="e8bb1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e8bb1-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="e8bb1-125">Wyłączanie operacji zapisu w zasobach metadanych (bazach danych, kontenerach, przepływności) za pomocą kluczy kont</span><span class="sxs-lookup"><span data-stu-id="e8bb1-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="e8bb1-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="e8bb1-127">Włączenie automatycznej pracy awaryjnej regionu zapisu w rzadkim przypadku, gdy region jest niedostępny ze względu na awarię.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="e8bb1-128">Automatyczna praca awaryjna spowoduje powstanie nowego regionu zapisu dla tego konta i zostanie wybrana na podstawie priorytetów pracy awaryjnej skonfigurowanych dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="e8bb1-129">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="e8bb1-129">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="e8bb1-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="e8bb1-131">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="e8bb1-132">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="e8bb1-132">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e8bb1-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="e8bb1-134">Umożliwia korzystanie z sieci wirtualnej na koncie bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="e8bb1-135">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="e8bb1-135">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="e8bb1-136">-IpRangeFilter</span></span>
<span data-ttu-id="e8bb1-137">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-137">Firewall support.</span></span>
<span data-ttu-id="e8bb1-138">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, które mają zostać uwzględnione jako dozwolona lista adresów IP klientów dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8bb1-139">-Location</span></span>
<span data-ttu-id="e8bb1-140">Dodaj lokalizację do konta bazy danych programu Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="e8bb1-141">Tablica ciągów, uporządkowana według priorytetu pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-141">Array of strings, ordered by failover priority.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-142">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="e8bb1-142">-LocationObject</span></span>
<span data-ttu-id="e8bb1-143">Dodaj lokalizację do konta bazy danych programu Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="e8bb1-144">Tablica obiektów PSLocation.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-144">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e8bb1-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="e8bb1-146">W przypadku użycia z ograniczoną spójnością nieodświeżoną ta wartość przedstawia czas nieodświeżony (w wartości TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="e8bb1-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="e8bb1-147">Dopuszczalny zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-147">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="e8bb1-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="e8bb1-149">W przypadku użycia z ograniczoną spójnością nieodświeżoną ta wartość reprezentuje liczbę nieaktualnych żądań, które są tolerowane.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="e8bb1-150">Akceptowanym zakresem dla tej wartości jest 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8bb1-151">-Name</span></span>
<span data-ttu-id="e8bb1-152">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-152">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e8bb1-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="e8bb1-154">Czy dla tego serwera jest dozwolony publiczny dostęp do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="e8bb1-155">Możliwe wartości to: "włączone", "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="e8bb1-155">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bb1-156">-ResourceGroupName</span></span>
<span data-ttu-id="e8bb1-157">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-157">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8bb1-158">-Tag</span></span>
<span data-ttu-id="e8bb1-159">Tagi Hashtable tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="e8bb1-160">Wyczyść istniejące znaczniki za pomocą pustego ciągu.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-160">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e8bb1-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="e8bb1-162">Tablica wartości ciągów z listy ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-162">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e8bb1-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e8bb1-164">Tablica PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8bb1-165">-WhatIf</span></span>
<span data-ttu-id="e8bb1-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8bb1-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bb1-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bb1-168">CommonParameters</span></span>
<span data-ttu-id="e8bb1-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bb1-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bb1-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8bb1-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bb1-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8bb1-171">INPUTS</span></span>

### <span data-ttu-id="e8bb1-172">Microsoft. Azure. Commands. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="e8bb1-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="e8bb1-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8bb1-173">OUTPUTS</span></span>

### <span data-ttu-id="e8bb1-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e8bb1-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e8bb1-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8bb1-175">NOTES</span></span>

## <span data-ttu-id="e8bb1-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8bb1-176">RELATED LINKS</span></span>
