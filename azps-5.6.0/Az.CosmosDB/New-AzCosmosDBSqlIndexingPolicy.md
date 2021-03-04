---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: b3d7591bf5dd83967230f6c96c3ca5b02232e316
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975914"
---
# <span data-ttu-id="88dfd-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="88dfd-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="88dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="88dfd-103">Tworzy nowy obiekt ADB Sql IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="88dfd-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="88dfd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88dfd-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88dfd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="88dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="88dfd-106">Polecenie cmdlet **New-AzCosmosDBSqlIndexingPolicy** tworzy nowy obiekt typu PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="88dfd-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="88dfd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="88dfd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88dfd-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="88dfd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88dfd-109">PARAMETERS</span></span>

### <span data-ttu-id="88dfd-110">— Automatyczne</span><span class="sxs-lookup"><span data-stu-id="88dfd-110">-Automatic</span></span>
<span data-ttu-id="88dfd-111">Wartość logiczna wskazująca, czy zasady indeksowania są automatyczne</span><span class="sxs-lookup"><span data-stu-id="88dfd-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="88dfd-112">- CompositePath</span><span class="sxs-lookup"><span data-stu-id="88dfd-112">-CompositePath</span></span>
<span data-ttu-id="88dfd-113">Tablica obiektów typu Microsoft.Azure.Commands.AlejaDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="88dfd-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="88dfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dfd-114">-DefaultProfile</span></span>
<span data-ttu-id="88dfd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88dfd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88dfd-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="88dfd-116">-ExcludedPath</span></span>
<span data-ttu-id="88dfd-117">Tablica ciągów zawierających ciągi excludedPath(Określa ścieżkę w dokumencie JSON do wykluczenia w usłudze Azure Azure DB).  .</span><span class="sxs-lookup"><span data-stu-id="88dfd-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="88dfd-118">- IncludedPath</span><span class="sxs-lookup"><span data-stu-id="88dfd-118">-IncludedPath</span></span>
<span data-ttu-id="88dfd-119">Tablica ciągów zawierających ciągi includedPath (Określa ścieżkę w dokumencie JSON, która ma zostać uwzględniona w elementach usługi Azure Dokumencie DB).</span><span class="sxs-lookup"><span data-stu-id="88dfd-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="88dfd-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="88dfd-120">-IndexingMode</span></span>
<span data-ttu-id="88dfd-121">wskazuje tryb indeksowania.</span><span class="sxs-lookup"><span data-stu-id="88dfd-121">indicates the indexing mode.</span></span>
<span data-ttu-id="88dfd-122">Możliwe wartości: "Spójne", "Leniwe", "Brak"</span><span class="sxs-lookup"><span data-stu-id="88dfd-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="88dfd-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="88dfd-123">-SpatialSpec</span></span>
<span data-ttu-id="88dfd-124">Tablica obiektów typu Microsoft.Azure.Commands.Dosdb.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="88dfd-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="88dfd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dfd-125">CommonParameters</span></span>
<span data-ttu-id="88dfd-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88dfd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dfd-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88dfd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dfd-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88dfd-128">INPUTS</span></span>

### <span data-ttu-id="88dfd-129">Brak</span><span class="sxs-lookup"><span data-stu-id="88dfd-129">None</span></span>

## <span data-ttu-id="88dfd-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88dfd-130">OUTPUTS</span></span>

### <span data-ttu-id="88dfd-131">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="88dfd-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="88dfd-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88dfd-132">NOTES</span></span>

## <span data-ttu-id="88dfd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88dfd-133">RELATED LINKS</span></span>
