---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341185"
---
# <span data-ttu-id="12654-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="12654-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="12654-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12654-102">SYNOPSIS</span></span>
<span data-ttu-id="12654-103">Pobiera wartość przepływności tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12654-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="12654-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12654-104">SYNTAX</span></span>

### <span data-ttu-id="12654-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12654-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12654-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12654-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12654-107">Opis</span><span class="sxs-lookup"><span data-stu-id="12654-107">DESCRIPTION</span></span>
<span data-ttu-id="12654-108">Polecenie cmdlet **Get-AzCosmosDBCassandraTableThroughput** pobiera obiekt przepływności odpowiadający danej przestrzeni.</span><span class="sxs-lookup"><span data-stu-id="12654-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="12654-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12654-109">EXAMPLES</span></span>

### <span data-ttu-id="12654-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12654-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="12654-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12654-111">PARAMETERS</span></span>

### <span data-ttu-id="12654-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12654-112">-AccountName</span></span>
<span data-ttu-id="12654-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="12654-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="12654-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12654-114">-Confirm</span></span>
<span data-ttu-id="12654-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12654-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12654-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12654-116">-DefaultProfile</span></span>
<span data-ttu-id="12654-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12654-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12654-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12654-118">-InputObject</span></span>
<span data-ttu-id="12654-119">Obiekt tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12654-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="12654-120">-Spacename</span><span class="sxs-lookup"><span data-stu-id="12654-120">-KeyspaceName</span></span>
<span data-ttu-id="12654-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="12654-121">Database name.</span></span>

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

### <span data-ttu-id="12654-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12654-122">-Name</span></span>
<span data-ttu-id="12654-123">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="12654-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="12654-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12654-124">-ResourceGroupName</span></span>
<span data-ttu-id="12654-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12654-125">Name of resource group.</span></span>

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

### <span data-ttu-id="12654-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12654-126">-WhatIf</span></span>
<span data-ttu-id="12654-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12654-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12654-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12654-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12654-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12654-129">CommonParameters</span></span>
<span data-ttu-id="12654-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12654-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12654-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12654-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12654-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12654-132">INPUTS</span></span>

### <span data-ttu-id="12654-133">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="12654-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="12654-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12654-134">OUTPUTS</span></span>

### <span data-ttu-id="12654-135">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="12654-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="12654-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12654-136">NOTES</span></span>

## <span data-ttu-id="12654-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12654-137">RELATED LINKS</span></span>
