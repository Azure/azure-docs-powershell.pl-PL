---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983617"
---
# <span data-ttu-id="cbbf1-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="cbbf1-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="cbbf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbf1-103">Pobiera przepływność wykresu Gremlin Graph dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="cbbf1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cbbf1-104">SYNTAX</span></span>

### <span data-ttu-id="cbbf1-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cbbf1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbf1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbbf1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbbf1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cbbf1-107">DESCRIPTION</span></span>
<span data-ttu-id="cbbf1-108">Polecenie **cmdlet Get-AzCosmosDBGremlinGraphThroughput** uzyskuje przepływność dla wykresu Gremlin Graph dla usługi Get-AzCosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="cbbf1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cbbf1-109">EXAMPLES</span></span>

### <span data-ttu-id="cbbf1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbbf1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="cbbf1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbbf1-111">PARAMETERS</span></span>

### <span data-ttu-id="cbbf1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cbbf1-112">-AccountName</span></span>
<span data-ttu-id="cbbf1-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cbbf1-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cbbf1-114">-Confirm</span></span>
<span data-ttu-id="cbbf1-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbbf1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cbbf1-116">-DatabaseName</span></span>
<span data-ttu-id="cbbf1-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-117">Database name.</span></span>

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

### <span data-ttu-id="cbbf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbf1-118">-DefaultProfile</span></span>
<span data-ttu-id="cbbf1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbbf1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbbf1-120">-InputObject</span></span>
<span data-ttu-id="cbbf1-121">Obiekt Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbbf1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cbbf1-122">-Name</span></span>
<span data-ttu-id="cbbf1-123">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="cbbf1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbbf1-124">-ResourceGroupName</span></span>
<span data-ttu-id="cbbf1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="cbbf1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbbf1-126">-WhatIf</span></span>
<span data-ttu-id="cbbf1-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbbf1-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbbf1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbf1-129">CommonParameters</span></span>
<span data-ttu-id="cbbf1-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbf1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbbf1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbf1-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbbf1-132">INPUTS</span></span>

### <span data-ttu-id="cbbf1-133">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="cbbf1-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="cbbf1-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbbf1-134">OUTPUTS</span></span>

### <span data-ttu-id="cbbf1-135">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cbbf1-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cbbf1-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cbbf1-136">NOTES</span></span>

## <span data-ttu-id="cbbf1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbbf1-137">RELATED LINKS</span></span>
