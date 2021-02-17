---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196819"
---
# <span data-ttu-id="ba3d1-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="ba3d1-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="ba3d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3d1-103">Tworzy nowy obiekt typu PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="ba3d1-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="ba3d1-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="ba3d1-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="ba3d1-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba3d1-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba3d1-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba3d1-106">DESCRIPTION</span></span>
<span data-ttu-id="ba3d1-107">Obiekt odpowiadający właściwości IncludedPath interfejsu API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ba3d1-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="ba3d1-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba3d1-108">EXAMPLES</span></span>

### <span data-ttu-id="ba3d1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba3d1-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="ba3d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba3d1-110">PARAMETERS</span></span>

### <span data-ttu-id="ba3d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3d1-111">-DefaultProfile</span></span>
<span data-ttu-id="ba3d1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba3d1-113">-Index</span><span class="sxs-lookup"><span data-stu-id="ba3d1-113">-Index</span></span>
<span data-ttu-id="ba3d1-114">Lista indeksów dla tej ścieżki</span><span class="sxs-lookup"><span data-stu-id="ba3d1-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3d1-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="ba3d1-115">-Path</span></span>
<span data-ttu-id="ba3d1-116">Ścieżka, do której ma zastosowanie zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="ba3d1-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="ba3d1-117">Ścieżki indeksu zazwyczaj zaczynają się od katalogu głównego i kończą się symbolami wieloznacznymi (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="ba3d1-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="ba3d1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3d1-118">CommonParameters</span></span>
<span data-ttu-id="ba3d1-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3d1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3d1-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba3d1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3d1-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba3d1-121">INPUTS</span></span>

### <span data-ttu-id="ba3d1-122">Brak</span><span class="sxs-lookup"><span data-stu-id="ba3d1-122">None</span></span>

## <span data-ttu-id="ba3d1-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba3d1-123">OUTPUTS</span></span>

### <span data-ttu-id="ba3d1-124">Microsoft.Azure.Commands.DoceńDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="ba3d1-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="ba3d1-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba3d1-125">NOTES</span></span>

## <span data-ttu-id="ba3d1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba3d1-126">RELATED LINKS</span></span>
