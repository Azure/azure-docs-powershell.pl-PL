---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501772"
---
# <span data-ttu-id="9ec56-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="9ec56-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="9ec56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ec56-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec56-103">Pobiera przepływność wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9ec56-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="9ec56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ec56-104">SYNTAX</span></span>

### <span data-ttu-id="9ec56-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ec56-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec56-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec56-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec56-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ec56-107">DESCRIPTION</span></span>
<span data-ttu-id="9ec56-108">Polecenie cmdlet **Get-AzCosmosDBGremlinGraphThroughput** pobiera przepływność wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9ec56-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="9ec56-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ec56-109">EXAMPLES</span></span>

### <span data-ttu-id="9ec56-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ec56-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="9ec56-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ec56-111">PARAMETERS</span></span>

### <span data-ttu-id="9ec56-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ec56-112">-AccountName</span></span>
<span data-ttu-id="9ec56-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9ec56-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9ec56-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ec56-114">-Confirm</span></span>
<span data-ttu-id="9ec56-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec56-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec56-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ec56-116">-DatabaseName</span></span>
<span data-ttu-id="9ec56-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9ec56-117">Database name.</span></span>

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

### <span data-ttu-id="9ec56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec56-118">-DefaultProfile</span></span>
<span data-ttu-id="9ec56-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ec56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ec56-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ec56-120">-InputObject</span></span>
<span data-ttu-id="9ec56-121">Obiekt wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9ec56-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="9ec56-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ec56-122">-Name</span></span>
<span data-ttu-id="9ec56-123">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9ec56-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="9ec56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec56-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ec56-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ec56-125">Name of resource group.</span></span>

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

### <span data-ttu-id="9ec56-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec56-126">-WhatIf</span></span>
<span data-ttu-id="9ec56-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec56-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec56-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ec56-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec56-129">CommonParameters</span></span>
<span data-ttu-id="9ec56-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec56-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ec56-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec56-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ec56-132">INPUTS</span></span>

### <span data-ttu-id="9ec56-133">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="9ec56-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="9ec56-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ec56-134">OUTPUTS</span></span>

### <span data-ttu-id="9ec56-135">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9ec56-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9ec56-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ec56-136">NOTES</span></span>

## <span data-ttu-id="9ec56-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ec56-137">RELATED LINKS</span></span>
