---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: c502040c2d4b11302c158cffb66bf6fd01e148ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996857"
---
# <span data-ttu-id="395dd-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="395dd-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="395dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395dd-102">SYNOPSIS</span></span>
<span data-ttu-id="395dd-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="395dd-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="395dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="395dd-104">SYNTAX</span></span>

### <span data-ttu-id="395dd-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="395dd-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395dd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="395dd-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395dd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="395dd-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="395dd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="395dd-108">DESCRIPTION</span></span>
<span data-ttu-id="395dd-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="395dd-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="395dd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="395dd-110">EXAMPLES</span></span>

### <span data-ttu-id="395dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="395dd-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="395dd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="395dd-112">PARAMETERS</span></span>

### <span data-ttu-id="395dd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="395dd-113">-AccountName</span></span>
<span data-ttu-id="395dd-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="395dd-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="395dd-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="395dd-115">-Confirm</span></span>
<span data-ttu-id="395dd-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="395dd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395dd-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="395dd-117">-DatabaseName</span></span>
<span data-ttu-id="395dd-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="395dd-118">Database name.</span></span>

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

### <span data-ttu-id="395dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395dd-119">-DefaultProfile</span></span>
<span data-ttu-id="395dd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="395dd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395dd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="395dd-121">-InputObject</span></span>
<span data-ttu-id="395dd-122">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="395dd-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="395dd-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="395dd-123">-Name</span></span>
<span data-ttu-id="395dd-124">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="395dd-124">Container name.</span></span>

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

### <span data-ttu-id="395dd-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="395dd-125">-ParentObject</span></span>
<span data-ttu-id="395dd-126">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="395dd-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="395dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="395dd-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="395dd-128">Name of resource group.</span></span>

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

### <span data-ttu-id="395dd-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="395dd-129">-ThroughputType</span></span>
<span data-ttu-id="395dd-130">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="395dd-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="395dd-131">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="395dd-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="395dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395dd-132">-WhatIf</span></span>
<span data-ttu-id="395dd-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="395dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395dd-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="395dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395dd-135">CommonParameters</span></span>
<span data-ttu-id="395dd-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395dd-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="395dd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395dd-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="395dd-138">INPUTS</span></span>

### <span data-ttu-id="395dd-139">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="395dd-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="395dd-140">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="395dd-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="395dd-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="395dd-141">OUTPUTS</span></span>

### <span data-ttu-id="395dd-142">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="395dd-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="395dd-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="395dd-143">NOTES</span></span>

## <span data-ttu-id="395dd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="395dd-144">RELATED LINKS</span></span>
