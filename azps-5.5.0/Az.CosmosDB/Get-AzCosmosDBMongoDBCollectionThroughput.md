---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181395"
---
# <span data-ttu-id="d879d-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="d879d-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="d879d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d879d-102">SYNOPSIS</span></span>
<span data-ttu-id="d879d-103">Pobiera właściwości przepływności Pliku ADB kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="d879d-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="d879d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d879d-104">SYNTAX</span></span>

### <span data-ttu-id="d879d-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d879d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d879d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d879d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d879d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d879d-107">DESCRIPTION</span></span>
<span data-ttu-id="d879d-108">Polecenie **cmdlet Get-AzCosmosDBMongoDBCollectionThroughput** pobiera właściwości przepływności kolekcji MongoDB.</span><span class="sxs-lookup"><span data-stu-id="d879d-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="d879d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d879d-109">EXAMPLES</span></span>

### <span data-ttu-id="d879d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d879d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="d879d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d879d-111">PARAMETERS</span></span>

### <span data-ttu-id="d879d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d879d-112">-AccountName</span></span>
<span data-ttu-id="d879d-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="d879d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d879d-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d879d-114">-Confirm</span></span>
<span data-ttu-id="d879d-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d879d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d879d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d879d-116">-DatabaseName</span></span>
<span data-ttu-id="d879d-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d879d-117">Database name.</span></span>

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

### <span data-ttu-id="d879d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d879d-118">-DefaultProfile</span></span>
<span data-ttu-id="d879d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d879d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d879d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d879d-120">-InputObject</span></span>
<span data-ttu-id="d879d-121">Jeśli zostanie podany, polecenie cmdlet zwraca kolekcję o odpowiedniej wartości przepływności.</span><span class="sxs-lookup"><span data-stu-id="d879d-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="d879d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d879d-122">-Name</span></span>
<span data-ttu-id="d879d-123">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="d879d-123">Collection name.</span></span>

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

### <span data-ttu-id="d879d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d879d-124">-ResourceGroupName</span></span>
<span data-ttu-id="d879d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d879d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d879d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d879d-126">-WhatIf</span></span>
<span data-ttu-id="d879d-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d879d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d879d-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d879d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d879d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d879d-129">CommonParameters</span></span>
<span data-ttu-id="d879d-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d879d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d879d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d879d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d879d-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d879d-132">INPUTS</span></span>

### <span data-ttu-id="d879d-133">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="d879d-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="d879d-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d879d-134">OUTPUTS</span></span>

### <span data-ttu-id="d879d-135">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d879d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d879d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d879d-136">NOTES</span></span>

## <span data-ttu-id="d879d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d879d-137">RELATED LINKS</span></span>
