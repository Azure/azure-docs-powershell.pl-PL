---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238519"
---
# <span data-ttu-id="04c9c-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="04c9c-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="04c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="04c9c-103">Tworzy nowy obiekt typu PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="04c9c-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="04c9c-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="04c9c-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="04c9c-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04c9c-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04c9c-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="04c9c-106">DESCRIPTION</span></span>
<span data-ttu-id="04c9c-107">Tworzy obiekt odpowiadający parametrowi SpatialSpec interfejsu API sql.</span><span class="sxs-lookup"><span data-stu-id="04c9c-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="04c9c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04c9c-108">EXAMPLES</span></span>

### <span data-ttu-id="04c9c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04c9c-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="04c9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04c9c-110">PARAMETERS</span></span>

### <span data-ttu-id="04c9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c9c-111">-DefaultProfile</span></span>
<span data-ttu-id="04c9c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04c9c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c9c-113">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="04c9c-113">-Path</span></span>
<span data-ttu-id="04c9c-114">Ścieżka w dokumencie JSON do indeksowania.</span><span class="sxs-lookup"><span data-stu-id="04c9c-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="04c9c-115">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="04c9c-115">-Type</span></span>
<span data-ttu-id="04c9c-116">Tablica ciągów z dopuszczalnymi wartościami: Punkt, Ciąg liniowy, Wielokąt, Wielopolygon.</span><span class="sxs-lookup"><span data-stu-id="04c9c-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="04c9c-117">Ujmij ścieżki w typ przestrzenny.</span><span class="sxs-lookup"><span data-stu-id="04c9c-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="04c9c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c9c-118">CommonParameters</span></span>
<span data-ttu-id="04c9c-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c9c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c9c-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04c9c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c9c-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04c9c-121">INPUTS</span></span>

### <span data-ttu-id="04c9c-122">Brak</span><span class="sxs-lookup"><span data-stu-id="04c9c-122">None</span></span>

## <span data-ttu-id="04c9c-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04c9c-123">OUTPUTS</span></span>

### <span data-ttu-id="04c9c-124">Microsoft.Azure.Commands.DoceńDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="04c9c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="04c9c-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04c9c-125">NOTES</span></span>

## <span data-ttu-id="04c9c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04c9c-126">RELATED LINKS</span></span>
