---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 75ea7849424d8587f4eb4151bde63f31ea35676f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896781"
---
# <span data-ttu-id="1814b-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="1814b-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="1814b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1814b-102">SYNOPSIS</span></span>
<span data-ttu-id="1814b-103">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1814b-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1814b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1814b-104">SYNTAX</span></span>

### <span data-ttu-id="1814b-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1814b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1814b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1814b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1814b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1814b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1814b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1814b-108">EXAMPLES</span></span>

### <span data-ttu-id="1814b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1814b-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="1814b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1814b-110">PARAMETERS</span></span>

### <span data-ttu-id="1814b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1814b-111">-AccountName</span></span>
<span data-ttu-id="1814b-112">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1814b-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1814b-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1814b-113">-Confirm</span></span>
<span data-ttu-id="1814b-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1814b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1814b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1814b-115">-DefaultProfile</span></span>
<span data-ttu-id="1814b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1814b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1814b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1814b-117">-InputObject</span></span>
<span data-ttu-id="1814b-118">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1814b-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1814b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1814b-119">-Name</span></span>
<span data-ttu-id="1814b-120">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1814b-120">Database name.</span></span>

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

### <span data-ttu-id="1814b-121">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="1814b-121">-ParentObject</span></span>
<span data-ttu-id="1814b-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1814b-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1814b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1814b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1814b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1814b-124">Name of resource group.</span></span>

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

### <span data-ttu-id="1814b-125">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="1814b-125">-Throughput</span></span>
<span data-ttu-id="1814b-126">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1814b-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="1814b-127">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="1814b-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1814b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1814b-128">-WhatIf</span></span>
<span data-ttu-id="1814b-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1814b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1814b-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1814b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1814b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1814b-131">CommonParameters</span></span>
<span data-ttu-id="1814b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1814b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1814b-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1814b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1814b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1814b-134">INPUTS</span></span>

### <span data-ttu-id="1814b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1814b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1814b-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1814b-136">OUTPUTS</span></span>

### <span data-ttu-id="1814b-137">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1814b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1814b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1814b-138">NOTES</span></span>

## <span data-ttu-id="1814b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1814b-139">RELATED LINKS</span></span>
