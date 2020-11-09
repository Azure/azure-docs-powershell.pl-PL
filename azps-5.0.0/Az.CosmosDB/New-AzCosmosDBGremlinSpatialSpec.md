---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307063"
---
# <span data-ttu-id="60f95-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="60f95-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="60f95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60f95-102">SYNOPSIS</span></span>
<span data-ttu-id="60f95-103">Tworzy nowy obiekt typu PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="60f95-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="60f95-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="60f95-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="60f95-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60f95-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60f95-106">Opis</span><span class="sxs-lookup"><span data-stu-id="60f95-106">DESCRIPTION</span></span>
<span data-ttu-id="60f95-107">Tworzy obiekt odpowiadający SpatialSpec API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="60f95-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="60f95-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60f95-108">EXAMPLES</span></span>

### <span data-ttu-id="60f95-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60f95-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="60f95-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60f95-110">PARAMETERS</span></span>

### <span data-ttu-id="60f95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f95-111">-DefaultProfile</span></span>
<span data-ttu-id="60f95-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60f95-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f95-113">-Path</span><span class="sxs-lookup"><span data-stu-id="60f95-113">-Path</span></span>
<span data-ttu-id="60f95-114">Ścieżka w dokumencie JSON do indeksu.</span><span class="sxs-lookup"><span data-stu-id="60f95-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="60f95-115">-Type</span><span class="sxs-lookup"><span data-stu-id="60f95-115">-Type</span></span>
<span data-ttu-id="60f95-116">Tablica ciągów z dopuszczalnymi wartościami: Point, LineString, Wielokąt, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="60f95-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="60f95-117">Typ przestrzenny reprezentujący ścieżki.</span><span class="sxs-lookup"><span data-stu-id="60f95-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="60f95-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f95-118">CommonParameters</span></span>
<span data-ttu-id="60f95-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f95-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f95-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60f95-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f95-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60f95-121">INPUTS</span></span>

### <span data-ttu-id="60f95-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="60f95-122">None</span></span>

## <span data-ttu-id="60f95-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60f95-123">OUTPUTS</span></span>

### <span data-ttu-id="60f95-124">Microsoft. Azure. Commands. CosmosDB. models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="60f95-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="60f95-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60f95-125">NOTES</span></span>

## <span data-ttu-id="60f95-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60f95-126">RELATED LINKS</span></span>
