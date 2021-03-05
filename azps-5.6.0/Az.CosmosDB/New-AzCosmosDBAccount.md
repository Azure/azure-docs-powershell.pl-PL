---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992825"
---
# <span data-ttu-id="02c7a-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="02c7a-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="02c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="02c7a-103">Utwórz nowe konto WołodekDB.</span><span class="sxs-lookup"><span data-stu-id="02c7a-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="02c7a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02c7a-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02c7a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="02c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="02c7a-106">Utwórz nowe konto AADB w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="02c7a-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="02c7a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02c7a-107">EXAMPLES</span></span>

### <span data-ttu-id="02c7a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02c7a-108">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="02c7a-109">W grupie ResourceGroup resourceGroup zostanie utworzone nowe konto w force ADB o nazwie databaseAccountName.</span><span class="sxs-lookup"><span data-stu-id="02c7a-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="02c7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02c7a-110">PARAMETERS</span></span>

### <span data-ttu-id="02c7a-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="02c7a-111">-ApiKind</span></span>
<span data-ttu-id="02c7a-112">Typ konta bazy danych Dla bazy danych Dla ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="02c7a-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="02c7a-113">Zaakceptowane wartości: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="02c7a-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="02c7a-114">Wartość domyślna: Sql</span><span class="sxs-lookup"><span data-stu-id="02c7a-114">Default value: Sql</span></span>

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

### <span data-ttu-id="02c7a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="02c7a-115">-AsJob</span></span>
<span data-ttu-id="02c7a-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="02c7a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02c7a-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="02c7a-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="02c7a-118">Interwał (w minutach) wykonywania kopii zapasowej (tylko dla kont z okresowymi kopiami zapasowymi w trybie okresowym)</span><span class="sxs-lookup"><span data-stu-id="02c7a-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="02c7a-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="02c7a-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="02c7a-120">Czas(w godzinach), dla którego każda kopia zapasowa jest zachowywana (tylko w przypadku kont z okresowymi kopiami zapasowymi w trybie okresowym)</span><span class="sxs-lookup"><span data-stu-id="02c7a-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="02c7a-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02c7a-121">-Confirm</span></span>
<span data-ttu-id="02c7a-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02c7a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c7a-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="02c7a-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="02c7a-124">Domyślny poziom spójności konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="02c7a-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="02c7a-125">Zaakceptowane wartości: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="02c7a-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="02c7a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c7a-126">-DefaultProfile</span></span>
<span data-ttu-id="02c7a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02c7a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c7a-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="02c7a-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="02c7a-129">Wyłączanie operacji zapisu na zasobach metadanych (bazy danych, kontenery, przepływność) za pośrednictwem kluczy kont</span><span class="sxs-lookup"><span data-stu-id="02c7a-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="02c7a-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="02c7a-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="02c7a-131">Wartość logiczna wskazująca, czy na koncie włączono funkcję AnalyticalStorage.</span><span class="sxs-lookup"><span data-stu-id="02c7a-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="02c7a-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="02c7a-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="02c7a-133">Włącza automatyczne trybu failover obszaru zapisu w rzadkim przypadku, gdy region jest niedostępny z powodu awarii.</span><span class="sxs-lookup"><span data-stu-id="02c7a-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="02c7a-134">Automatyczne tryb failover spowoduje nowy region zapisu dla konta i zostanie wybrany na podstawie priorytetów trybu failover skonfigurowanych dla konta.</span><span class="sxs-lookup"><span data-stu-id="02c7a-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="02c7a-135">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="02c7a-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="02c7a-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="02c7a-136">-EnableFreeTier</span></span>
<span data-ttu-id="02c7a-137">Wartość logiczna wskazująca, czy na koncie jest włączona opcja FreeTier.</span><span class="sxs-lookup"><span data-stu-id="02c7a-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="02c7a-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="02c7a-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="02c7a-139">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="02c7a-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="02c7a-140">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="02c7a-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="02c7a-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02c7a-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="02c7a-142">Włącza sieć wirtualną na koncie bazy danych Db firmy A0.</span><span class="sxs-lookup"><span data-stu-id="02c7a-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="02c7a-143">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="02c7a-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="02c7a-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="02c7a-144">-IpRule</span></span>
<span data-ttu-id="02c7a-145">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="02c7a-145">Firewall support.</span></span> <span data-ttu-id="02c7a-146">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, który ma zostać uwzględniony jako lista dozwolonych adresów IP klienta dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="02c7a-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="02c7a-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="02c7a-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="02c7a-148">URI klucza</span><span class="sxs-lookup"><span data-stu-id="02c7a-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="02c7a-149">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="02c7a-149">-Location</span></span>
<span data-ttu-id="02c7a-150">Dodaj lokalizację do konta bazy danych Db firmy A</span><span class="sxs-lookup"><span data-stu-id="02c7a-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="02c7a-151">Tablica ciągów uporządkowanych według priorytetu trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02c7a-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="02c7a-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="02c7a-152">-LocationObject</span></span>
<span data-ttu-id="02c7a-153">Dodaj lokalizację do konta bazy danych Db firmy A</span><span class="sxs-lookup"><span data-stu-id="02c7a-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="02c7a-154">Tablica obiektów PSLocation.</span><span class="sxs-lookup"><span data-stu-id="02c7a-154">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="02c7a-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="02c7a-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="02c7a-156">W przypadku korzystania z spójności z ograniczoną nieaktualnością ta wartość oznacza czas, w którym stale się powtarza.</span><span class="sxs-lookup"><span data-stu-id="02c7a-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="02c7a-157">Zaakceptowany zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="02c7a-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="02c7a-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="02c7a-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="02c7a-159">W przypadku korzystania z spójności powiązanej stale (Bounded Staleness) ta wartość reprezentuje liczbę żądań, które były nieaktualne.</span><span class="sxs-lookup"><span data-stu-id="02c7a-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="02c7a-160">Zaakceptowany zakres dla tej wartości to 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="02c7a-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="02c7a-161">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="02c7a-161">-Name</span></span>
<span data-ttu-id="02c7a-162">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="02c7a-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02c7a-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="02c7a-163">-NetworkAclBypass</span></span>
<span data-ttu-id="02c7a-164">Czy dla tego konta dla usługi Synapse Link włączono obejście listy Acl sieci, czy nie.</span><span class="sxs-lookup"><span data-stu-id="02c7a-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="02c7a-165">Możliwe wartości to: "Brak", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="02c7a-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="02c7a-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="02c7a-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="02c7a-167">Lista identyfikatorów zasobów, aby zezwolić na obejście Acl sieci dla łącza Synapse Link.</span><span class="sxs-lookup"><span data-stu-id="02c7a-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="02c7a-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="02c7a-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="02c7a-169">Określa, czy dla tego serwera jest dozwolony dostęp do publicznego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="02c7a-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="02c7a-170">Możliwe wartości: "Włączone", "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="02c7a-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="02c7a-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c7a-171">-ResourceGroupName</span></span>
<span data-ttu-id="02c7a-172">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02c7a-172">Name of resource group.</span></span>

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

