---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177234"
---
# <span data-ttu-id="96116-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="96116-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="96116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96116-102">SYNOPSIS</span></span>
<span data-ttu-id="96116-103">Aktualizowanie atrybutów konta Wsad.</span><span class="sxs-lookup"><span data-stu-id="96116-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="96116-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96116-104">SYNTAX</span></span>

### <span data-ttu-id="96116-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="96116-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96116-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96116-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96116-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96116-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96116-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="96116-108">DESCRIPTION</span></span>
<span data-ttu-id="96116-109">Aktualizowanie właściwości konta AADB.</span><span class="sxs-lookup"><span data-stu-id="96116-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="96116-110">Regionów kont nie można zaktualizować tak jak innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="96116-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="96116-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96116-111">EXAMPLES</span></span>

### <span data-ttu-id="96116-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96116-112">Example 1</span></span>
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

<span data-ttu-id="96116-113">Zaktualizowano parametr DefaultConsistencyLevel do wartości "Strong", Włączony AutomaticFailover, Enabled MultipleWriteLocations i Enabled VirtualNetwork dla konta Dosdb o nazwie accountName.</span><span class="sxs-lookup"><span data-stu-id="96116-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="96116-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96116-114">PARAMETERS</span></span>

### <span data-ttu-id="96116-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="96116-115">-AsJob</span></span>
<span data-ttu-id="96116-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="96116-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96116-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96116-117">-Confirm</span></span>
<span data-ttu-id="96116-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="96116-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96116-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="96116-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="96116-120">Domyślny poziom spójności konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="96116-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="96116-121">Zaakceptowane wartości: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="96116-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="96116-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96116-122">-DefaultProfile</span></span>
<span data-ttu-id="96116-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="96116-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96116-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="96116-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="96116-125">Wyłączanie operacji zapisu na zasobach metadanych (bazy danych, kontenery, przepływność) za pośrednictwem kluczy kont</span><span class="sxs-lookup"><span data-stu-id="96116-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="96116-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="96116-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="96116-127">Wartość logiczna wskazująca, czy na koncie włączono funkcję AnalyticalStorage.</span><span class="sxs-lookup"><span data-stu-id="96116-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="96116-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="96116-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="96116-129">Włącza automatyczne trybu failover obszaru zapisu w rzadkim przypadku, gdy region jest niedostępny z powodu awarii.</span><span class="sxs-lookup"><span data-stu-id="96116-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="96116-130">Automatyczna funkcja trybu failover spowoduje nowy region zapisu dla konta i zostanie wybrany na podstawie priorytetów trybu failover skonfigurowanych dla konta.</span><span class="sxs-lookup"><span data-stu-id="96116-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="96116-131">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="96116-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="96116-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="96116-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="96116-133">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="96116-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="96116-134">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="96116-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="96116-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="96116-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="96116-136">Umożliwia korzystanie z sieci wirtualnej na koncie bazy danych Db firmy Ws.</span><span class="sxs-lookup"><span data-stu-id="96116-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="96116-137">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="96116-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="96116-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96116-138">-InputObject</span></span>
<span data-ttu-id="96116-139">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="96116-139">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96116-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="96116-140">-IpRule</span></span>
<span data-ttu-id="96116-141">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="96116-141">Firewall support.</span></span> <span data-ttu-id="96116-142">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, który ma zostać uwzględniony jako lista dozwolonych adresów IP klienta dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="96116-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="96116-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="96116-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="96116-144">URI klucza</span><span class="sxs-lookup"><span data-stu-id="96116-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="96116-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="96116-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="96116-146">W przypadku korzystania z spójności z ograniczoną nieaktualnością ta wartość oznacza czas, w którym stale się powtarza.</span><span class="sxs-lookup"><span data-stu-id="96116-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="96116-147">Zaakceptowany zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="96116-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="96116-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="96116-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="96116-149">W przypadku korzystania z spójności powiązanej nieaktualności ta wartość oznacza liczbę stale powiązanych żądań.</span><span class="sxs-lookup"><span data-stu-id="96116-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="96116-150">Zaakceptowany zakres dla tej wartości to 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="96116-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="96116-151">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="96116-151">-Name</span></span>
<span data-ttu-id="96116-152">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="96116-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="96116-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="96116-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="96116-154">Określa, czy dla tego serwera dozwolony jest dostęp do publicznego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="96116-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="96116-155">Możliwe wartości: "Włączone", "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="96116-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="96116-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96116-156">-ResourceGroupName</span></span>
<span data-ttu-id="96116-157">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96116-157">Name of resource group.</span></span>

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

### <span data-ttu-id="96116-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96116-158">-ResourceId</span></span>
<span data-ttu-id="96116-159">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="96116-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="96116-160">— Tag</span><span class="sxs-lookup"><span data-stu-id="96116-160">-Tag</span></span>
<span data-ttu-id="96116-161">Tabela skrótów tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="96116-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="96116-162">Użyj pustego ciągu, aby wyczyścić istniejący tag.</span><span class="sxs-lookup"><span data-stu-id="96116-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="96116-163">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="96116-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="96116-164">Tablica wartości ciągów ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96116-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="96116-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="96116-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="96116-166">Tablica obiektów PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96116-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="96116-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96116-167">-WhatIf</span></span>
<span data-ttu-id="96116-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96116-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96116-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="96116-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96116-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96116-170">CommonParameters</span></span>
<span data-ttu-id="96116-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96116-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96116-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96116-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96116-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96116-173">INPUTS</span></span>

### <span data-ttu-id="96116-174">Microsoft.Azure.Commands.Dosdb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="96116-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="96116-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96116-175">OUTPUTS</span></span>

### <span data-ttu-id="96116-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="96116-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="96116-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96116-177">NOTES</span></span>

## <span data-ttu-id="96116-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96116-178">RELATED LINKS</span></span>
