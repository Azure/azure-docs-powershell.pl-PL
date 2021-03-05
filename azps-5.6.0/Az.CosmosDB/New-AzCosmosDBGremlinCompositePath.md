---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: c88cde11d277a4a2e0473d41f83e1b62e13216bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007994"
---
# <span data-ttu-id="fcdc5-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="fcdc5-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="fcdc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdc5-103">Tworzy nowy obiekt typu PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="fcdc5-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="fcdc5-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcdc5-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcdc5-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcdc5-106">DESCRIPTION</span></span>
<span data-ttu-id="fcdc5-107">Obiekt odpowiadający projektowi CompositePath interfejsu API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="fcdc5-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcdc5-108">EXAMPLES</span></span>

### <span data-ttu-id="fcdc5-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fcdc5-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="fcdc5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcdc5-110">PARAMETERS</span></span>

### <span data-ttu-id="fcdc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdc5-111">-DefaultProfile</span></span>
<span data-ttu-id="fcdc5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcdc5-113">— zamówienie</span><span class="sxs-lookup"><span data-stu-id="fcdc5-113">-Order</span></span>
<span data-ttu-id="fcdc5-114">Pobiera lub ustawia kolejność sortowania dla ścieżek złożonych.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="fcdc5-115">Możliwe wartości: "Rosnąco", "Malejąco"</span><span class="sxs-lookup"><span data-stu-id="fcdc5-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="fcdc5-116">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="fcdc5-116">-Path</span></span>
<span data-ttu-id="fcdc5-117">Ścieżka, do której ma zastosowanie zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="fcdc5-118">Ścieżki indeksu zwykle zaczynają się od katalogu głównego i kończą się symbolami wieloznacznymi (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="fcdc5-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="fcdc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdc5-119">CommonParameters</span></span>
<span data-ttu-id="fcdc5-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdc5-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcdc5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdc5-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcdc5-122">INPUTS</span></span>

### <span data-ttu-id="fcdc5-123">Brak</span><span class="sxs-lookup"><span data-stu-id="fcdc5-123">None</span></span>

## <span data-ttu-id="fcdc5-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcdc5-124">OUTPUTS</span></span>

### <span data-ttu-id="fcdc5-125">Microsoft.Azure.Commands.Dosdb.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="fcdc5-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="fcdc5-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcdc5-126">NOTES</span></span>

## <span data-ttu-id="fcdc5-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcdc5-127">RELATED LINKS</span></span>
