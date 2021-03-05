---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: b65443b2fc8d8b97b4b0598e0bfbb3afb9d1b925
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998838"
---
# <span data-ttu-id="b6d15-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b6d15-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b6d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6d15-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d15-103">Tworzy nową bazę danych GrasDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b6d15-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b6d15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6d15-104">SYNTAX</span></span>

### <span data-ttu-id="b6d15-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b6d15-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d15-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6d15-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6d15-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6d15-107">DESCRIPTION</span></span>
<span data-ttu-id="b6d15-108">Tworzy nową bazę danych GrasDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b6d15-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b6d15-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6d15-109">EXAMPLES</span></span>

### <span data-ttu-id="b6d15-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6d15-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="b6d15-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6d15-111">PARAMETERS</span></span>

### <span data-ttu-id="b6d15-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6d15-112">-AccountName</span></span>
<span data-ttu-id="b6d15-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="b6d15-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b6d15-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b6d15-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b6d15-115">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="b6d15-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b6d15-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6d15-116">-Confirm</span></span>
<span data-ttu-id="b6d15-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6d15-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6d15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d15-118">-DefaultProfile</span></span>
<span data-ttu-id="b6d15-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6d15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d15-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6d15-120">-Name</span></span>
<span data-ttu-id="b6d15-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b6d15-121">Database name.</span></span>

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

### <span data-ttu-id="b6d15-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="b6d15-122">-ParentObject</span></span>
<span data-ttu-id="b6d15-123">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="b6d15-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6d15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d15-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6d15-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6d15-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b6d15-126">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="b6d15-126">-Throughput</span></span>
<span data-ttu-id="b6d15-127">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b6d15-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="b6d15-128">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="b6d15-128">Default value is 400.</span></span>

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

### <span data-ttu-id="b6d15-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d15-129">-WhatIf</span></span>
<span data-ttu-id="b6d15-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6d15-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6d15-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b6d15-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6d15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d15-132">CommonParameters</span></span>
<span data-ttu-id="b6d15-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d15-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6d15-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d15-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6d15-135">INPUTS</span></span>

### <span data-ttu-id="b6d15-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b6d15-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b6d15-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6d15-137">OUTPUTS</span></span>

### <span data-ttu-id="b6d15-138">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b6d15-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b6d15-139">Microsoft.Azure.Commands.DoceńDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b6d15-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b6d15-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6d15-140">NOTES</span></span>

## <span data-ttu-id="b6d15-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6d15-141">RELATED LINKS</span></span>
