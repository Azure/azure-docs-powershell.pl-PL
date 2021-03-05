---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962433"
---
# <span data-ttu-id="c32de-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="c32de-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="c32de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32de-102">SYNOPSIS</span></span>
<span data-ttu-id="c32de-103">Tworzy nowy obiekt typu PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="c32de-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="c32de-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="c32de-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="c32de-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c32de-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c32de-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="c32de-106">DESCRIPTION</span></span>
<span data-ttu-id="c32de-107">Obiekt odpowiadający obiektowi IncludedPath interfejsu API SQL.</span><span class="sxs-lookup"><span data-stu-id="c32de-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="c32de-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c32de-108">EXAMPLES</span></span>

### <span data-ttu-id="c32de-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c32de-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="c32de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c32de-110">PARAMETERS</span></span>

### <span data-ttu-id="c32de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32de-111">-DefaultProfile</span></span>
<span data-ttu-id="c32de-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c32de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c32de-113">-Index</span><span class="sxs-lookup"><span data-stu-id="c32de-113">-Index</span></span>
<span data-ttu-id="c32de-114">Lista indeksów dla tej ścieżki</span><span class="sxs-lookup"><span data-stu-id="c32de-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="c32de-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="c32de-115">-Path</span></span>
<span data-ttu-id="c32de-116">Ścieżka, do której ma zastosowanie zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="c32de-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="c32de-117">Ścieżki indeksu zwykle zaczynają się od katalogu głównego i kończą się symbolami wieloznacznymi (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="c32de-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="c32de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32de-118">CommonParameters</span></span>
<span data-ttu-id="c32de-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32de-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c32de-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32de-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c32de-121">INPUTS</span></span>

### <span data-ttu-id="c32de-122">Brak</span><span class="sxs-lookup"><span data-stu-id="c32de-122">None</span></span>

## <span data-ttu-id="c32de-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c32de-123">OUTPUTS</span></span>

### <span data-ttu-id="c32de-124">Microsoft.Azure.Commands.DoceńDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="c32de-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="c32de-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c32de-125">NOTES</span></span>

## <span data-ttu-id="c32de-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c32de-126">RELATED LINKS</span></span>
