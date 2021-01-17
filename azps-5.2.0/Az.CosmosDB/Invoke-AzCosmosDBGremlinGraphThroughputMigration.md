---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343477"
---
# <span data-ttu-id="2a5b8-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2a5b8-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="2a5b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5b8-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2a5b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a5b8-104">SYNTAX</span></span>

### <span data-ttu-id="2a5b8-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a5b8-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a5b8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5b8-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a5b8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5b8-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a5b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2a5b8-108">DESCRIPTION</span></span>
<span data-ttu-id="2a5b8-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2a5b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a5b8-110">EXAMPLES</span></span>

### <span data-ttu-id="2a5b8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a5b8-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="2a5b8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a5b8-112">PARAMETERS</span></span>

### <span data-ttu-id="2a5b8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a5b8-113">-AccountName</span></span>
<span data-ttu-id="2a5b8-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2a5b8-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a5b8-115">-Confirm</span></span>
<span data-ttu-id="2a5b8-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a5b8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a5b8-117">-DatabaseName</span></span>
<span data-ttu-id="2a5b8-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-118">Database name.</span></span>

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

### <span data-ttu-id="2a5b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5b8-119">-DefaultProfile</span></span>
<span data-ttu-id="2a5b8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a5b8-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a5b8-121">-InputObject</span></span>
<span data-ttu-id="2a5b8-122">Obiekt wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="2a5b8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a5b8-123">-Name</span></span>
<span data-ttu-id="2a5b8-124">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="2a5b8-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="2a5b8-125">-ParentObject</span></span>
<span data-ttu-id="2a5b8-126">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="2a5b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a5b8-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2a5b8-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="2a5b8-129">-ThroughputType</span></span>
<span data-ttu-id="2a5b8-130">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="2a5b8-131">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-131">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a5b8-132">-WhatIf</span></span>
<span data-ttu-id="2a5b8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a5b8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a5b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5b8-135">CommonParameters</span></span>
<span data-ttu-id="2a5b8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5b8-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a5b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5b8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a5b8-138">INPUTS</span></span>

### <span data-ttu-id="2a5b8-139">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2a5b8-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2a5b8-140">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="2a5b8-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="2a5b8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a5b8-141">OUTPUTS</span></span>

### <span data-ttu-id="2a5b8-142">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2a5b8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2a5b8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a5b8-143">NOTES</span></span>

## <span data-ttu-id="2a5b8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a5b8-144">RELATED LINKS</span></span>
