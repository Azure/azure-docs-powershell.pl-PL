---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501698"
---
# <span data-ttu-id="c5b31-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="c5b31-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="c5b31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5b31-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b31-103">Aktualizowanie regionów konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c5b31-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="c5b31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5b31-104">SYNTAX</span></span>

### <span data-ttu-id="c5b31-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c5b31-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5b31-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b31-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b31-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b31-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b31-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c5b31-108">DESCRIPTION</span></span>
<span data-ttu-id="c5b31-109">Aktualizowanie regionów konta CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c5b31-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="c5b31-110">Lokalizację można podać jako obiekt typu PSLocation lub jako ciągi nazw lokalizacji uporządkowanych według priorytetu pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="c5b31-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="c5b31-111">W parametrze locationobject jest oczekiwana lista bieżących lokalizacji (prioritiies w trybie failover) dołączonych przez nowy LocationObjects odpowiadający nowym lokalizacjom, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="c5b31-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="c5b31-112">Parametr lokalizacji oczekuje listy bieżącej lokalizacji (uporządkowanej według priorytetu pracy awaryjnej) i nowych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c5b31-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="c5b31-113">Uwaga: obsługujemy także Dodawanie regionów.</span><span class="sxs-lookup"><span data-stu-id="c5b31-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="c5b31-114">Podaj lokalizację lub lokalizację.</span><span class="sxs-lookup"><span data-stu-id="c5b31-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="c5b31-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5b31-115">EXAMPLES</span></span>

### <span data-ttu-id="c5b31-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5b31-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="c5b31-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5b31-117">PARAMETERS</span></span>

### <span data-ttu-id="c5b31-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5b31-118">-AsJob</span></span>
<span data-ttu-id="c5b31-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c5b31-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5b31-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5b31-120">-Confirm</span></span>
<span data-ttu-id="c5b31-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5b31-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b31-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b31-122">-DefaultProfile</span></span>
<span data-ttu-id="c5b31-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5b31-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b31-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c5b31-124">-InputObject</span></span>
<span data-ttu-id="c5b31-125">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="c5b31-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c5b31-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c5b31-126">-Location</span></span>
<span data-ttu-id="c5b31-127">Nazwa lokalizacji, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="c5b31-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="c5b31-128">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="c5b31-128">-LocationObject</span></span>
<span data-ttu-id="c5b31-129">Dodaj lokalizację do konta bazy danych programu Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c5b31-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="c5b31-130">Tablica obiektów PSLocation.</span><span class="sxs-lookup"><span data-stu-id="c5b31-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="c5b31-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5b31-131">-Name</span></span>
<span data-ttu-id="c5b31-132">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c5b31-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c5b31-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b31-133">-ResourceGroupName</span></span>
<span data-ttu-id="c5b31-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5b31-134">Name of resource group.</span></span>

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

### <span data-ttu-id="c5b31-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5b31-135">-ResourceId</span></span>
<span data-ttu-id="c5b31-136">Identyfikator zasobu (ResourceId).</span><span class="sxs-lookup"><span data-stu-id="c5b31-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c5b31-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b31-137">-WhatIf</span></span>
<span data-ttu-id="c5b31-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5b31-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b31-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c5b31-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b31-140">CommonParameters</span></span>
<span data-ttu-id="c5b31-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b31-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5b31-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b31-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5b31-143">INPUTS</span></span>

### <span data-ttu-id="c5b31-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c5b31-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c5b31-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5b31-145">OUTPUTS</span></span>

### <span data-ttu-id="c5b31-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c5b31-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c5b31-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5b31-147">NOTES</span></span>

## <span data-ttu-id="c5b31-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5b31-148">RELATED LINKS</span></span>
