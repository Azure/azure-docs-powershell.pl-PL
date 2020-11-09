---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306810"
---
# <span data-ttu-id="08d51-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="08d51-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="08d51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08d51-102">SYNOPSIS</span></span>
<span data-ttu-id="08d51-103">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="08d51-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="08d51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08d51-104">SYNTAX</span></span>

### <span data-ttu-id="08d51-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08d51-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d51-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08d51-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d51-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08d51-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d51-108">Opis</span><span class="sxs-lookup"><span data-stu-id="08d51-108">DESCRIPTION</span></span>
<span data-ttu-id="08d51-109">Aktualizuje wartość przepływności w bazie danych CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="08d51-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="08d51-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08d51-110">EXAMPLES</span></span>

### <span data-ttu-id="08d51-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08d51-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="08d51-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08d51-112">PARAMETERS</span></span>

### <span data-ttu-id="08d51-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08d51-113">-AccountName</span></span>
<span data-ttu-id="08d51-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="08d51-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="08d51-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="08d51-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="08d51-116">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="08d51-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="08d51-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08d51-117">-Confirm</span></span>
<span data-ttu-id="08d51-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08d51-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08d51-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d51-119">-DefaultProfile</span></span>
<span data-ttu-id="08d51-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08d51-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08d51-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08d51-121">-InputObject</span></span>
<span data-ttu-id="08d51-122">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="08d51-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="08d51-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08d51-123">-Name</span></span>
<span data-ttu-id="08d51-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="08d51-124">Database name.</span></span>

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

### <span data-ttu-id="08d51-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="08d51-125">-ParentObject</span></span>
<span data-ttu-id="08d51-126">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="08d51-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="08d51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d51-127">-ResourceGroupName</span></span>
<span data-ttu-id="08d51-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08d51-128">Name of resource group.</span></span>

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

### <span data-ttu-id="08d51-129">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="08d51-129">-Throughput</span></span>
<span data-ttu-id="08d51-130">Przepływność bazy danych Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="08d51-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="08d51-131">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="08d51-131">Default value is 400.</span></span>

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

### <span data-ttu-id="08d51-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d51-132">-WhatIf</span></span>
<span data-ttu-id="08d51-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08d51-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08d51-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08d51-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08d51-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d51-135">CommonParameters</span></span>
<span data-ttu-id="08d51-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08d51-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d51-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08d51-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d51-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08d51-138">INPUTS</span></span>

### <span data-ttu-id="08d51-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="08d51-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="08d51-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08d51-140">OUTPUTS</span></span>

### <span data-ttu-id="08d51-141">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="08d51-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="08d51-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08d51-142">NOTES</span></span>

## <span data-ttu-id="08d51-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08d51-143">RELATED LINKS</span></span>
