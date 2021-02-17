---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199043"
---
# <span data-ttu-id="927d2-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="927d2-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="927d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="927d2-102">SYNOPSIS</span></span>
<span data-ttu-id="927d2-103">Pobiera wartość przepływności tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="927d2-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="927d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="927d2-104">SYNTAX</span></span>

### <span data-ttu-id="927d2-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="927d2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927d2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="927d2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="927d2-107">DESCRIPTION</span></span>
<span data-ttu-id="927d2-108">Polecenie **cmdlet Get-AzCosmosDBCassandraTableThroughput** pobiera obiekt przepływności odpowiadający danej klawiszowi Keyspace.</span><span class="sxs-lookup"><span data-stu-id="927d2-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="927d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="927d2-109">EXAMPLES</span></span>

### <span data-ttu-id="927d2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="927d2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="927d2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="927d2-111">PARAMETERS</span></span>

### <span data-ttu-id="927d2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="927d2-112">-AccountName</span></span>
<span data-ttu-id="927d2-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="927d2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="927d2-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="927d2-114">-Confirm</span></span>
<span data-ttu-id="927d2-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="927d2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927d2-116">-DefaultProfile</span></span>
<span data-ttu-id="927d2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="927d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="927d2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="927d2-118">-InputObject</span></span>
<span data-ttu-id="927d2-119">Obiekt Cassandra Table.</span><span class="sxs-lookup"><span data-stu-id="927d2-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="927d2-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="927d2-120">-KeyspaceName</span></span>
<span data-ttu-id="927d2-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="927d2-121">Database name.</span></span>

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

### <span data-ttu-id="927d2-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="927d2-122">-Name</span></span>
<span data-ttu-id="927d2-123">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="927d2-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="927d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="927d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="927d2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="927d2-125">Name of resource group.</span></span>

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

### <span data-ttu-id="927d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927d2-126">-WhatIf</span></span>
<span data-ttu-id="927d2-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="927d2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="927d2-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="927d2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927d2-129">CommonParameters</span></span>
<span data-ttu-id="927d2-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927d2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="927d2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927d2-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="927d2-132">INPUTS</span></span>

### <span data-ttu-id="927d2-133">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="927d2-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="927d2-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="927d2-134">OUTPUTS</span></span>

### <span data-ttu-id="927d2-135">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="927d2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="927d2-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="927d2-136">NOTES</span></span>

## <span data-ttu-id="927d2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="927d2-137">RELATED LINKS</span></span>
