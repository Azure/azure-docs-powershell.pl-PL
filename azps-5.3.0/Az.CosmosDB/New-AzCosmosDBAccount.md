---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 4e31ae75f6fcea77c179757312988a0abbbb58f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503842"
---
# <span data-ttu-id="68ae6-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="68ae6-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="68ae6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="68ae6-103">Utwórz nowe konto CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="68ae6-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="68ae6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68ae6-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ae6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="68ae6-106">Utwórz nowe konto usługi CosmosDB w danym przystawce zasobów.</span><span class="sxs-lookup"><span data-stu-id="68ae6-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="68ae6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="68ae6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68ae6-108">Example 1</span></span>
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

<span data-ttu-id="68ae6-109">Nowe konto CosmosDB o nazwie databaseAccountName jest tworzone w resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="68ae6-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="68ae6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="68ae6-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="68ae6-111">-ApiKind</span></span>
<span data-ttu-id="68ae6-112">Typ konta bazy danych Cosmos DB, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="68ae6-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="68ae6-113">Akceptowane wartości: SQL, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="68ae6-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="68ae6-114">Wartość domyślna: SQL</span><span class="sxs-lookup"><span data-stu-id="68ae6-114">Default value: Sql</span></span>

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

### <span data-ttu-id="68ae6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68ae6-115">-AsJob</span></span>
<span data-ttu-id="68ae6-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="68ae6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68ae6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68ae6-117">-Confirm</span></span>
<span data-ttu-id="68ae6-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ae6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ae6-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="68ae6-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="68ae6-120">Domyślny poziom spójności konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="68ae6-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="68ae6-121">Akceptowane wartości: BoundedStaleness, ConsistentPrefix, on, Session, silne</span><span class="sxs-lookup"><span data-stu-id="68ae6-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="68ae6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ae6-122">-DefaultProfile</span></span>
<span data-ttu-id="68ae6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68ae6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ae6-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="68ae6-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="68ae6-125">Wyłączanie operacji zapisu w zasobach metadanych (bazach danych, kontenerach, przepływności) za pomocą kluczy kont</span><span class="sxs-lookup"><span data-stu-id="68ae6-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="68ae6-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="68ae6-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="68ae6-127">Wartość logiczna wskazująca, czy AnalyticalStorage jest włączony na koncie.</span><span class="sxs-lookup"><span data-stu-id="68ae6-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ae6-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="68ae6-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="68ae6-129">Włączenie automatycznej pracy awaryjnej regionu zapisu w rzadkim przypadku, gdy region jest niedostępny ze względu na awarię.</span><span class="sxs-lookup"><span data-stu-id="68ae6-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="68ae6-130">Automatyczna praca awaryjna spowoduje powstanie nowego regionu zapisu dla tego konta i zostanie wybrana na podstawie priorytetów pracy awaryjnej skonfigurowanych dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="68ae6-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="68ae6-131">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="68ae6-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="68ae6-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="68ae6-132">-EnableFreeTier</span></span>
<span data-ttu-id="68ae6-133">Wartość logiczna wskazująca, czy FreeTier jest włączony na koncie.</span><span class="sxs-lookup"><span data-stu-id="68ae6-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ae6-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="68ae6-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="68ae6-135">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="68ae6-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="68ae6-136">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="68ae6-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="68ae6-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68ae6-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="68ae6-138">Umożliwia korzystanie z sieci wirtualnej na koncie bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="68ae6-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="68ae6-139">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="68ae6-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="68ae6-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="68ae6-140">-IpRule</span></span>
<span data-ttu-id="68ae6-141">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="68ae6-141">Firewall support.</span></span> <span data-ttu-id="68ae6-142">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, które mają zostać uwzględnione jako lista dozwolonych adresów IP klientów dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="68ae6-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="68ae6-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="68ae6-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="68ae6-144">Identyfikator URI magazynu identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="68ae6-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="68ae6-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="68ae6-145">-Location</span></span>
<span data-ttu-id="68ae6-146">Dodaj lokalizację do konta bazy danych programu Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="68ae6-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="68ae6-147">Tablica ciągów, uporządkowana według priorytetu pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="68ae6-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="68ae6-148">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="68ae6-148">-LocationObject</span></span>
<span data-ttu-id="68ae6-149">Dodaj lokalizację do konta bazy danych programu Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="68ae6-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="68ae6-150">Tablica obiektów PSLocation.</span><span class="sxs-lookup"><span data-stu-id="68ae6-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="68ae6-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="68ae6-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="68ae6-152">W przypadku użycia z ograniczoną spójnością nieodświeżoną ta wartość przedstawia czas nieodświeżony (w wartości TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="68ae6-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="68ae6-153">Dopuszczalny zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="68ae6-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="68ae6-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="68ae6-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="68ae6-155">W przypadku użycia z ograniczoną spójnością nieodświeżoną ta wartość reprezentuje liczbę nieaktualnych żądań, które są tolerowane.</span><span class="sxs-lookup"><span data-stu-id="68ae6-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="68ae6-156">Akceptowanym zakresem dla tej wartości jest 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="68ae6-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="68ae6-157">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68ae6-157">-Name</span></span>
<span data-ttu-id="68ae6-158">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="68ae6-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="68ae6-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="68ae6-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="68ae6-160">Czy dla tego serwera jest dozwolony publiczny dostęp do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="68ae6-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="68ae6-161">Możliwe wartości to: "włączone", "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="68ae6-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="68ae6-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ae6-162">-ResourceGroupName</span></span>
<span data-ttu-id="68ae6-163">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68ae6-163">Name of resource group.</span></span>

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

### <span data-ttu-id="68ae6-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="68ae6-164">-ServerVersion</span></span>
<span data-ttu-id="68ae6-165">ServerVersion, prawidłowy tylko w przypadku MongoDB kont.</span><span class="sxs-lookup"><span data-stu-id="68ae6-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="68ae6-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="68ae6-166">-Tag</span></span>
<span data-ttu-id="68ae6-167">Tagi Hashtable tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="68ae6-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="68ae6-168">Wyczyść istniejące znaczniki za pomocą pustego ciągu.</span><span class="sxs-lookup"><span data-stu-id="68ae6-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="68ae6-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="68ae6-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="68ae6-170">Tablica wartości ciągów z listy ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="68ae6-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="68ae6-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="68ae6-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="68ae6-172">Tablica PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="68ae6-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="68ae6-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ae6-173">-WhatIf</span></span>
<span data-ttu-id="68ae6-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ae6-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ae6-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68ae6-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ae6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ae6-176">CommonParameters</span></span>
<span data-ttu-id="68ae6-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ae6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ae6-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68ae6-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ae6-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68ae6-179">INPUTS</span></span>

### <span data-ttu-id="68ae6-180">Microsoft. Azure. Commands. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="68ae6-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="68ae6-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68ae6-181">OUTPUTS</span></span>

### <span data-ttu-id="68ae6-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="68ae6-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="68ae6-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68ae6-183">NOTES</span></span>

## <span data-ttu-id="68ae6-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68ae6-184">RELATED LINKS</span></span>
 
