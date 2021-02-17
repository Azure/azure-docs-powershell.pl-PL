---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 4e17e8fc2ee3b9fa82881387fa4422616b25551c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196874"
---
# <span data-ttu-id="32b79-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="32b79-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="32b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b79-102">SYNOPSIS</span></span>
<span data-ttu-id="32b79-103">Skorzystaj z tej funkcji, aby przeprowadzić migrację przepływności automatycznego skalowania do przepływności ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="32b79-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="32b79-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="32b79-104">SYNTAX</span></span>

### <span data-ttu-id="32b79-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="32b79-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b79-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32b79-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b79-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32b79-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b79-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="32b79-108">DESCRIPTION</span></span>
<span data-ttu-id="32b79-109">Paramter ThroughpyteType definiuje przepływność, do której ma zostać migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="32b79-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="32b79-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="32b79-110">EXAMPLES</span></span>

### <span data-ttu-id="32b79-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32b79-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="32b79-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32b79-112">PARAMETERS</span></span>

### <span data-ttu-id="32b79-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="32b79-113">-AccountName</span></span>
<span data-ttu-id="32b79-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="32b79-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="32b79-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32b79-115">-Confirm</span></span>
<span data-ttu-id="32b79-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="32b79-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b79-117">-DefaultProfile</span></span>
<span data-ttu-id="32b79-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="32b79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b79-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32b79-119">-InputObject</span></span>
<span data-ttu-id="32b79-120">Obiekt Cassandra Table.</span><span class="sxs-lookup"><span data-stu-id="32b79-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="32b79-121">-KeyspaceName</span></span>
<span data-ttu-id="32b79-122">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="32b79-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="32b79-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="32b79-123">-Name</span></span>
<span data-ttu-id="32b79-124">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="32b79-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="32b79-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="32b79-125">-ParentObject</span></span>
<span data-ttu-id="32b79-126">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="32b79-126">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b79-127">-ResourceGroupName</span></span>
<span data-ttu-id="32b79-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32b79-128">Name of resource group.</span></span>

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

### <span data-ttu-id="32b79-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="32b79-129">-ThroughputType</span></span>
<span data-ttu-id="32b79-130">Typ przepływności, do jakiego ma być migrowana migracja.</span><span class="sxs-lookup"><span data-stu-id="32b79-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="32b79-131">Możliwe wartości to: Automatyczne skalowanie, Ręczne.</span><span class="sxs-lookup"><span data-stu-id="32b79-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="32b79-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b79-132">-WhatIf</span></span>
<span data-ttu-id="32b79-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b79-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b79-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="32b79-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b79-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b79-135">CommonParameters</span></span>
<span data-ttu-id="32b79-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b79-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b79-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32b79-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b79-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32b79-138">INPUTS</span></span>

### <span data-ttu-id="32b79-139">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="32b79-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="32b79-140">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="32b79-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="32b79-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32b79-141">OUTPUTS</span></span>

### <span data-ttu-id="32b79-142">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="32b79-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="32b79-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="32b79-143">NOTES</span></span>

## <span data-ttu-id="32b79-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32b79-144">RELATED LINKS</span></span>
