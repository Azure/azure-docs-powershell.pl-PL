---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: c5d7bc79185639c4ec79ab14d7ed2f6201dcedb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977322"
---
# <span data-ttu-id="5f55f-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="5f55f-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="5f55f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f55f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f55f-103">Aktualizuje wartość przepływności wykresu Gremlin Graph dla grysdb.</span><span class="sxs-lookup"><span data-stu-id="5f55f-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5f55f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f55f-104">SYNTAX</span></span>

### <span data-ttu-id="5f55f-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5f55f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f55f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f55f-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f55f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f55f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f55f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f55f-108">DESCRIPTION</span></span>
<span data-ttu-id="5f55f-109">Aktualizuje wartość przepływności wykresu Gremlin Graph dla grysdb.</span><span class="sxs-lookup"><span data-stu-id="5f55f-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5f55f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f55f-110">EXAMPLES</span></span>

### <span data-ttu-id="5f55f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f55f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="5f55f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f55f-112">PARAMETERS</span></span>

### <span data-ttu-id="5f55f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f55f-113">-AccountName</span></span>
<span data-ttu-id="5f55f-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="5f55f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5f55f-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5f55f-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5f55f-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="5f55f-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5f55f-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f55f-117">-Confirm</span></span>
<span data-ttu-id="5f55f-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5f55f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f55f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f55f-119">-DatabaseName</span></span>
<span data-ttu-id="5f55f-120">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5f55f-120">Database name.</span></span>

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

### <span data-ttu-id="5f55f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f55f-121">-DefaultProfile</span></span>
<span data-ttu-id="5f55f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f55f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f55f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f55f-123">-InputObject</span></span>
<span data-ttu-id="5f55f-124">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5f55f-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f55f-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5f55f-125">-Name</span></span>
<span data-ttu-id="5f55f-126">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5f55f-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5f55f-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="5f55f-127">-ParentObject</span></span>
<span data-ttu-id="5f55f-128">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5f55f-128">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f55f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f55f-129">-ResourceGroupName</span></span>
<span data-ttu-id="5f55f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f55f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5f55f-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="5f55f-131">-Throughput</span></span>
<span data-ttu-id="5f55f-132">Przepływność wykresu Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5f55f-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="5f55f-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="5f55f-133">Default value is 400.</span></span>

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

### <span data-ttu-id="5f55f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f55f-134">-WhatIf</span></span>
<span data-ttu-id="5f55f-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f55f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f55f-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5f55f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f55f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f55f-137">CommonParameters</span></span>
<span data-ttu-id="5f55f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f55f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f55f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f55f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f55f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f55f-140">INPUTS</span></span>

### <span data-ttu-id="5f55f-141">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5f55f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5f55f-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f55f-142">OUTPUTS</span></span>

### <span data-ttu-id="5f55f-143">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5f55f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5f55f-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f55f-144">NOTES</span></span>

## <span data-ttu-id="5f55f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f55f-145">RELATED LINKS</span></span>
