---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 15ee57c32d8eeeca996994900113360adac1c407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177307"
---
# <span data-ttu-id="f6915-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="f6915-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="f6915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6915-102">SYNOPSIS</span></span>
<span data-ttu-id="f6915-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="f6915-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="f6915-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6915-104">SYNTAX</span></span>

### <span data-ttu-id="f6915-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f6915-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6915-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6915-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6915-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6915-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6915-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6915-108">DESCRIPTION</span></span>
<span data-ttu-id="f6915-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="f6915-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="f6915-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6915-110">EXAMPLES</span></span>

### <span data-ttu-id="f6915-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6915-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="f6915-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6915-112">PARAMETERS</span></span>

### <span data-ttu-id="f6915-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f6915-113">-AccountName</span></span>
<span data-ttu-id="f6915-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="f6915-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f6915-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6915-115">-Confirm</span></span>
<span data-ttu-id="f6915-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f6915-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6915-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6915-117">-DefaultProfile</span></span>
<span data-ttu-id="f6915-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6915-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6915-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6915-119">-InputObject</span></span>
<span data-ttu-id="f6915-120">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="f6915-120">Sql Database object.</span></span>

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

### <span data-ttu-id="f6915-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f6915-121">-Name</span></span>
<span data-ttu-id="f6915-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f6915-122">Database name.</span></span>

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

### <span data-ttu-id="f6915-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="f6915-123">-ParentObject</span></span>
<span data-ttu-id="f6915-124">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="f6915-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f6915-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6915-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6915-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6915-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f6915-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="f6915-127">-ThroughputType</span></span>
<span data-ttu-id="f6915-128">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="f6915-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="f6915-129">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="f6915-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="f6915-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6915-130">-WhatIf</span></span>
<span data-ttu-id="f6915-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6915-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6915-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f6915-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6915-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6915-133">CommonParameters</span></span>
<span data-ttu-id="f6915-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6915-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6915-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6915-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6915-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6915-136">INPUTS</span></span>

### <span data-ttu-id="f6915-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="f6915-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="f6915-138">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f6915-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f6915-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6915-139">OUTPUTS</span></span>

### <span data-ttu-id="f6915-140">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f6915-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f6915-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6915-141">NOTES</span></span>

## <span data-ttu-id="f6915-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6915-142">RELATED LINKS</span></span>
