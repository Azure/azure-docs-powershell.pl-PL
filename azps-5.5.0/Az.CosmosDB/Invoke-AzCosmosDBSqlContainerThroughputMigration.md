---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: ac15f6ba4d8db1e4f3ab35c34b33b78fdefa05a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177315"
---
# <span data-ttu-id="ddb00-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="ddb00-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="ddb00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb00-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb00-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="ddb00-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="ddb00-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddb00-104">SYNTAX</span></span>

### <span data-ttu-id="ddb00-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ddb00-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb00-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb00-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb00-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb00-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddb00-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddb00-108">DESCRIPTION</span></span>
<span data-ttu-id="ddb00-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="ddb00-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="ddb00-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddb00-110">EXAMPLES</span></span>

### <span data-ttu-id="ddb00-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ddb00-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="ddb00-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb00-112">PARAMETERS</span></span>

### <span data-ttu-id="ddb00-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ddb00-113">-AccountName</span></span>
<span data-ttu-id="ddb00-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="ddb00-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ddb00-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddb00-115">-Confirm</span></span>
<span data-ttu-id="ddb00-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddb00-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb00-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddb00-117">-DatabaseName</span></span>
<span data-ttu-id="ddb00-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ddb00-118">Database name.</span></span>

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

### <span data-ttu-id="ddb00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb00-119">-DefaultProfile</span></span>
<span data-ttu-id="ddb00-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb00-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddb00-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddb00-121">-InputObject</span></span>
<span data-ttu-id="ddb00-122">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="ddb00-122">Sql Container object.</span></span>

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

### <span data-ttu-id="ddb00-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddb00-123">-Name</span></span>
<span data-ttu-id="ddb00-124">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="ddb00-124">Container name.</span></span>

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

### <span data-ttu-id="ddb00-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddb00-125">-ParentObject</span></span>
<span data-ttu-id="ddb00-126">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="ddb00-126">Sql Database object.</span></span>

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

### <span data-ttu-id="ddb00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb00-127">-ResourceGroupName</span></span>
<span data-ttu-id="ddb00-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ddb00-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ddb00-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="ddb00-129">-ThroughputType</span></span>
<span data-ttu-id="ddb00-130">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="ddb00-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="ddb00-131">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="ddb00-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="ddb00-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb00-132">-WhatIf</span></span>
<span data-ttu-id="ddb00-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddb00-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddb00-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddb00-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb00-135">CommonParameters</span></span>
<span data-ttu-id="ddb00-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb00-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddb00-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb00-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddb00-138">INPUTS</span></span>

### <span data-ttu-id="ddb00-139">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ddb00-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ddb00-140">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ddb00-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="ddb00-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddb00-141">OUTPUTS</span></span>

### <span data-ttu-id="ddb00-142">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ddb00-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ddb00-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddb00-143">NOTES</span></span>

## <span data-ttu-id="ddb00-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddb00-144">RELATED LINKS</span></span>
