---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372379"
---
# <span data-ttu-id="e541d-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="e541d-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="e541d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e541d-102">SYNOPSIS</span></span>
<span data-ttu-id="e541d-103">Umożliwia zaktualizowanie wartości przepływności wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e541d-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="e541d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e541d-104">SYNTAX</span></span>

### <span data-ttu-id="e541d-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e541d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e541d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e541d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e541d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e541d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e541d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e541d-108">DESCRIPTION</span></span>
<span data-ttu-id="e541d-109">Umożliwia zaktualizowanie wartości przepływności wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e541d-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="e541d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e541d-110">EXAMPLES</span></span>

### <span data-ttu-id="e541d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e541d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e541d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e541d-112">PARAMETERS</span></span>

### <span data-ttu-id="e541d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e541d-113">-AccountName</span></span>
<span data-ttu-id="e541d-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e541d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e541d-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e541d-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e541d-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="e541d-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e541d-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e541d-117">-Confirm</span></span>
<span data-ttu-id="e541d-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e541d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e541d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e541d-119">-DatabaseName</span></span>
<span data-ttu-id="e541d-120">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e541d-120">Database name.</span></span>

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

### <span data-ttu-id="e541d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e541d-121">-DefaultProfile</span></span>
<span data-ttu-id="e541d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e541d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e541d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e541d-123">-InputObject</span></span>
<span data-ttu-id="e541d-124">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e541d-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="e541d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e541d-125">-Name</span></span>
<span data-ttu-id="e541d-126">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e541d-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="e541d-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e541d-127">-ParentObject</span></span>
<span data-ttu-id="e541d-128">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e541d-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="e541d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e541d-129">-ResourceGroupName</span></span>
<span data-ttu-id="e541d-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e541d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e541d-131">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="e541d-131">-Throughput</span></span>
<span data-ttu-id="e541d-132">Przepływność wykresu Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e541d-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="e541d-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="e541d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="e541d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e541d-134">-WhatIf</span></span>
<span data-ttu-id="e541d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e541d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e541d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e541d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e541d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e541d-137">CommonParameters</span></span>
<span data-ttu-id="e541d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e541d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e541d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e541d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e541d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e541d-140">INPUTS</span></span>

### <span data-ttu-id="e541d-141">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e541d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="e541d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e541d-142">OUTPUTS</span></span>

### <span data-ttu-id="e541d-143">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e541d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e541d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e541d-144">NOTES</span></span>

## <span data-ttu-id="e541d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e541d-145">RELATED LINKS</span></span>
