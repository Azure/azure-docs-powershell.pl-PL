---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501692"
---
# <span data-ttu-id="293c5-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="293c5-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="293c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="293c5-102">SYNOPSIS</span></span>
<span data-ttu-id="293c5-103">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="293c5-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="293c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="293c5-104">SYNTAX</span></span>

### <span data-ttu-id="293c5-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="293c5-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="293c5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="293c5-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="293c5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="293c5-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="293c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="293c5-108">DESCRIPTION</span></span>
<span data-ttu-id="293c5-109">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="293c5-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="293c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="293c5-110">EXAMPLES</span></span>

### <span data-ttu-id="293c5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="293c5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="293c5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="293c5-112">PARAMETERS</span></span>

### <span data-ttu-id="293c5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="293c5-113">-AccountName</span></span>
<span data-ttu-id="293c5-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="293c5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="293c5-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="293c5-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="293c5-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="293c5-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="293c5-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="293c5-117">-Confirm</span></span>
<span data-ttu-id="293c5-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="293c5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="293c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293c5-119">-DefaultProfile</span></span>
<span data-ttu-id="293c5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="293c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293c5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="293c5-121">-InputObject</span></span>
<span data-ttu-id="293c5-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="293c5-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="293c5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="293c5-123">-Name</span></span>
<span data-ttu-id="293c5-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="293c5-124">Database name.</span></span>

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

### <span data-ttu-id="293c5-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="293c5-125">-ParentObject</span></span>
<span data-ttu-id="293c5-126">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="293c5-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="293c5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="293c5-127">-ResourceGroupName</span></span>
<span data-ttu-id="293c5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="293c5-128">Name of resource group.</span></span>

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

### <span data-ttu-id="293c5-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="293c5-129">-Throughput</span></span>
<span data-ttu-id="293c5-130">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="293c5-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="293c5-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="293c5-131">Default value is 400.</span></span>

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

### <span data-ttu-id="293c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293c5-132">-WhatIf</span></span>
<span data-ttu-id="293c5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="293c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293c5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="293c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="293c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293c5-135">CommonParameters</span></span>
<span data-ttu-id="293c5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293c5-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="293c5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293c5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="293c5-138">INPUTS</span></span>

### <span data-ttu-id="293c5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="293c5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="293c5-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="293c5-140">OUTPUTS</span></span>

### <span data-ttu-id="293c5-141">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="293c5-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="293c5-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="293c5-142">NOTES</span></span>

## <span data-ttu-id="293c5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="293c5-143">RELATED LINKS</span></span>
