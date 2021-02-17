---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177226"
---
# <span data-ttu-id="01f83-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="01f83-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="01f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01f83-102">SYNOPSIS</span></span>
<span data-ttu-id="01f83-103">Aktualizuj regiony konta AADB.</span><span class="sxs-lookup"><span data-stu-id="01f83-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="01f83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01f83-104">SYNTAX</span></span>

### <span data-ttu-id="01f83-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="01f83-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01f83-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01f83-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f83-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01f83-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f83-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="01f83-108">DESCRIPTION</span></span>
<span data-ttu-id="01f83-109">Aktualizuj regiony konta AADB.</span><span class="sxs-lookup"><span data-stu-id="01f83-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="01f83-110">Lokalizacja może być zapewniana jako obiekt typu PSLocation lub jako ciąg nazwy lokalizacji uporządkowanej według priorytetu trybu failover.</span><span class="sxs-lookup"><span data-stu-id="01f83-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="01f83-111">Parametr LocationObject oczekuje listy bieżących lokalizacji (uwzględnionych priorytetów trybu failover) dołączonych przez nowe lokalizacjeObjects odpowiadające nowym lokalizacjom do dodania.</span><span class="sxs-lookup"><span data-stu-id="01f83-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="01f83-112">Parametr lokalizacji oczekuje listy bieżącej lokalizacji (uporządkowanej według priorytetu trybu failover) i nowych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="01f83-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="01f83-113">Pamiętaj, że obsługujemy tylko dodawanie regionów.</span><span class="sxs-lookup"><span data-stu-id="01f83-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="01f83-114">Podaj lokalizację lub obiekt LocationObject.</span><span class="sxs-lookup"><span data-stu-id="01f83-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="01f83-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01f83-115">EXAMPLES</span></span>

### <span data-ttu-id="01f83-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01f83-116">Example 1</span></span>
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

## <span data-ttu-id="01f83-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01f83-117">PARAMETERS</span></span>

### <span data-ttu-id="01f83-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="01f83-118">-AsJob</span></span>
<span data-ttu-id="01f83-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="01f83-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01f83-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01f83-120">-Confirm</span></span>
<span data-ttu-id="01f83-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01f83-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f83-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f83-122">-DefaultProfile</span></span>
<span data-ttu-id="01f83-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01f83-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01f83-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01f83-124">-InputObject</span></span>
<span data-ttu-id="01f83-125">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="01f83-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="01f83-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="01f83-126">-Location</span></span>
<span data-ttu-id="01f83-127">Nazwa lokalizacji, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="01f83-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="01f83-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="01f83-128">-LocationObject</span></span>
<span data-ttu-id="01f83-129">Dodaj lokalizację do konta bazy danych Db firmy Dos.</span><span class="sxs-lookup"><span data-stu-id="01f83-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="01f83-130">Tablica obiektów PSLocation.</span><span class="sxs-lookup"><span data-stu-id="01f83-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="01f83-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="01f83-131">-Name</span></span>
<span data-ttu-id="01f83-132">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="01f83-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01f83-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f83-133">-ResourceGroupName</span></span>
<span data-ttu-id="01f83-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01f83-134">Name of resource group.</span></span>

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

### <span data-ttu-id="01f83-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01f83-135">-ResourceId</span></span>
<span data-ttu-id="01f83-136">ZasóbId zasobu.</span><span class="sxs-lookup"><span data-stu-id="01f83-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="01f83-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f83-137">-WhatIf</span></span>
<span data-ttu-id="01f83-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01f83-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f83-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="01f83-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f83-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f83-140">CommonParameters</span></span>
<span data-ttu-id="01f83-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f83-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f83-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01f83-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f83-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01f83-143">INPUTS</span></span>

### <span data-ttu-id="01f83-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="01f83-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="01f83-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01f83-145">OUTPUTS</span></span>

### <span data-ttu-id="01f83-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="01f83-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="01f83-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01f83-147">NOTES</span></span>

## <span data-ttu-id="01f83-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01f83-148">RELATED LINKS</span></span>
