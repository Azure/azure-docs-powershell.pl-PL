---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 8285afa9ba3764058f12ef0d8bfae009735a5ca3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957450"
---
# <span data-ttu-id="1dfcb-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="1dfcb-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="1dfcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dfcb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfcb-103">Tworzy nowy obiekt typu PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="1dfcb-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="1dfcb-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1dfcb-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dfcb-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="1dfcb-106">DESCRIPTION</span></span>
<span data-ttu-id="1dfcb-107">Tworzy obiekt odpowiadający parametrowi SpatialSpec interfejsu API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="1dfcb-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1dfcb-108">EXAMPLES</span></span>

### <span data-ttu-id="1dfcb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1dfcb-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="1dfcb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dfcb-110">PARAMETERS</span></span>

### <span data-ttu-id="1dfcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfcb-111">-DefaultProfile</span></span>
<span data-ttu-id="1dfcb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dfcb-113">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="1dfcb-113">-Path</span></span>
<span data-ttu-id="1dfcb-114">Ścieżka w dokumencie JSON do indeksowania.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="1dfcb-115">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="1dfcb-115">-Type</span></span>
<span data-ttu-id="1dfcb-116">Tablica ciągów z dopuszczalnymi wartościami: Punkt, Ciąg liniowy, Wielokąt, Wielopolygon.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="1dfcb-117">Ujmij ścieżki w typ przestrzenny.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="1dfcb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfcb-118">CommonParameters</span></span>
<span data-ttu-id="1dfcb-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dfcb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfcb-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dfcb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfcb-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dfcb-121">INPUTS</span></span>

### <span data-ttu-id="1dfcb-122">Brak</span><span class="sxs-lookup"><span data-stu-id="1dfcb-122">None</span></span>

## <span data-ttu-id="1dfcb-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dfcb-123">OUTPUTS</span></span>

### <span data-ttu-id="1dfcb-124">Microsoft.Azure.Commands.DoceńDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="1dfcb-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="1dfcb-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1dfcb-125">NOTES</span></span>

## <span data-ttu-id="1dfcb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dfcb-126">RELATED LINKS</span></span>
