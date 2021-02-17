---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177322"
---
# <span data-ttu-id="34ab5-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="34ab5-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="34ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="34ab5-103">Pobiera przepływność wykresu Gremlin Graph dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="34ab5-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="34ab5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34ab5-104">SYNTAX</span></span>

### <span data-ttu-id="34ab5-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="34ab5-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ab5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34ab5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34ab5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="34ab5-107">DESCRIPTION</span></span>
<span data-ttu-id="34ab5-108">Polecenie **cmdlet Get-AzCosmosDBGremlinGraphThroughput** uzyskuje przepływność dla wykresu Gremlin Graph dla usługi Get-AzCosmosDB.</span><span class="sxs-lookup"><span data-stu-id="34ab5-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="34ab5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34ab5-109">EXAMPLES</span></span>

### <span data-ttu-id="34ab5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34ab5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="34ab5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34ab5-111">PARAMETERS</span></span>

### <span data-ttu-id="34ab5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34ab5-112">-AccountName</span></span>
<span data-ttu-id="34ab5-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="34ab5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34ab5-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34ab5-114">-Confirm</span></span>
<span data-ttu-id="34ab5-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34ab5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ab5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34ab5-116">-DatabaseName</span></span>
<span data-ttu-id="34ab5-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="34ab5-117">Database name.</span></span>

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

### <span data-ttu-id="34ab5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ab5-118">-DefaultProfile</span></span>
<span data-ttu-id="34ab5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34ab5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ab5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34ab5-120">-InputObject</span></span>
<span data-ttu-id="34ab5-121">Obiekt Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="34ab5-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="34ab5-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34ab5-122">-Name</span></span>
<span data-ttu-id="34ab5-123">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="34ab5-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="34ab5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ab5-124">-ResourceGroupName</span></span>
<span data-ttu-id="34ab5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34ab5-125">Name of resource group.</span></span>

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

### <span data-ttu-id="34ab5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ab5-126">-WhatIf</span></span>
<span data-ttu-id="34ab5-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ab5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ab5-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34ab5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ab5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ab5-129">CommonParameters</span></span>
<span data-ttu-id="34ab5-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ab5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ab5-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34ab5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ab5-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34ab5-132">INPUTS</span></span>

### <span data-ttu-id="34ab5-133">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="34ab5-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="34ab5-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34ab5-134">OUTPUTS</span></span>

### <span data-ttu-id="34ab5-135">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="34ab5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="34ab5-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34ab5-136">NOTES</span></span>

## <span data-ttu-id="34ab5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34ab5-137">RELATED LINKS</span></span>
