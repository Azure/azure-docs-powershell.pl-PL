---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: c9a50c833de9290e08ac211b52586d25e5082c59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960849"
---
# <span data-ttu-id="2d0ea-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="2d0ea-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="2d0ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2d0ea-103">Tworzy nowy obiekt o typie indeksów PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="2d0ea-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBSqlIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="2d0ea-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d0ea-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d0ea-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d0ea-106">DESCRIPTION</span></span>
<span data-ttu-id="2d0ea-107">Obiekt odpowiadający indeksom includedpath interfejsu API sql.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="2d0ea-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d0ea-108">EXAMPLES</span></span>

### <span data-ttu-id="2d0ea-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d0ea-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="2d0ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d0ea-110">PARAMETERS</span></span>

### <span data-ttu-id="2d0ea-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="2d0ea-111">-DataType</span></span>
<span data-ttu-id="2d0ea-112">Typ danych, do którego zastosowano zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="2d0ea-113">Dopuszczalne wartości to: 'Ciąg', 'Liczba', 'Punkt', 'Wielokąt', 'LineString', 'MultiPolygon'</span><span class="sxs-lookup"><span data-stu-id="2d0ea-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="2d0ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d0ea-114">-DefaultProfile</span></span>
<span data-ttu-id="2d0ea-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d0ea-116">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="2d0ea-116">-Kind</span></span>
<span data-ttu-id="2d0ea-117">Wskazuje typ indeksu.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-117">Indicates the type of index.</span></span>
<span data-ttu-id="2d0ea-118">Możliwe wartości to: "Skrót", "Zakres", "Przestrzenny"</span><span class="sxs-lookup"><span data-stu-id="2d0ea-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="2d0ea-119">— Dokładność</span><span class="sxs-lookup"><span data-stu-id="2d0ea-119">-Precision</span></span>
<span data-ttu-id="2d0ea-120">Dokładność indeksu.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-120">The precision of the index.</span></span>
<span data-ttu-id="2d0ea-121">-1 to dokładność maksymalna.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d0ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d0ea-122">CommonParameters</span></span>
<span data-ttu-id="2d0ea-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d0ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d0ea-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d0ea-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d0ea-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d0ea-125">INPUTS</span></span>

### <span data-ttu-id="2d0ea-126">Brak</span><span class="sxs-lookup"><span data-stu-id="2d0ea-126">None</span></span>

## <span data-ttu-id="2d0ea-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d0ea-127">OUTPUTS</span></span>

### <span data-ttu-id="2d0ea-128">Microsoft.Azure.Commands.DoceńDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="2d0ea-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="2d0ea-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d0ea-129">NOTES</span></span>

## <span data-ttu-id="2d0ea-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d0ea-130">RELATED LINKS</span></span>