### <span data-ttu-id="02c7a-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="02c7a-173">-ServerVersion</span></span>
<span data-ttu-id="02c7a-174">ServerVersion, ważne tylko w przypadku kont MongoDB.</span><span class="sxs-lookup"><span data-stu-id="02c7a-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="02c7a-175">— Tag</span><span class="sxs-lookup"><span data-stu-id="02c7a-175">-Tag</span></span>
<span data-ttu-id="02c7a-176">Tabela skrótów tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="02c7a-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="02c7a-177">Użyj pustego ciągu, aby wyczyścić istniejący tag.</span><span class="sxs-lookup"><span data-stu-id="02c7a-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="02c7a-178">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="02c7a-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="02c7a-179">Tablica wartości ciągów ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02c7a-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="02c7a-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="02c7a-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="02c7a-181">Tablica obiektów PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02c7a-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="02c7a-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c7a-182">-WhatIf</span></span>
<span data-ttu-id="02c7a-183">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02c7a-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c7a-184">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="02c7a-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c7a-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c7a-185">CommonParameters</span></span>
<span data-ttu-id="02c7a-186">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c7a-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c7a-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02c7a-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c7a-188">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02c7a-188">INPUTS</span></span>

### <span data-ttu-id="02c7a-189">Microsoft.Azure.Commands.Dosdb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="02c7a-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="02c7a-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02c7a-190">OUTPUTS</span></span>

### <span data-ttu-id="02c7a-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="02c7a-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="02c7a-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02c7a-192">NOTES</span></span>

## <span data-ttu-id="02c7a-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02c7a-193">RELATED LINKS</span></span>
