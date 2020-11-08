---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052598"
---
# <span data-ttu-id="77fc1-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="77fc1-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="77fc1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="77fc1-103">Tworzy nowy obiekt typu PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="77fc1-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="77fc1-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBSqlIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="77fc1-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="77fc1-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77fc1-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77fc1-106">Opis</span><span class="sxs-lookup"><span data-stu-id="77fc1-106">DESCRIPTION</span></span>
<span data-ttu-id="77fc1-107">Obiekt odpowiadający indeksom programu SQL API IncludedPath's.</span><span class="sxs-lookup"><span data-stu-id="77fc1-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="77fc1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77fc1-108">EXAMPLES</span></span>

### <span data-ttu-id="77fc1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77fc1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="77fc1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77fc1-110">PARAMETERS</span></span>

### <span data-ttu-id="77fc1-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="77fc1-111">-DataType</span></span>
<span data-ttu-id="77fc1-112">Typ danych, do którego jest stosowane zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="77fc1-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="77fc1-113">Możliwe są następujące wartości: "String", "number", "Point", "Wielokąt", "LineString", "MultiPolygon".</span><span class="sxs-lookup"><span data-stu-id="77fc1-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="77fc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fc1-114">-DefaultProfile</span></span>
<span data-ttu-id="77fc1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77fc1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77fc1-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="77fc1-116">-Kind</span></span>
<span data-ttu-id="77fc1-117">Wskazuje typ indeksu.</span><span class="sxs-lookup"><span data-stu-id="77fc1-117">Indicates the type of index.</span></span>
<span data-ttu-id="77fc1-118">Możliwe wartości to: "hash", "Range", "przestrzenny"</span><span class="sxs-lookup"><span data-stu-id="77fc1-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="77fc1-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="77fc1-119">-Precision</span></span>
<span data-ttu-id="77fc1-120">Precyzja indeksu.</span><span class="sxs-lookup"><span data-stu-id="77fc1-120">The precision of the index.</span></span>
<span data-ttu-id="77fc1-121">-1 to maksymalna precyzja.</span><span class="sxs-lookup"><span data-stu-id="77fc1-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="77fc1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fc1-122">CommonParameters</span></span>
<span data-ttu-id="77fc1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77fc1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fc1-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77fc1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fc1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77fc1-125">INPUTS</span></span>

### <span data-ttu-id="77fc1-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77fc1-126">None</span></span>

## <span data-ttu-id="77fc1-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77fc1-127">OUTPUTS</span></span>

### <span data-ttu-id="77fc1-128">Microsoft. Azure. Commands. CosmosDB. models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="77fc1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="77fc1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77fc1-129">NOTES</span></span>

## <span data-ttu-id="77fc1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77fc1-130">RELATED LINKS</span></span>
