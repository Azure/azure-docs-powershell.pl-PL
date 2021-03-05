---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: a223fd71ecf65ecb34b605e79ee0d6f7670d3a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977361"
---
# <span data-ttu-id="2f103-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="2f103-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="2f103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f103-102">SYNOPSIS</span></span>
<span data-ttu-id="2f103-103">Aktualizuje bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2f103-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="2f103-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="2f103-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="2f103-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f103-105">SYNTAX</span></span>

### <span data-ttu-id="2f103-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2f103-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f103-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f103-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f103-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f103-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f103-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f103-109">DESCRIPTION</span></span>
<span data-ttu-id="2f103-110">Aktualizuje bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2f103-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="2f103-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="2f103-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="2f103-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f103-112">EXAMPLES</span></span>

### <span data-ttu-id="2f103-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f103-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="2f103-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f103-114">PARAMETERS</span></span>

### <span data-ttu-id="2f103-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2f103-115">-AccountName</span></span>
<span data-ttu-id="2f103-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="2f103-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2f103-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2f103-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2f103-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="2f103-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2f103-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f103-119">-Confirm</span></span>
<span data-ttu-id="2f103-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f103-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f103-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f103-121">-DefaultProfile</span></span>
<span data-ttu-id="2f103-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f103-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f103-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f103-123">-InputObject</span></span>
<span data-ttu-id="2f103-124">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2f103-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f103-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2f103-125">-Name</span></span>
<span data-ttu-id="2f103-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2f103-126">Database name.</span></span>

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

### <span data-ttu-id="2f103-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="2f103-127">-ParentObject</span></span>
<span data-ttu-id="2f103-128">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="2f103-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2f103-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f103-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f103-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f103-130">Name of resource group.</span></span>

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

### <span data-ttu-id="2f103-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="2f103-131">-Throughput</span></span>
<span data-ttu-id="2f103-132">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="2f103-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="2f103-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="2f103-133">Default value is 400.</span></span>

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

### <span data-ttu-id="2f103-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f103-134">-WhatIf</span></span>
<span data-ttu-id="2f103-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f103-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f103-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2f103-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f103-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f103-137">CommonParameters</span></span>
<span data-ttu-id="2f103-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f103-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f103-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f103-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f103-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f103-140">INPUTS</span></span>

### <span data-ttu-id="2f103-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2f103-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="2f103-142">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2f103-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="2f103-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f103-143">OUTPUTS</span></span>

### <span data-ttu-id="2f103-144">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2f103-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2f103-145">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2f103-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2f103-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f103-146">NOTES</span></span>

## <span data-ttu-id="2f103-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f103-147">RELATED LINKS</span></span>
