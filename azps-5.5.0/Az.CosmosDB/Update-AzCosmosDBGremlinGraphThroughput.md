---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181251"
---
# <span data-ttu-id="f2079-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="f2079-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="f2079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2079-102">SYNOPSIS</span></span>
<span data-ttu-id="f2079-103">Aktualizuje wartość przepływności wykresu Gremlin Graph dla grysdb.</span><span class="sxs-lookup"><span data-stu-id="f2079-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f2079-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2079-104">SYNTAX</span></span>

### <span data-ttu-id="f2079-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f2079-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2079-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2079-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2079-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2079-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2079-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2079-108">DESCRIPTION</span></span>
<span data-ttu-id="f2079-109">Aktualizuje wartość przepływności wykresu Gremlin Graph dla grysdb.</span><span class="sxs-lookup"><span data-stu-id="f2079-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f2079-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2079-110">EXAMPLES</span></span>

### <span data-ttu-id="f2079-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2079-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="f2079-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2079-112">PARAMETERS</span></span>

### <span data-ttu-id="f2079-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2079-113">-AccountName</span></span>
<span data-ttu-id="f2079-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="f2079-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f2079-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f2079-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f2079-116">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="f2079-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f2079-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2079-117">-Confirm</span></span>
<span data-ttu-id="f2079-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2079-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2079-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2079-119">-DatabaseName</span></span>
<span data-ttu-id="f2079-120">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f2079-120">Database name.</span></span>

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

### <span data-ttu-id="f2079-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2079-121">-DefaultProfile</span></span>
<span data-ttu-id="f2079-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2079-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2079-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2079-123">-InputObject</span></span>
<span data-ttu-id="f2079-124">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f2079-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f2079-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2079-125">-Name</span></span>
<span data-ttu-id="f2079-126">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f2079-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f2079-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="f2079-127">-ParentObject</span></span>
<span data-ttu-id="f2079-128">Obiekt Gremlin Database.</span><span class="sxs-lookup"><span data-stu-id="f2079-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f2079-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2079-129">-ResourceGroupName</span></span>
<span data-ttu-id="f2079-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2079-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f2079-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="f2079-131">-Throughput</span></span>
<span data-ttu-id="f2079-132">Przepływność wykresu Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f2079-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f2079-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="f2079-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f2079-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2079-134">-WhatIf</span></span>
<span data-ttu-id="f2079-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2079-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2079-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2079-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2079-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2079-137">CommonParameters</span></span>
<span data-ttu-id="f2079-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2079-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2079-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2079-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2079-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2079-140">INPUTS</span></span>

### <span data-ttu-id="f2079-141">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f2079-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f2079-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2079-142">OUTPUTS</span></span>

### <span data-ttu-id="f2079-143">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f2079-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f2079-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2079-144">NOTES</span></span>

## <span data-ttu-id="f2079-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2079-145">RELATED LINKS</span></span>
