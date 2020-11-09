---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306990"
---
# <span data-ttu-id="421b7-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="421b7-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="421b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="421b7-102">SYNOPSIS</span></span>
<span data-ttu-id="421b7-103">Tworzy nowy obiekt IndexingPolicy SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="421b7-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="421b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="421b7-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="421b7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="421b7-105">DESCRIPTION</span></span>
<span data-ttu-id="421b7-106">Polecenie cmdlet **New-AzCosmosDBSqlIndexingPolicy** tworzy nowy obiekt typu PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="421b7-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="421b7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="421b7-107">EXAMPLES</span></span>

### <span data-ttu-id="421b7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="421b7-108">Example 1</span></span>
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

## <span data-ttu-id="421b7-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="421b7-109">PARAMETERS</span></span>

### <span data-ttu-id="421b7-110">-Automatyczna</span><span class="sxs-lookup"><span data-stu-id="421b7-110">-Automatic</span></span>
<span data-ttu-id="421b7-111">Wartość logiczna wskazująca, czy zasady indeksowania są automatyczne</span><span class="sxs-lookup"><span data-stu-id="421b7-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="421b7-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="421b7-112">-CompositePath</span></span>
<span data-ttu-id="421b7-113">Tablica tablicy obiektów typu Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="421b7-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="421b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421b7-114">-DefaultProfile</span></span>
<span data-ttu-id="421b7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="421b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="421b7-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="421b7-116">-ExcludedPath</span></span>
<span data-ttu-id="421b7-117">Tablica ciągów zawierających excludedPath (określa ścieżkę w dokumencie JSON, która ma zostać wykluczona w ramach usługi Azure Cosmos DB Service).  czynników.</span><span class="sxs-lookup"><span data-stu-id="421b7-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="421b7-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="421b7-118">-IncludedPath</span></span>
<span data-ttu-id="421b7-119">Tablica ciągów zawierających includedPath (określa ścieżkę w dokumencie JSON, która ma być uwzględniana w elementach usługi Azure Cosmos DB Service).</span><span class="sxs-lookup"><span data-stu-id="421b7-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="421b7-120">-Indexmode</span><span class="sxs-lookup"><span data-stu-id="421b7-120">-IndexingMode</span></span>
<span data-ttu-id="421b7-121">wskazuje tryb indeksowania.</span><span class="sxs-lookup"><span data-stu-id="421b7-121">indicates the indexing mode.</span></span>
<span data-ttu-id="421b7-122">Możliwe wartości to: "zgodne", "z opóźnieniem", "Brak".</span><span class="sxs-lookup"><span data-stu-id="421b7-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="421b7-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="421b7-123">-SpatialSpec</span></span>
<span data-ttu-id="421b7-124">Tablica obiektów typu Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="421b7-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="421b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421b7-125">CommonParameters</span></span>
<span data-ttu-id="421b7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="421b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421b7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="421b7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421b7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="421b7-128">INPUTS</span></span>

### <span data-ttu-id="421b7-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="421b7-129">None</span></span>

## <span data-ttu-id="421b7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="421b7-130">OUTPUTS</span></span>

### <span data-ttu-id="421b7-131">Microsoft. Azure. Commands. CosmosDB. models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="421b7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="421b7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="421b7-132">NOTES</span></span>

## <span data-ttu-id="421b7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="421b7-133">RELATED LINKS</span></span>
