---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346030"
---
# <span data-ttu-id="e9480-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e9480-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="e9480-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9480-102">SYNOPSIS</span></span>
<span data-ttu-id="e9480-103">Za pomocą tej operacji można migrować przepływność automatycznego skalowania do przepustowości ręcznej i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="e9480-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e9480-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9480-104">SYNTAX</span></span>

### <span data-ttu-id="e9480-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9480-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9480-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9480-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9480-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9480-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9480-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e9480-108">DESCRIPTION</span></span>
<span data-ttu-id="e9480-109">Parametr ThroughpyteType określa przepływność, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="e9480-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e9480-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9480-110">EXAMPLES</span></span>

### <span data-ttu-id="e9480-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9480-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="e9480-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9480-112">PARAMETERS</span></span>

### <span data-ttu-id="e9480-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9480-113">-AccountName</span></span>
<span data-ttu-id="e9480-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e9480-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e9480-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9480-115">-Confirm</span></span>
<span data-ttu-id="e9480-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9480-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9480-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9480-117">-DefaultProfile</span></span>
<span data-ttu-id="e9480-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9480-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9480-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e9480-119">-InputObject</span></span>
<span data-ttu-id="e9480-120">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="e9480-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9480-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9480-121">-Name</span></span>
<span data-ttu-id="e9480-122">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="e9480-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e9480-123">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e9480-123">-ParentObject</span></span>
<span data-ttu-id="e9480-124">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e9480-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e9480-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9480-125">-ResourceGroupName</span></span>
<span data-ttu-id="e9480-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9480-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e9480-127">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="e9480-127">-ThroughputType</span></span>
<span data-ttu-id="e9480-128">Typ przepustowości, do którego ma zostać dokonana migracja.</span><span class="sxs-lookup"><span data-stu-id="e9480-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="e9480-129">Możliwe wartości: automatyczne skalowanie, ręczne.</span><span class="sxs-lookup"><span data-stu-id="e9480-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e9480-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9480-130">-WhatIf</span></span>
<span data-ttu-id="e9480-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9480-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9480-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9480-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9480-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9480-133">CommonParameters</span></span>
<span data-ttu-id="e9480-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9480-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9480-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9480-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9480-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9480-136">INPUTS</span></span>

### <span data-ttu-id="e9480-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="e9480-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="e9480-138">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e9480-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e9480-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9480-139">OUTPUTS</span></span>

### <span data-ttu-id="e9480-140">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e9480-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e9480-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9480-141">NOTES</span></span>

## <span data-ttu-id="e9480-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9480-142">RELATED LINKS</span></span>
