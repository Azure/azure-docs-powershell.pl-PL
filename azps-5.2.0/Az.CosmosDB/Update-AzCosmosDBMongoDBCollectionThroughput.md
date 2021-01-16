---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329350"
---
# <span data-ttu-id="beeea-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="beeea-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="beeea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="beeea-102">SYNOPSIS</span></span>
<span data-ttu-id="beeea-103">Umożliwia zaktualizowanie wartości przepływności kolekcji MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="beeea-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="beeea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="beeea-104">SYNTAX</span></span>

### <span data-ttu-id="beeea-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="beeea-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beeea-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beeea-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beeea-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beeea-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beeea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="beeea-108">DESCRIPTION</span></span>
<span data-ttu-id="beeea-109">Umożliwia zaktualizowanie wartości przepływności kolekcji MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="beeea-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="beeea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="beeea-110">EXAMPLES</span></span>

### <span data-ttu-id="beeea-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="beeea-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="beeea-112">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="beeea-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="beeea-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="beeea-113">PARAMETERS</span></span>

### <span data-ttu-id="beeea-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="beeea-114">-AccountName</span></span>
<span data-ttu-id="beeea-115">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="beeea-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="beeea-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="beeea-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="beeea-117">Maksymalna wartość przepływności, jeśli funkcja automatycznego skalowania jest włączona.</span><span class="sxs-lookup"><span data-stu-id="beeea-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="beeea-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="beeea-118">-Confirm</span></span>
<span data-ttu-id="beeea-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beeea-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beeea-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="beeea-120">-DatabaseName</span></span>
<span data-ttu-id="beeea-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="beeea-121">Database name.</span></span>

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

### <span data-ttu-id="beeea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeea-122">-DefaultProfile</span></span>
<span data-ttu-id="beeea-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="beeea-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beeea-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="beeea-124">-InputObject</span></span>
<span data-ttu-id="beeea-125">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="beeea-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beeea-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="beeea-126">-Name</span></span>
<span data-ttu-id="beeea-127">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="beeea-127">Collection name.</span></span>

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

### <span data-ttu-id="beeea-128">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="beeea-128">-ParentObject</span></span>
<span data-ttu-id="beeea-129">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="beeea-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beeea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beeea-130">-ResourceGroupName</span></span>
<span data-ttu-id="beeea-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="beeea-131">Name of resource group.</span></span>

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

### <span data-ttu-id="beeea-132">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="beeea-132">-Throughput</span></span>
<span data-ttu-id="beeea-133">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="beeea-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="beeea-134">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="beeea-134">Default value is 400.</span></span>

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

### <span data-ttu-id="beeea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beeea-135">-WhatIf</span></span>
<span data-ttu-id="beeea-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beeea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beeea-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="beeea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beeea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeea-138">CommonParameters</span></span>
<span data-ttu-id="beeea-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beeea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeea-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beeea-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeea-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="beeea-141">INPUTS</span></span>

### <span data-ttu-id="beeea-142">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="beeea-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="beeea-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="beeea-143">OUTPUTS</span></span>

### <span data-ttu-id="beeea-144">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="beeea-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="beeea-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="beeea-145">NOTES</span></span>

## <span data-ttu-id="beeea-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="beeea-146">RELATED LINKS</span></span>
