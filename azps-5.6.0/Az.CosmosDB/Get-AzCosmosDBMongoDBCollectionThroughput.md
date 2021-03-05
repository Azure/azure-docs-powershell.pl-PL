---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 8c27df120b17805a72e7ed50497448a8f3f58461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009194"
---
# <span data-ttu-id="801c8-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="801c8-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="801c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="801c8-102">SYNOPSIS</span></span>
<span data-ttu-id="801c8-103">Pobiera właściwości przepływności Pliku ADB kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="801c8-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="801c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="801c8-104">SYNTAX</span></span>

### <span data-ttu-id="801c8-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="801c8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="801c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="801c8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="801c8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="801c8-107">DESCRIPTION</span></span>
<span data-ttu-id="801c8-108">Polecenie **cmdlet Get-AzCosmosDBMongoDBCollectionThroughput** pobiera właściwości przepływności kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="801c8-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="801c8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="801c8-109">EXAMPLES</span></span>

### <span data-ttu-id="801c8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="801c8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="801c8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="801c8-111">PARAMETERS</span></span>

### <span data-ttu-id="801c8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="801c8-112">-AccountName</span></span>
<span data-ttu-id="801c8-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="801c8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="801c8-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="801c8-114">-Confirm</span></span>
<span data-ttu-id="801c8-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="801c8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="801c8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="801c8-116">-DatabaseName</span></span>
<span data-ttu-id="801c8-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="801c8-117">Database name.</span></span>

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

### <span data-ttu-id="801c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801c8-118">-DefaultProfile</span></span>
<span data-ttu-id="801c8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="801c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="801c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="801c8-120">-InputObject</span></span>
<span data-ttu-id="801c8-121">Jeśli zostanie podany, polecenie cmdlet zwraca kolekcję o odpowiedniej wartości przepływności.</span><span class="sxs-lookup"><span data-stu-id="801c8-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="801c8-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="801c8-122">-Name</span></span>
<span data-ttu-id="801c8-123">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="801c8-123">Collection name.</span></span>

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

### <span data-ttu-id="801c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="801c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="801c8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="801c8-125">Name of resource group.</span></span>

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

### <span data-ttu-id="801c8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="801c8-126">-WhatIf</span></span>
<span data-ttu-id="801c8-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="801c8-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="801c8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="801c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801c8-129">CommonParameters</span></span>
<span data-ttu-id="801c8-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801c8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="801c8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801c8-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="801c8-132">INPUTS</span></span>

### <span data-ttu-id="801c8-133">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="801c8-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="801c8-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="801c8-134">OUTPUTS</span></span>

### <span data-ttu-id="801c8-135">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="801c8-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="801c8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="801c8-136">NOTES</span></span>

## <span data-ttu-id="801c8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="801c8-137">RELATED LINKS</span></span>
