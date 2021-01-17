---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345997"
---
# <span data-ttu-id="c7c6e-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c7c6e-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="c7c6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c6e-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c7c6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7c6e-104">SYNTAX</span></span>

### <span data-ttu-id="c7c6e-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c7c6e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c6e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c6e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c6e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c6e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c6e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c7c6e-108">DESCRIPTION</span></span>
<span data-ttu-id="c7c6e-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c7c6e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7c6e-110">EXAMPLES</span></span>

### <span data-ttu-id="c7c6e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7c6e-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="c7c6e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7c6e-112">PARAMETERS</span></span>

### <span data-ttu-id="c7c6e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c7c6e-113">-AccountName</span></span>
<span data-ttu-id="c7c6e-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c7c6e-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7c6e-115">-Confirm</span></span>
<span data-ttu-id="c7c6e-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c6e-117">-DefaultProfile</span></span>
<span data-ttu-id="c7c6e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c6e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7c6e-119">-InputObject</span></span>
<span data-ttu-id="c7c6e-120">Obiekt tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="c7c6e-121">-Spacename</span><span class="sxs-lookup"><span data-stu-id="c7c6e-121">-KeyspaceName</span></span>
<span data-ttu-id="c7c6e-122">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c7c6e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7c6e-123">-Name</span></span>
<span data-ttu-id="c7c6e-124">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c7c6e-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="c7c6e-125">-ParentObject</span></span>
<span data-ttu-id="c7c6e-126">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c7c6e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c6e-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7c6e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c7c6e-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="c7c6e-129">-ThroughputType</span></span>
<span data-ttu-id="c7c6e-130">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="c7c6e-131">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c7c6e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c6e-132">-WhatIf</span></span>
<span data-ttu-id="c7c6e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c6e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c6e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c6e-135">CommonParameters</span></span>
<span data-ttu-id="c7c6e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c6e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c6e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7c6e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c6e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7c6e-138">INPUTS</span></span>

### <span data-ttu-id="c7c6e-139">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c7c6e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c7c6e-140">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="c7c6e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="c7c6e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7c6e-141">OUTPUTS</span></span>

### <span data-ttu-id="c7c6e-142">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c7c6e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c7c6e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7c6e-143">NOTES</span></span>

## <span data-ttu-id="c7c6e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7c6e-144">RELATED LINKS</span></span>
