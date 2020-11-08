---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051150"
---
# <span data-ttu-id="02ddb-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="02ddb-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="02ddb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="02ddb-103">Umożliwia zaktualizowanie wartości przepływności kolekcji MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="02ddb-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="02ddb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02ddb-104">SYNTAX</span></span>

### <span data-ttu-id="02ddb-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02ddb-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ddb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ddb-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ddb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ddb-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02ddb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02ddb-108">EXAMPLES</span></span>

### <span data-ttu-id="02ddb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02ddb-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="02ddb-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="02ddb-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="02ddb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02ddb-111">PARAMETERS</span></span>

### <span data-ttu-id="02ddb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02ddb-112">-AccountName</span></span>
<span data-ttu-id="02ddb-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="02ddb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02ddb-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02ddb-114">-Confirm</span></span>
<span data-ttu-id="02ddb-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ddb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ddb-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02ddb-116">-DatabaseName</span></span>
<span data-ttu-id="02ddb-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="02ddb-117">Database name.</span></span>

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

### <span data-ttu-id="02ddb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ddb-118">-DefaultProfile</span></span>
<span data-ttu-id="02ddb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02ddb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ddb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02ddb-120">-InputObject</span></span>
<span data-ttu-id="02ddb-121">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="02ddb-121">Mongo Database object.</span></span>

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

### <span data-ttu-id="02ddb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02ddb-122">-Name</span></span>
<span data-ttu-id="02ddb-123">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="02ddb-123">Collection name.</span></span>

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

### <span data-ttu-id="02ddb-124">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="02ddb-124">-ParentObject</span></span>
<span data-ttu-id="02ddb-125">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="02ddb-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="02ddb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ddb-126">-ResourceGroupName</span></span>
<span data-ttu-id="02ddb-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02ddb-127">Name of resource group.</span></span>

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

### <span data-ttu-id="02ddb-128">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="02ddb-128">-Throughput</span></span>
<span data-ttu-id="02ddb-129">Przepływność kontenera SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="02ddb-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="02ddb-130">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="02ddb-130">Default value is 400.</span></span>

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

### <span data-ttu-id="02ddb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ddb-131">-WhatIf</span></span>
<span data-ttu-id="02ddb-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ddb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ddb-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02ddb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ddb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ddb-134">CommonParameters</span></span>
<span data-ttu-id="02ddb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ddb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ddb-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ddb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ddb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02ddb-137">INPUTS</span></span>

### <span data-ttu-id="02ddb-138">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="02ddb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="02ddb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02ddb-139">OUTPUTS</span></span>

### <span data-ttu-id="02ddb-140">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="02ddb-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="02ddb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02ddb-141">NOTES</span></span>

## <span data-ttu-id="02ddb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02ddb-142">RELATED LINKS</span></span>
