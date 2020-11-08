---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051149"
---
# <span data-ttu-id="0d759-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="0d759-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="0d759-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d759-102">SYNOPSIS</span></span>
<span data-ttu-id="0d759-103">Umożliwia zaktualizowanie wartości przepływności wykresu Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0d759-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0d759-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d759-104">SYNTAX</span></span>

### <span data-ttu-id="0d759-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d759-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d759-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d759-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d759-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d759-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d759-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d759-108">EXAMPLES</span></span>

### <span data-ttu-id="0d759-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d759-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="0d759-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d759-110">PARAMETERS</span></span>

### <span data-ttu-id="0d759-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0d759-111">-AccountName</span></span>
<span data-ttu-id="0d759-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0d759-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0d759-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d759-113">-Confirm</span></span>
<span data-ttu-id="0d759-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d759-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d759-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d759-115">-DatabaseName</span></span>
<span data-ttu-id="0d759-116">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0d759-116">Database name.</span></span>

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

### <span data-ttu-id="0d759-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d759-117">-DefaultProfile</span></span>
<span data-ttu-id="0d759-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d759-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d759-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d759-119">-InputObject</span></span>
<span data-ttu-id="0d759-120">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0d759-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="0d759-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d759-121">-Name</span></span>
<span data-ttu-id="0d759-122">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0d759-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="0d759-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="0d759-123">-ParentObject</span></span>
<span data-ttu-id="0d759-124">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="0d759-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="0d759-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d759-125">-ResourceGroupName</span></span>
<span data-ttu-id="0d759-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d759-126">Name of resource group.</span></span>

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

### <span data-ttu-id="0d759-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="0d759-127">-Throughput</span></span>
<span data-ttu-id="0d759-128">Przepływność wykresu Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0d759-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="0d759-129">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="0d759-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d759-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d759-130">-WhatIf</span></span>
<span data-ttu-id="0d759-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d759-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d759-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d759-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d759-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d759-133">CommonParameters</span></span>
<span data-ttu-id="0d759-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d759-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d759-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d759-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d759-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d759-136">INPUTS</span></span>

### <span data-ttu-id="0d759-137">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0d759-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="0d759-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d759-138">OUTPUTS</span></span>

### <span data-ttu-id="0d759-139">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0d759-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0d759-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d759-140">NOTES</span></span>

## <span data-ttu-id="0d759-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d759-141">RELATED LINKS</span></span>
