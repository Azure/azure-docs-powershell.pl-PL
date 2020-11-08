---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224055"
---
# <span data-ttu-id="81126-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="81126-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="81126-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81126-102">SYNOPSIS</span></span>
<span data-ttu-id="81126-103">Tworzy nowy obiekt typu PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="81126-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="81126-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="81126-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="81126-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81126-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81126-106">Opis</span><span class="sxs-lookup"><span data-stu-id="81126-106">DESCRIPTION</span></span>
<span data-ttu-id="81126-107">Obiekt odpowiadający CompositePath API funkcji SQL.</span><span class="sxs-lookup"><span data-stu-id="81126-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="81126-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81126-108">EXAMPLES</span></span>

### <span data-ttu-id="81126-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81126-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="81126-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81126-110">PARAMETERS</span></span>

### <span data-ttu-id="81126-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81126-111">-DefaultProfile</span></span>
<span data-ttu-id="81126-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81126-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81126-113">-Order (kolejność)</span><span class="sxs-lookup"><span data-stu-id="81126-113">-Order</span></span>
<span data-ttu-id="81126-114">Pobiera lub ustawia kolejność sortowania ścieżek złożonych.</span><span class="sxs-lookup"><span data-stu-id="81126-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="81126-115">Możliwe wartości obejmują: "rosnąco", "malejąco"</span><span class="sxs-lookup"><span data-stu-id="81126-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="81126-116">-Path</span><span class="sxs-lookup"><span data-stu-id="81126-116">-Path</span></span>
<span data-ttu-id="81126-117">Ścieżka, do której odnosi się zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="81126-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="81126-118">Ścieżki indeksu zwykle zaczynają się od katalogu głównego i kończą się symbolem wieloznacznym (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="81126-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="81126-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81126-119">CommonParameters</span></span>
<span data-ttu-id="81126-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81126-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81126-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81126-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81126-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81126-122">INPUTS</span></span>

### <span data-ttu-id="81126-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="81126-123">None</span></span>

## <span data-ttu-id="81126-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81126-124">OUTPUTS</span></span>

### <span data-ttu-id="81126-125">Microsoft. Azure. Commands. CosmosDB. models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="81126-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="81126-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81126-126">NOTES</span></span>

## <span data-ttu-id="81126-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81126-127">RELATED LINKS</span></span>
