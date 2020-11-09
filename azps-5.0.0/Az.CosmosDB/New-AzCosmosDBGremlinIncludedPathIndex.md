---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307081"
---
# <span data-ttu-id="f9a1a-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="f9a1a-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="f9a1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a1a-103">Tworzy nowy obiekt typu PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="f9a1a-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="f9a1a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9a1a-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9a1a-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f9a1a-106">DESCRIPTION</span></span>
<span data-ttu-id="f9a1a-107">Obiekt odpowiadający indeksom IncludedPath's interfejsu API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="f9a1a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9a1a-108">EXAMPLES</span></span>

### <span data-ttu-id="f9a1a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9a1a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="f9a1a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9a1a-110">PARAMETERS</span></span>

### <span data-ttu-id="f9a1a-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="f9a1a-111">-DataType</span></span>
<span data-ttu-id="f9a1a-112">Typ danych, do którego jest stosowane zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="f9a1a-113">Możliwe są następujące wartości: "String", "number", "Point", "Wielokąt", "LineString", "MultiPolygon".</span><span class="sxs-lookup"><span data-stu-id="f9a1a-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="f9a1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a1a-114">-DefaultProfile</span></span>
<span data-ttu-id="f9a1a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9a1a-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="f9a1a-116">-Kind</span></span>
<span data-ttu-id="f9a1a-117">Wskazuje typ indeksu.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-117">Indicates the type of index.</span></span>
<span data-ttu-id="f9a1a-118">Możliwe wartości to: "hash", "Range", "przestrzenny"</span><span class="sxs-lookup"><span data-stu-id="f9a1a-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="f9a1a-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="f9a1a-119">-Precision</span></span>
<span data-ttu-id="f9a1a-120">Precyzja indeksu.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-120">The precision of the index.</span></span>
<span data-ttu-id="f9a1a-121">-1 to maksymalna precyzja.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="f9a1a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a1a-122">CommonParameters</span></span>
<span data-ttu-id="f9a1a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a1a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a1a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9a1a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a1a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9a1a-125">INPUTS</span></span>

### <span data-ttu-id="f9a1a-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f9a1a-126">None</span></span>

## <span data-ttu-id="f9a1a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9a1a-127">OUTPUTS</span></span>

### <span data-ttu-id="f9a1a-128">Microsoft. Azure. Commands. CosmosDB. models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="f9a1a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="f9a1a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9a1a-129">NOTES</span></span>

## <span data-ttu-id="f9a1a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9a1a-130">RELATED LINKS</span></span>
