---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501736"
---
# <span data-ttu-id="95640-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="95640-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="95640-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95640-102">SYNOPSIS</span></span>
<span data-ttu-id="95640-103">Tworzy nowy obiekt IndexingPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="95640-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="95640-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95640-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95640-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95640-105">DESCRIPTION</span></span>
<span data-ttu-id="95640-106">Polecenie cmdlet **New-AzCosmosDBGremlinIndexingPolicy** tworzy nowy obiekt typu PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="95640-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="95640-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95640-107">EXAMPLES</span></span>

### <span data-ttu-id="95640-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95640-108">Example 1</span></span>
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

<span data-ttu-id="95640-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="95640-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="95640-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95640-110">PARAMETERS</span></span>

### <span data-ttu-id="95640-111">-Automatyczna</span><span class="sxs-lookup"><span data-stu-id="95640-111">-Automatic</span></span>
<span data-ttu-id="95640-112">Wartość logiczna wskazująca, czy zasady indeksowania są automatyczne</span><span class="sxs-lookup"><span data-stu-id="95640-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="95640-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="95640-113">-CompositePath</span></span>
<span data-ttu-id="95640-114">Tablica tablicy obiektów typu Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="95640-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="95640-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95640-115">-DefaultProfile</span></span>
<span data-ttu-id="95640-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95640-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95640-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="95640-117">-ExcludedPath</span></span>
<span data-ttu-id="95640-118">Tablica ciągów zawierających excludedPath (określa ścieżkę w dokumencie JSON, która ma zostać wykluczona w ramach usługi Azure Cosmos DB Service).  czynników.</span><span class="sxs-lookup"><span data-stu-id="95640-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="95640-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="95640-119">-IncludedPath</span></span>
<span data-ttu-id="95640-120">Tablica ciągów zawierających includedPath (określa ścieżkę w dokumencie JSON, która ma być uwzględniana w elementach usługi Azure Cosmos DB Service).</span><span class="sxs-lookup"><span data-stu-id="95640-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="95640-121">-Indexmode</span><span class="sxs-lookup"><span data-stu-id="95640-121">-IndexingMode</span></span>
<span data-ttu-id="95640-122">Wskazuje tryb indeksowania.</span><span class="sxs-lookup"><span data-stu-id="95640-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="95640-123">Możliwe wartości to: "zgodne", "z opóźnieniem", "Brak".</span><span class="sxs-lookup"><span data-stu-id="95640-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="95640-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="95640-124">-SpatialSpec</span></span>
<span data-ttu-id="95640-125">Tablica obiektów typu Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="95640-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="95640-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95640-126">CommonParameters</span></span>
<span data-ttu-id="95640-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95640-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95640-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95640-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95640-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95640-129">INPUTS</span></span>

### <span data-ttu-id="95640-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="95640-130">None</span></span>

## <span data-ttu-id="95640-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95640-131">OUTPUTS</span></span>

### <span data-ttu-id="95640-132">Microsoft. Azure. Commands. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="95640-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="95640-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95640-133">NOTES</span></span>

## <span data-ttu-id="95640-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95640-134">RELATED LINKS</span></span>
