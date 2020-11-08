---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223575"
---
# <span data-ttu-id="954d9-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="954d9-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="954d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="954d9-102">SYNOPSIS</span></span>
<span data-ttu-id="954d9-103">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="954d9-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="954d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="954d9-104">SYNTAX</span></span>

### <span data-ttu-id="954d9-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="954d9-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="954d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="954d9-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="954d9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="954d9-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="954d9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="954d9-108">DESCRIPTION</span></span>
<span data-ttu-id="954d9-109">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="954d9-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="954d9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="954d9-110">EXAMPLES</span></span>

### <span data-ttu-id="954d9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="954d9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="954d9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="954d9-112">PARAMETERS</span></span>

### <span data-ttu-id="954d9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="954d9-113">-AccountName</span></span>
<span data-ttu-id="954d9-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="954d9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="954d9-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="954d9-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="954d9-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="954d9-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="954d9-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="954d9-117">-Confirm</span></span>
<span data-ttu-id="954d9-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="954d9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="954d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954d9-119">-DefaultProfile</span></span>
<span data-ttu-id="954d9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="954d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="954d9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="954d9-121">-InputObject</span></span>
<span data-ttu-id="954d9-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="954d9-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="954d9-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="954d9-123">-Name</span></span>
<span data-ttu-id="954d9-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="954d9-124">Database name.</span></span>

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

### <span data-ttu-id="954d9-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="954d9-125">-ParentObject</span></span>
<span data-ttu-id="954d9-126">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="954d9-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="954d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="954d9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="954d9-128">Name of resource group.</span></span>

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

### <span data-ttu-id="954d9-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="954d9-129">-Throughput</span></span>
<span data-ttu-id="954d9-130">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="954d9-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="954d9-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="954d9-131">Default value is 400.</span></span>

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

### <span data-ttu-id="954d9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="954d9-132">-WhatIf</span></span>
<span data-ttu-id="954d9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="954d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="954d9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="954d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="954d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954d9-135">CommonParameters</span></span>
<span data-ttu-id="954d9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="954d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954d9-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="954d9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954d9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="954d9-138">INPUTS</span></span>

### <span data-ttu-id="954d9-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="954d9-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="954d9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="954d9-140">OUTPUTS</span></span>

### <span data-ttu-id="954d9-141">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="954d9-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="954d9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="954d9-142">NOTES</span></span>

## <span data-ttu-id="954d9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="954d9-143">RELATED LINKS</span></span>
