---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181291"
---
# <span data-ttu-id="74bdb-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="74bdb-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="74bdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="74bdb-103">Aktualizuje bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="74bdb-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="74bdb-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="74bdb-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="74bdb-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74bdb-105">SYNTAX</span></span>

### <span data-ttu-id="74bdb-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="74bdb-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74bdb-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74bdb-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74bdb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74bdb-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74bdb-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="74bdb-109">DESCRIPTION</span></span>
<span data-ttu-id="74bdb-110">Aktualizuje bazę danych GrysDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="74bdb-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="74bdb-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="74bdb-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="74bdb-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74bdb-112">EXAMPLES</span></span>

### <span data-ttu-id="74bdb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74bdb-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="74bdb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74bdb-114">PARAMETERS</span></span>

### <span data-ttu-id="74bdb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74bdb-115">-AccountName</span></span>
<span data-ttu-id="74bdb-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="74bdb-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74bdb-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="74bdb-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="74bdb-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="74bdb-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="74bdb-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74bdb-119">-Confirm</span></span>
<span data-ttu-id="74bdb-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74bdb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74bdb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bdb-121">-DefaultProfile</span></span>
<span data-ttu-id="74bdb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74bdb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74bdb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74bdb-123">-InputObject</span></span>
<span data-ttu-id="74bdb-124">Obiekt Bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="74bdb-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="74bdb-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74bdb-125">-Name</span></span>
<span data-ttu-id="74bdb-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="74bdb-126">Database name.</span></span>

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

### <span data-ttu-id="74bdb-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="74bdb-127">-ParentObject</span></span>
<span data-ttu-id="74bdb-128">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="74bdb-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="74bdb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74bdb-129">-ResourceGroupName</span></span>
<span data-ttu-id="74bdb-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74bdb-130">Name of resource group.</span></span>

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

### <span data-ttu-id="74bdb-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="74bdb-131">-Throughput</span></span>
<span data-ttu-id="74bdb-132">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="74bdb-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="74bdb-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="74bdb-133">Default value is 400.</span></span>

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

### <span data-ttu-id="74bdb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74bdb-134">-WhatIf</span></span>
<span data-ttu-id="74bdb-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74bdb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74bdb-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74bdb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74bdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bdb-137">CommonParameters</span></span>
<span data-ttu-id="74bdb-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74bdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bdb-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74bdb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bdb-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74bdb-140">INPUTS</span></span>

### <span data-ttu-id="74bdb-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="74bdb-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="74bdb-142">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="74bdb-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="74bdb-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74bdb-143">OUTPUTS</span></span>

### <span data-ttu-id="74bdb-144">Microsoft.Azure.Commands.DoceńDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="74bdb-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="74bdb-145">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="74bdb-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="74bdb-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74bdb-146">NOTES</span></span>

## <span data-ttu-id="74bdb-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74bdb-147">RELATED LINKS</span></span>
