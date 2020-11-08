---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049518"
---
# <span data-ttu-id="2a9e0-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="2a9e0-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="2a9e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a9e0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9e0-103">Aktualizowanie atrybutów konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="2a9e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a9e0-104">SYNTAX</span></span>

### <span data-ttu-id="2a9e0-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a9e0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a9e0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a9e0-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a9e0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a9e0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a9e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2a9e0-108">DESCRIPTION</span></span>
<span data-ttu-id="2a9e0-109">Aktualizowanie właściwości konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="2a9e0-110">Nie można zaktualizować regionów kont simulataneously z innymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="2a9e0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a9e0-111">EXAMPLES</span></span>

### <span data-ttu-id="2a9e0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a9e0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="2a9e0-113">Zaktualizowano DefaultConsistencyLevel na "mocne", włączono AutomaticFailover, włączono MultipleWriteLocations i włączono VirtualNetwork dla konta CosmosDB o nazwie AccountName.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="2a9e0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a9e0-114">PARAMETERS</span></span>

### <span data-ttu-id="2a9e0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a9e0-115">-AsJob</span></span>
<span data-ttu-id="2a9e0-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2a9e0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a9e0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a9e0-117">-Confirm</span></span>
<span data-ttu-id="2a9e0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a9e0-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="2a9e0-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="2a9e0-120">Domyślny poziom spójności konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="2a9e0-121">Akceptowane wartości: BoundedStaleness, ConsistentPrefix, on, Session, silne</span><span class="sxs-lookup"><span data-stu-id="2a9e0-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="2a9e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9e0-122">-DefaultProfile</span></span>
<span data-ttu-id="2a9e0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a9e0-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="2a9e0-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="2a9e0-125">Wyłączanie operacji zapisu w zasobach metadanych (bazach danych, kontenerach, przepływności) za pomocą kluczy kont</span><span class="sxs-lookup"><span data-stu-id="2a9e0-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="2a9e0-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="2a9e0-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="2a9e0-127">Włączenie automatycznej pracy awaryjnej regionu zapisu w rzadkim przypadku, gdy region jest niedostępny ze względu na awarię.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="2a9e0-128">Automatyczna praca awaryjna spowoduje powstanie nowego regionu zapisu dla tego konta i zostanie wybrana na podstawie priorytetów pracy awaryjnej skonfigurowanych dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="2a9e0-129">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="2a9e0-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="2a9e0-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="2a9e0-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="2a9e0-131">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="2a9e0-132">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="2a9e0-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="2a9e0-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a9e0-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="2a9e0-134">Umożliwia korzystanie z sieci wirtualnej na koncie bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="2a9e0-135">Akceptowane wartości: FAŁSZ, prawda</span><span class="sxs-lookup"><span data-stu-id="2a9e0-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="2a9e0-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a9e0-136">-InputObject</span></span>
<span data-ttu-id="2a9e0-137">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2a9e0-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9e0-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="2a9e0-138">-IpRangeFilter</span></span>
<span data-ttu-id="2a9e0-139">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-139">Firewall support.</span></span>
<span data-ttu-id="2a9e0-140">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, które mają zostać uwzględnione jako dozwolona lista adresów IP klientów dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="2a9e0-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2a9e0-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="2a9e0-142">W przypadku użycia z ograniczoną spójnością nieodświeżoną ta wartość przedstawia czas nieodświeżony (w wartości TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="2a9e0-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="2a9e0-143">Dopuszczalny zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="2a9e0-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="2a9e0-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="2a9e0-145">W przypadku użycia z ograniczoną spójnością nieodświeżoną ta wartość reprezentuje liczbę nieaktualnych żądań, które są tolerowane.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="2a9e0-146">Akceptowanym zakresem dla tej wartości jest 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="2a9e0-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a9e0-147">-Name</span></span>
<span data-ttu-id="2a9e0-148">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-148">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9e0-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2a9e0-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="2a9e0-150">Czy dla tego serwera jest dozwolony publiczny dostęp do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="2a9e0-151">Możliwe wartości to: "włączone", "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="2a9e0-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="2a9e0-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9e0-152">-ResourceGroupName</span></span>
<span data-ttu-id="2a9e0-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-153">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9e0-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a9e0-154">-ResourceId</span></span>
<span data-ttu-id="2a9e0-155">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="2a9e0-155">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9e0-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a9e0-156">-Tag</span></span>
<span data-ttu-id="2a9e0-157">Tagi Hashtable tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="2a9e0-158">Wyczyść istniejące znaczniki za pomocą pustego ciągu.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="2a9e0-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2a9e0-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="2a9e0-160">Tablica wartości ciągów z listy ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="2a9e0-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="2a9e0-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="2a9e0-162">Tablica PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9e0-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a9e0-163">-WhatIf</span></span>
<span data-ttu-id="2a9e0-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a9e0-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a9e0-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9e0-166">CommonParameters</span></span>
<span data-ttu-id="2a9e0-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9e0-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a9e0-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9e0-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a9e0-169">INPUTS</span></span>

### <span data-ttu-id="2a9e0-170">Microsoft. Azure. Commands. CosmosDB. models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="2a9e0-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="2a9e0-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a9e0-171">OUTPUTS</span></span>

### <span data-ttu-id="2a9e0-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2a9e0-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2a9e0-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a9e0-173">NOTES</span></span>

## <span data-ttu-id="2a9e0-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a9e0-174">RELATED LINKS</span></span>
