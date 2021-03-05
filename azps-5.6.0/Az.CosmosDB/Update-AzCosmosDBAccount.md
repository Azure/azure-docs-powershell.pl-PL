---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010737"
---
# <span data-ttu-id="e7f3f-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e7f3f-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e7f3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f3f-103">Aktualizowanie atrybutów konta Wsad.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="e7f3f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7f3f-104">SYNTAX</span></span>

### <span data-ttu-id="e7f3f-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e7f3f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f3f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7f3f-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f3f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7f3f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f3f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7f3f-108">DESCRIPTION</span></span>
<span data-ttu-id="e7f3f-109">Aktualizowanie właściwości konta AADB.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="e7f3f-110">Regionów kont nie można zaktualizować tak jak innych właściwości.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="e7f3f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7f3f-111">EXAMPLES</span></span>

### <span data-ttu-id="e7f3f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7f3f-112">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="e7f3f-113">Zaktualizowano parametr DefaultConsistencyLevel do wartości "Strong", Włączony AutomaticFailover, Enabled MultipleWriteLocations i Enabled VirtualNetwork dla konta Dosdb o nazwie accountName.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="e7f3f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7f3f-114">PARAMETERS</span></span>

### <span data-ttu-id="e7f3f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e7f3f-115">-AsJob</span></span>
<span data-ttu-id="e7f3f-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e7f3f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7f3f-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="e7f3f-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="e7f3f-118">Interwał (w minutach) wykonywania kopii zapasowej (tylko dla kont z okresowymi kopiami zapasowymi w trybie okresowym)</span><span class="sxs-lookup"><span data-stu-id="e7f3f-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="e7f3f-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="e7f3f-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="e7f3f-120">Czas(w godzinach), dla którego każda kopia zapasowa jest zachowywana (tylko w przypadku kont z okresowymi kopiami zapasowymi w trybie okresowym)</span><span class="sxs-lookup"><span data-stu-id="e7f3f-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="e7f3f-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7f3f-121">-Confirm</span></span>
<span data-ttu-id="e7f3f-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f3f-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="e7f3f-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="e7f3f-124">Domyślny poziom spójności konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="e7f3f-125">Zaakceptowane wartości: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="e7f3f-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="e7f3f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f3f-126">-DefaultProfile</span></span>
<span data-ttu-id="e7f3f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f3f-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e7f3f-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="e7f3f-129">Wyłączanie operacji zapisu na zasobach metadanych (bazy danych, kontenery, przepływność) za pośrednictwem kluczy kont</span><span class="sxs-lookup"><span data-stu-id="e7f3f-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="e7f3f-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="e7f3f-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="e7f3f-131">Wartość logiczna wskazująca, czy na koncie włączono funkcję AnalyticalStorage.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="e7f3f-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="e7f3f-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="e7f3f-133">Włącza automatyczne trybu failover obszaru zapisu w rzadkim przypadku, gdy region jest niedostępny z powodu awarii.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="e7f3f-134">Automatyczne tryb failover spowoduje nowy region zapisu dla konta i zostanie wybrany na podstawie priorytetów trybu failover skonfigurowanych dla konta.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="e7f3f-135">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="e7f3f-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e7f3f-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="e7f3f-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="e7f3f-137">Włącz wiele lokalizacji zapisu.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="e7f3f-138">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="e7f3f-138">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e7f3f-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7f3f-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="e7f3f-140">Włącza sieć wirtualną na koncie bazy danych Db firmy A0.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="e7f3f-141">Zaakceptowane wartości: fałsz, prawda</span><span class="sxs-lookup"><span data-stu-id="e7f3f-141">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e7f3f-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f3f-142">-InputObject</span></span>
<span data-ttu-id="e7f3f-143">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="e7f3f-143">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e7f3f-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e7f3f-144">-IpRule</span></span>
<span data-ttu-id="e7f3f-145">Obsługa zapory.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-145">Firewall support.</span></span> <span data-ttu-id="e7f3f-146">Określa zestaw adresów IP lub zakresów adresów IP w formularzu CIDR, który ma zostać uwzględniony jako lista dozwolonych adresów IP klienta dla danego konta bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="e7f3f-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="e7f3f-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="e7f3f-148">URI klucza</span><span class="sxs-lookup"><span data-stu-id="e7f3f-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="e7f3f-149">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e7f3f-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="e7f3f-150">W przypadku korzystania z spójności z ograniczoną nieaktualnością ta wartość oznacza czas, w którym stale się powtarza.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="e7f3f-151">Zaakceptowany zakres dla tej wartości to 5-86400.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-151">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="e7f3f-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="e7f3f-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="e7f3f-153">W przypadku korzystania z spójności powiązanej stale (Bounded Staleness) ta wartość reprezentuje liczbę żądań, które były nieaktualne.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="e7f3f-154">Zaakceptowany zakres dla tej wartości to 1 – 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="e7f3f-155">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7f3f-155">-Name</span></span>
<span data-ttu-id="e7f3f-156">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-156">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7f3f-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="e7f3f-157">-NetworkAclBypass</span></span>
<span data-ttu-id="e7f3f-158">Czy dla tego konta dla usługi Synapse Link włączono obejście listy Acl sieci, czy nie.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="e7f3f-159">Możliwe wartości to: "Brak", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="e7f3f-159">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="e7f3f-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f3f-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="e7f3f-161">Lista identyfikatorów zasobów, aby zezwolić na obejście Acl sieci dla łącza Synapse Link.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="e7f3f-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e7f3f-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="e7f3f-163">Określa, czy dla tego serwera jest dozwolony dostęp do publicznego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="e7f3f-164">Możliwe wartości: "Włączone", "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="e7f3f-164">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="e7f3f-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f3f-165">-ResourceGroupName</span></span>
<span data-ttu-id="e7f3f-166">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-166">Name of resource group.</span></span>

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

### <span data-ttu-id="e7f3f-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f3f-167">-ResourceId</span></span>
<span data-ttu-id="e7f3f-168">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-168">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="e7f3f-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="e7f3f-169">-ServerVersion</span></span>
<span data-ttu-id="e7f3f-170">ServerVersion, ważne tylko w przypadku kont MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="e7f3f-171">— Tag</span><span class="sxs-lookup"><span data-stu-id="e7f3f-171">-Tag</span></span>
<span data-ttu-id="e7f3f-172">Tabela skrótów tagów jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="e7f3f-173">Użyj pustego ciągu, aby wyczyścić istniejący tag.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-173">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="e7f3f-174">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7f3f-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="e7f3f-175">Tablica wartości ciągów ACL dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-175">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="e7f3f-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e7f3f-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e7f3f-177">Tablica obiektów PSVirtualNetworkRuleObjects dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="e7f3f-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f3f-178">-WhatIf</span></span>
<span data-ttu-id="e7f3f-179">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f3f-180">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f3f-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f3f-181">CommonParameters</span></span>
<span data-ttu-id="e7f3f-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f3f-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f3f-183">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7f3f-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f3f-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7f3f-184">INPUTS</span></span>

### <span data-ttu-id="e7f3f-185">Microsoft.Azure.Commands.Dosdb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="e7f3f-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="e7f3f-186">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7f3f-186">OUTPUTS</span></span>

### <span data-ttu-id="e7f3f-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e7f3f-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e7f3f-188">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7f3f-188">NOTES</span></span>

## <span data-ttu-id="e7f3f-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7f3f-189">RELATED LINKS</span></span>
