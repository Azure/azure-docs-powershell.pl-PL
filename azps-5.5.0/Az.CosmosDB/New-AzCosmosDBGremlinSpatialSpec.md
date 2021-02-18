---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181315"
---
# <span data-ttu-id="ee16e-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ee16e-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="ee16e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee16e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee16e-103">Tworzy nowy obiekt typu PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="ee16e-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="ee16e-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="ee16e-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="ee16e-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee16e-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee16e-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee16e-106">DESCRIPTION</span></span>
<span data-ttu-id="ee16e-107">Tworzy obiekt odpowiadający parametrowi SpatialSpec interfejsu API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ee16e-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="ee16e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee16e-108">EXAMPLES</span></span>

### <span data-ttu-id="ee16e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee16e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="ee16e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee16e-110">PARAMETERS</span></span>

### <span data-ttu-id="ee16e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee16e-111">-DefaultProfile</span></span>
<span data-ttu-id="ee16e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee16e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee16e-113">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="ee16e-113">-Path</span></span>
<span data-ttu-id="ee16e-114">Ścieżka w dokumencie JSON do indeksowania.</span><span class="sxs-lookup"><span data-stu-id="ee16e-114">Path in JSON document to index.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee16e-115">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="ee16e-115">-Type</span></span>
<span data-ttu-id="ee16e-116">Tablica ciągów z dopuszczalnymi wartościami: punkt, ciąg liniowy, wielokąt, wielopolon.</span><span class="sxs-lookup"><span data-stu-id="ee16e-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="ee16e-117">Ujmij ścieżki w typ przestrzenny.</span><span class="sxs-lookup"><span data-stu-id="ee16e-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee16e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee16e-118">CommonParameters</span></span>
<span data-ttu-id="ee16e-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee16e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee16e-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee16e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee16e-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee16e-121">INPUTS</span></span>

### <span data-ttu-id="ee16e-122">Brak</span><span class="sxs-lookup"><span data-stu-id="ee16e-122">None</span></span>

## <span data-ttu-id="ee16e-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee16e-123">OUTPUTS</span></span>

### <span data-ttu-id="ee16e-124">Microsoft.Azure.Commands.DoceńDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ee16e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="ee16e-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee16e-125">NOTES</span></span>

## <span data-ttu-id="ee16e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee16e-126">RELATED LINKS</span></span>
