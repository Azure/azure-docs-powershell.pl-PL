---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181307"
---
# <span data-ttu-id="9297a-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="9297a-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="9297a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9297a-102">SYNOPSIS</span></span>
<span data-ttu-id="9297a-103">Tworzy nowy obiekt typu PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="9297a-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="9297a-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="9297a-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="9297a-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9297a-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9297a-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="9297a-106">DESCRIPTION</span></span>
<span data-ttu-id="9297a-107">Obiekt odpowiadający projektowi CompositePath interfejsu API języka Sql.</span><span class="sxs-lookup"><span data-stu-id="9297a-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="9297a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9297a-108">EXAMPLES</span></span>

### <span data-ttu-id="9297a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9297a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="9297a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9297a-110">PARAMETERS</span></span>

### <span data-ttu-id="9297a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9297a-111">-DefaultProfile</span></span>
<span data-ttu-id="9297a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9297a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9297a-113">— Zamówienie</span><span class="sxs-lookup"><span data-stu-id="9297a-113">-Order</span></span>
<span data-ttu-id="9297a-114">Pobiera lub ustawia kolejność sortowania dla ścieżek złożonych.</span><span class="sxs-lookup"><span data-stu-id="9297a-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="9297a-115">Możliwe wartości: "Rosnąco", "Malejąco"</span><span class="sxs-lookup"><span data-stu-id="9297a-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="9297a-116">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="9297a-116">-Path</span></span>
<span data-ttu-id="9297a-117">Ścieżka, do której ma zastosowanie zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="9297a-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="9297a-118">Ścieżki indeksu zazwyczaj zaczynają się od katalogu głównego i kończą się symbolami wieloznacznymi (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="9297a-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="9297a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9297a-119">CommonParameters</span></span>
<span data-ttu-id="9297a-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9297a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9297a-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9297a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9297a-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9297a-122">INPUTS</span></span>

### <span data-ttu-id="9297a-123">Brak</span><span class="sxs-lookup"><span data-stu-id="9297a-123">None</span></span>

## <span data-ttu-id="9297a-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9297a-124">OUTPUTS</span></span>

### <span data-ttu-id="9297a-125">Microsoft.Azure.Commands.Dosdb.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="9297a-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="9297a-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9297a-126">NOTES</span></span>

## <span data-ttu-id="9297a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9297a-127">RELATED LINKS</span></span>
