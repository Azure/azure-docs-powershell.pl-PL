---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: ce554f3591f022bdbc375c12a50ea9dae85b8baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998810"
---
# <span data-ttu-id="9929a-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="9929a-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="9929a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9929a-102">SYNOPSIS</span></span>
<span data-ttu-id="9929a-103">Tworzy nowy obiekt ADB IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9929a-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="9929a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9929a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9929a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9929a-105">DESCRIPTION</span></span>
<span data-ttu-id="9929a-106">Polecenie cmdlet **New-AzCosmosDBGremlinIndexingPolicy** tworzy nowy obiekt typu PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9929a-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="9929a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9929a-107">EXAMPLES</span></span>

### <span data-ttu-id="9929a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9929a-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="9929a-109">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="9929a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9929a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9929a-110">PARAMETERS</span></span>

### <span data-ttu-id="9929a-111">— Automatyczne</span><span class="sxs-lookup"><span data-stu-id="9929a-111">-Automatic</span></span>
<span data-ttu-id="9929a-112">Wartość logiczna wskazująca, czy zasady indeksowania są automatyczne</span><span class="sxs-lookup"><span data-stu-id="9929a-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9929a-113">- CompositePath</span><span class="sxs-lookup"><span data-stu-id="9929a-113">-CompositePath</span></span>
<span data-ttu-id="9929a-114">Tablica obiektów typu Microsoft.Azure.Commands.AlejaDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="9929a-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9929a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9929a-115">-DefaultProfile</span></span>
<span data-ttu-id="9929a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9929a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9929a-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="9929a-117">-ExcludedPath</span></span>
<span data-ttu-id="9929a-118">Tablica ciągów zawierających ciągi excludedPath(Określa ścieżkę w dokumencie JSON do wykluczenia w usłudze Azure Azure DB).  .</span><span class="sxs-lookup"><span data-stu-id="9929a-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9929a-119">- IncludedPath</span><span class="sxs-lookup"><span data-stu-id="9929a-119">-IncludedPath</span></span>
<span data-ttu-id="9929a-120">Tablica ciągów zawierających ciągi includedPath (Określa ścieżkę w dokumencie JSON, która ma zostać uwzględniona w elementach usługi Azure Dokumencie DB).</span><span class="sxs-lookup"><span data-stu-id="9929a-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9929a-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="9929a-121">-IndexingMode</span></span>
<span data-ttu-id="9929a-122">Wskazuje tryb indeksowania.</span><span class="sxs-lookup"><span data-stu-id="9929a-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="9929a-123">Możliwe wartości: "Spójne", "Leniwe", "Brak"</span><span class="sxs-lookup"><span data-stu-id="9929a-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="9929a-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9929a-124">-SpatialSpec</span></span>
<span data-ttu-id="9929a-125">Tablica obiektów typu Microsoft.Azure.Commands.Dosdb.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9929a-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9929a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9929a-126">CommonParameters</span></span>
<span data-ttu-id="9929a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9929a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9929a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9929a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9929a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9929a-129">INPUTS</span></span>

### <span data-ttu-id="9929a-130">Brak</span><span class="sxs-lookup"><span data-stu-id="9929a-130">None</span></span>

## <span data-ttu-id="9929a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9929a-131">OUTPUTS</span></span>

### <span data-ttu-id="9929a-132">Microsoft.Azure.Commands.Dosdb.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="9929a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="9929a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9929a-133">NOTES</span></span>

## <span data-ttu-id="9929a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9929a-134">RELATED LINKS</span></span>
