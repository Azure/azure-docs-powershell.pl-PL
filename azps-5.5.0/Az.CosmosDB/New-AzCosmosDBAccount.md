---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 810888885c53381c274f85dc79ea2dd7bd4492c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198987"
---
# <span data-ttu-id="39340-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="39340-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="39340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39340-102">SYNOPSIS</span></span>
<span data-ttu-id="39340-103">Utwórz nowe konto WołodekDB.</span><span class="sxs-lookup"><span data-stu-id="39340-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="39340-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39340-104">SYNTAX</span></span>

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

## <span data-ttu-id="39340-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39340-105">DESCRIPTION</span></span>
<span data-ttu-id="39340-106">Utwórz nowe konto AADB w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="39340-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="39340-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39340-107">EXAMPLES</span></span>

### <span data-ttu-id="39340-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39340-108">Example 1</span></span>
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

<span data-ttu-id="39340-109">W grupie ResourceGroup resourceGroup zostanie utworzone nowe konto w force ADB o nazwie databaseAccountName.</span><span class="sxs-lookup"><span data-stu-id="39340-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="39340-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39340-110">PARAMETERS</span></span>

### <span data-ttu-id="39340-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="39340-111">-ApiKind</span></span>
<span data-ttu-id="39340-112">Typ konta bazy danych Dla bazy danych Dla ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="39340-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="39340-113">Zaakceptowane wartości: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="39340-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="39340-114">Wartość domyślna: Sql</span><span class="sxs-lookup"><span data-stu-id="39340-114">Default value: Sql</span></span>

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

### <span data-ttu-id="39340-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="39340-115">-AsJob</span></span>
<span data-ttu-id="39340-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="39340-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39340-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39340-117">-Confirm</span></span>
<span data-ttu-id="39340-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39340-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39340-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="39340-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="39340-120">Domyślny poziom spójności konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="39340-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="39340-121">Zaakceptowane wartości: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="39340-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="39340-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39340-122">-DefaultProfile</span></span>
<span data-ttu-id="39340-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39340-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39340-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="39340-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="39340-125">Wyłączanie operacji zapisu na zasobach metadanych (bazy danych, kontenery, przepływność) za pośrednictwem kluczy kont</span><span class="sxs-lookup"><span data-stu-id="39340-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="39340-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="39340-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="39340-127">Wartość logiczna wskazująca, czy na koncie włączono funkcję AnalyticalStorage.</span><span class="sxs-lookup"><span data-stu-id="39340-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="39340-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="39340-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="39340-129">Włącza automatyczne trybu failover obszaru zapisu w rzadkim przypadku, gdy region jest niedostępny z powodu awarii.</span><span class="sxs-lookup"><span data-stu-id="39340-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="39340-130">Automatyczne tryb failover spowoduje nowy region zapisu dla konta i zostanie wybrany na podstawie priorytetów trybu failover skonfigurowanych dla konta.</span><span class="sxs-lookup"><span data-stu-id="39340-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="39340-131">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="39340-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="39340-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="39340-132">-EnableFreeTier</span></span>
<span data-ttu-id="39340-133">Wartość logiczna wskazująca, czy na koncie jest włączona opcja FreeTier.</span><span class="sxs-lookup"><span data-stu-id="39340-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="39340-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="39340-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="39340-135">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="39340-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="39340-136">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="39340-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="39340-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="39340-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="39340-138">Włącza sieć wirtualną na koncie bazy danych Db firmy A0.</span><span class="sxs-lookup"><span data-stu-id="39340-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="39340-139">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="39340-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="39340-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="39340-140">-IpRule</span></span>
<span data-ttu-id="39340-141">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="39340-141">Firewall support.</span></span> <span data-ttu-id="39340-142">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, który ma zostać uwzględniony jako lista dozwolonych adresów IP klienta dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="39340-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="39340-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="39340-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="39340-144">URI klucza</span><span class="sxs-lookup"><span data-stu-id="39340-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="39340-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="39340-145">-Location</span></span>
<span data-ttu-id="39340-146">Dodaj lokalizację do konta bazy danych Db firmy A</span><span class="sxs-lookup"><span data-stu-id="39340-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="39340-147">Tablica ciągów uporządkowanych według priorytetu trybu failover.</span><span class="sxs-lookup"><span data-stu-id="39340-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="39340-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="39340-148">-LocationObject</span></span>
<span data-ttu-id="39340-149">Dodaj lokalizację do konta bazy danych Db firmy A</span><span class="sxs-lookup"><span data-stu-id="39340-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="39340-150">Tablica obiektów PSLocation.</span><span class="sxs-lookup"><span data-stu-id="39340-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="39340-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="39340-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="39340-152">W przypadku korzystania z spójności z ograniczoną nieaktualnością ta wartość oznacza czas, w którym stale się powtarza.</span><span class="sxs-lookup"><span data-stu-id="39340-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="39340-153">Zaakceptowany zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="39340-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="39340-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="39340-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="39340-155">W przypadku korzystania z spójności powiązanej stale (Bounded Staleness) ta wartość reprezentuje liczbę żądań, które były nieaktualne.</span><span class="sxs-lookup"><span data-stu-id="39340-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="39340-156">Zaakceptowany zakres dla tej wartości to 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="39340-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="39340-157">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="39340-157">-Name</span></span>
<span data-ttu-id="39340-158">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="39340-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39340-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="39340-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="39340-160">Określa, czy dla tego serwera jest dozwolony dostęp do publicznego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="39340-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="39340-161">Możliwe wartości: "Włączone", "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="39340-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="39340-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39340-162">-ResourceGroupName</span></span>
<span data-ttu-id="39340-163">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39340-163">Name of resource group.</span></span>

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

### <span data-ttu-id="39340-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="39340-164">-ServerVersion</span></span>
<span data-ttu-id="39340-165">ServerVersion, ważne tylko w przypadku kont MongoDB.</span><span class="sxs-lookup"><span data-stu-id="39340-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="39340-166">— Tag</span><span class="sxs-lookup"><span data-stu-id="39340-166">-Tag</span></span>
<span data-ttu-id="39340-167">Tabela skrótów tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="39340-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="39340-168">Użyj pustego ciągu, aby wyczyścić istniejący tag.</span><span class="sxs-lookup"><span data-stu-id="39340-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="39340-169">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="39340-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="39340-170">Tablica wartości ciągów ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39340-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="39340-171">- VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="39340-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="39340-172">Tablica obiektów PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39340-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="39340-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39340-173">-WhatIf</span></span>
<span data-ttu-id="39340-174">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39340-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39340-175">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="39340-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39340-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39340-176">CommonParameters</span></span>
<span data-ttu-id="39340-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39340-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39340-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39340-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39340-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39340-179">INPUTS</span></span>

### <span data-ttu-id="39340-180">Microsoft.Azure.Commands.Dosdb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="39340-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="39340-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39340-181">OUTPUTS</span></span>

### <span data-ttu-id="39340-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="39340-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="39340-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39340-183">NOTES</span></span>

## <span data-ttu-id="39340-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39340-184">RELATED LINKS</span></span>
