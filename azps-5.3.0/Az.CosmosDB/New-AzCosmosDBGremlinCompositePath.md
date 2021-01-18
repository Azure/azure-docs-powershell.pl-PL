---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501741"
---
# <span data-ttu-id="5f803-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="5f803-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="5f803-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f803-102">SYNOPSIS</span></span>
<span data-ttu-id="5f803-103">Tworzy nowy obiekt typu PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="5f803-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="5f803-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="5f803-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="5f803-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f803-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f803-106">Opis</span><span class="sxs-lookup"><span data-stu-id="5f803-106">DESCRIPTION</span></span>
<span data-ttu-id="5f803-107">Obiekt odpowiadający CompositePath API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5f803-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="5f803-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f803-108">EXAMPLES</span></span>

### <span data-ttu-id="5f803-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f803-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="5f803-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f803-110">PARAMETERS</span></span>

### <span data-ttu-id="5f803-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f803-111">-DefaultProfile</span></span>
<span data-ttu-id="5f803-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f803-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f803-113">-Order (kolejność)</span><span class="sxs-lookup"><span data-stu-id="5f803-113">-Order</span></span>
<span data-ttu-id="5f803-114">Pobiera lub ustawia kolejność sortowania ścieżek złożonych.</span><span class="sxs-lookup"><span data-stu-id="5f803-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="5f803-115">Możliwe wartości obejmują: "rosnąco", "malejąco"</span><span class="sxs-lookup"><span data-stu-id="5f803-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="5f803-116">-Path</span><span class="sxs-lookup"><span data-stu-id="5f803-116">-Path</span></span>
<span data-ttu-id="5f803-117">Ścieżka, do której odnosi się zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="5f803-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="5f803-118">Ścieżki indeksu zwykle zaczynają się od katalogu głównego i kończą się symbolem wieloznacznym (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="5f803-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="5f803-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f803-119">CommonParameters</span></span>
<span data-ttu-id="5f803-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f803-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f803-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f803-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f803-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f803-122">INPUTS</span></span>

### <span data-ttu-id="5f803-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5f803-123">None</span></span>

## <span data-ttu-id="5f803-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f803-124">OUTPUTS</span></span>

### <span data-ttu-id="5f803-125">Microsoft. Azure. Commands. CosmosDB. models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="5f803-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="5f803-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f803-126">NOTES</span></span>

## <span data-ttu-id="5f803-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f803-127">RELATED LINKS</span></span>
