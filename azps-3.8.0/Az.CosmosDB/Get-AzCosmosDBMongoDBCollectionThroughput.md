---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053085"
---
# <span data-ttu-id="2fba3-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="2fba3-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="2fba3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fba3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fba3-103">Pobiera właściwości przepływności CosmosDB kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="2fba3-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="2fba3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fba3-104">SYNTAX</span></span>

### <span data-ttu-id="2fba3-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2fba3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fba3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fba3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fba3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fba3-107">DESCRIPTION</span></span>
<span data-ttu-id="2fba3-108">Polecenie cmdlet **Get-AzCosmosDBMongoDBCollectionThroughput** pobiera właściwości przepływności kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="2fba3-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="2fba3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fba3-109">EXAMPLES</span></span>

### <span data-ttu-id="2fba3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fba3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="2fba3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fba3-111">PARAMETERS</span></span>

### <span data-ttu-id="2fba3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2fba3-112">-AccountName</span></span>
<span data-ttu-id="2fba3-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2fba3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2fba3-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fba3-114">-Confirm</span></span>
<span data-ttu-id="2fba3-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fba3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fba3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2fba3-116">-DatabaseName</span></span>
<span data-ttu-id="2fba3-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2fba3-117">Database name.</span></span>

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

### <span data-ttu-id="2fba3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fba3-118">-DefaultProfile</span></span>
<span data-ttu-id="2fba3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fba3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fba3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2fba3-120">-InputObject</span></span>
<span data-ttu-id="2fba3-121">Jeśli ta funkcja zostanie dostarczona, polecenie cmdlet zwróci kolekcję z odpowiednią wartością przepustowości.</span><span class="sxs-lookup"><span data-stu-id="2fba3-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fba3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fba3-122">-Name</span></span>
<span data-ttu-id="2fba3-123">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="2fba3-123">Collection name.</span></span>

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

### <span data-ttu-id="2fba3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fba3-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fba3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fba3-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2fba3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fba3-126">-WhatIf</span></span>
<span data-ttu-id="2fba3-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fba3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fba3-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fba3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fba3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fba3-129">CommonParameters</span></span>
<span data-ttu-id="2fba3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fba3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fba3-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fba3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fba3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fba3-132">INPUTS</span></span>

### <span data-ttu-id="2fba3-133">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="2fba3-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="2fba3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fba3-134">OUTPUTS</span></span>

### <span data-ttu-id="2fba3-135">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2fba3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2fba3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fba3-136">NOTES</span></span>

## <span data-ttu-id="2fba3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fba3-137">RELATED LINKS</span></span>
