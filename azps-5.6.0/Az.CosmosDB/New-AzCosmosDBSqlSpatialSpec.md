---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: e22c8931cf70fba970e71b7a2d099cda725287d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004321"
---
# <span data-ttu-id="b3b76-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="b3b76-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="b3b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b76-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b76-103">Tworzy nowy obiekt typu PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="b3b76-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="b3b76-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="b3b76-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="b3b76-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3b76-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3b76-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3b76-106">DESCRIPTION</span></span>
<span data-ttu-id="b3b76-107">Tworzy obiekt odpowiadający parametrowi SpatialSpec interfejsu API sql.</span><span class="sxs-lookup"><span data-stu-id="b3b76-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="b3b76-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3b76-108">EXAMPLES</span></span>

### <span data-ttu-id="b3b76-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3b76-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="b3b76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3b76-110">PARAMETERS</span></span>

### <span data-ttu-id="b3b76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b76-111">-DefaultProfile</span></span>
<span data-ttu-id="b3b76-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b76-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b76-113">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="b3b76-113">-Path</span></span>
<span data-ttu-id="b3b76-114">Ścieżka w dokumencie JSON do indeksowania.</span><span class="sxs-lookup"><span data-stu-id="b3b76-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="b3b76-115">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="b3b76-115">-Type</span></span>
<span data-ttu-id="b3b76-116">Tablica ciągów z dopuszczalnymi wartościami: Punkt, Ciąg liniowy, Wielokąt, Wielopolygon.</span><span class="sxs-lookup"><span data-stu-id="b3b76-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="b3b76-117">Ujmij ścieżki w typ przestrzenny.</span><span class="sxs-lookup"><span data-stu-id="b3b76-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="b3b76-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b76-118">CommonParameters</span></span>
<span data-ttu-id="b3b76-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b76-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b76-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3b76-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b76-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3b76-121">INPUTS</span></span>

### <span data-ttu-id="b3b76-122">Brak</span><span class="sxs-lookup"><span data-stu-id="b3b76-122">None</span></span>

## <span data-ttu-id="b3b76-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3b76-123">OUTPUTS</span></span>

### <span data-ttu-id="b3b76-124">Microsoft.Azure.Commands.DoceńDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="b3b76-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="b3b76-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3b76-125">NOTES</span></span>

## <span data-ttu-id="b3b76-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3b76-126">RELATED LINKS</span></span>
