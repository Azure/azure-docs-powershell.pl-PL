---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052600"
---
# <span data-ttu-id="9ff53-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9ff53-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="9ff53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff53-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff53-103">Tworzy nowy obiekt typu PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="9ff53-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="9ff53-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9ff53-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="9ff53-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff53-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ff53-106">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff53-106">DESCRIPTION</span></span>
<span data-ttu-id="9ff53-107">Tworzy obiekt odpowiadający SpatialSpec API funkcji SQL.</span><span class="sxs-lookup"><span data-stu-id="9ff53-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="9ff53-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff53-108">EXAMPLES</span></span>

### <span data-ttu-id="9ff53-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ff53-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="9ff53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff53-110">PARAMETERS</span></span>

### <span data-ttu-id="9ff53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff53-111">-DefaultProfile</span></span>
<span data-ttu-id="9ff53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff53-113">-Path</span><span class="sxs-lookup"><span data-stu-id="9ff53-113">-Path</span></span>
<span data-ttu-id="9ff53-114">Ścieżka w dokumencie JSON do indeksu.</span><span class="sxs-lookup"><span data-stu-id="9ff53-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="9ff53-115">-Type</span><span class="sxs-lookup"><span data-stu-id="9ff53-115">-Type</span></span>
<span data-ttu-id="9ff53-116">Tablica ciągów z dopuszczalnymi wartościami: Point, LineString, Wielokąt, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="9ff53-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="9ff53-117">Typ przestrzenny reprezentujący ścieżki.</span><span class="sxs-lookup"><span data-stu-id="9ff53-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="9ff53-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff53-118">CommonParameters</span></span>
<span data-ttu-id="9ff53-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff53-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff53-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff53-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff53-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff53-121">INPUTS</span></span>

### <span data-ttu-id="9ff53-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9ff53-122">None</span></span>

## <span data-ttu-id="9ff53-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff53-123">OUTPUTS</span></span>

### <span data-ttu-id="9ff53-124">Microsoft. Azure. Commands. CosmosDB. models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9ff53-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="9ff53-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff53-125">NOTES</span></span>

## <span data-ttu-id="9ff53-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff53-126">RELATED LINKS</span></span>
