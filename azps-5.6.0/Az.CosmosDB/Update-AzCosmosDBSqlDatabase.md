---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1bfb0ec8392c0ddcce20db839f1817688e8feb7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977201"
---
# <span data-ttu-id="07751-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07751-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="07751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07751-102">SYNOPSIS</span></span>
<span data-ttu-id="07751-103">Aktualizuje bazę danych SqlsDB.</span><span class="sxs-lookup"><span data-stu-id="07751-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="07751-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="07751-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="07751-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07751-105">SYNTAX</span></span>

### <span data-ttu-id="07751-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="07751-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07751-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07751-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07751-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07751-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07751-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="07751-109">DESCRIPTION</span></span>
<span data-ttu-id="07751-110">Aktualizuje bazę danych SqlsDB.</span><span class="sxs-lookup"><span data-stu-id="07751-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="07751-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="07751-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="07751-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07751-112">EXAMPLES</span></span>

### <span data-ttu-id="07751-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07751-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="07751-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07751-114">PARAMETERS</span></span>

### <span data-ttu-id="07751-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07751-115">-AccountName</span></span>
<span data-ttu-id="07751-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="07751-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="07751-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="07751-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="07751-118">Wartość maksymalnej przepływności, jeśli jest włączona funkcja automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="07751-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="07751-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07751-119">-Confirm</span></span>
<span data-ttu-id="07751-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="07751-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07751-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07751-121">-DefaultProfile</span></span>
<span data-ttu-id="07751-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="07751-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07751-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07751-123">-InputObject</span></span>
<span data-ttu-id="07751-124">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="07751-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07751-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="07751-125">-Name</span></span>
<span data-ttu-id="07751-126">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="07751-126">Database name.</span></span>

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

### <span data-ttu-id="07751-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="07751-127">-ParentObject</span></span>
<span data-ttu-id="07751-128">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="07751-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="07751-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07751-129">-ResourceGroupName</span></span>
<span data-ttu-id="07751-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="07751-130">Name of resource group.</span></span>

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

### <span data-ttu-id="07751-131">— Przepływność</span><span class="sxs-lookup"><span data-stu-id="07751-131">-Throughput</span></span>
<span data-ttu-id="07751-132">Przepływność baz danych SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="07751-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="07751-133">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="07751-133">Default value is 400.</span></span>

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

### <span data-ttu-id="07751-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07751-134">-WhatIf</span></span>
<span data-ttu-id="07751-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07751-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07751-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="07751-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07751-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07751-137">CommonParameters</span></span>
<span data-ttu-id="07751-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07751-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07751-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07751-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07751-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07751-140">INPUTS</span></span>

### <span data-ttu-id="07751-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="07751-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="07751-142">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="07751-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="07751-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07751-143">OUTPUTS</span></span>

### <span data-ttu-id="07751-144">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="07751-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="07751-145">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="07751-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="07751-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07751-146">NOTES</span></span>

## <span data-ttu-id="07751-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07751-147">RELATED LINKS</span></span>
