---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062840"
---
# <span data-ttu-id="8a933-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="8a933-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="8a933-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a933-102">SYNOPSIS</span></span>
<span data-ttu-id="8a933-103">Tworzy nowy obiekt typu PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="8a933-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="8a933-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="8a933-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="8a933-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a933-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a933-106">Opis</span><span class="sxs-lookup"><span data-stu-id="8a933-106">DESCRIPTION</span></span>
<span data-ttu-id="8a933-107">Obiekt odpowiadający IncludedPath API funkcji SQL.</span><span class="sxs-lookup"><span data-stu-id="8a933-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="8a933-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a933-108">EXAMPLES</span></span>

### <span data-ttu-id="8a933-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a933-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="8a933-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a933-110">PARAMETERS</span></span>

### <span data-ttu-id="8a933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a933-111">-DefaultProfile</span></span>
<span data-ttu-id="8a933-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a933-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a933-113">-Index</span><span class="sxs-lookup"><span data-stu-id="8a933-113">-Index</span></span>
<span data-ttu-id="8a933-114">Lista indeksów dla tej ścieżki</span><span class="sxs-lookup"><span data-stu-id="8a933-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="8a933-115">-Path</span><span class="sxs-lookup"><span data-stu-id="8a933-115">-Path</span></span>
<span data-ttu-id="8a933-116">Ścieżka, do której odnosi się zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="8a933-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="8a933-117">Ścieżki indeksu zwykle zaczynają się od katalogu głównego i kończą się symbolem wieloznacznym (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="8a933-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="8a933-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a933-118">CommonParameters</span></span>
<span data-ttu-id="8a933-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a933-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a933-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a933-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a933-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a933-121">INPUTS</span></span>

### <span data-ttu-id="8a933-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8a933-122">None</span></span>

## <span data-ttu-id="8a933-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a933-123">OUTPUTS</span></span>

### <span data-ttu-id="8a933-124">Microsoft. Azure. Commands. CosmosDB. models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="8a933-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="8a933-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a933-125">NOTES</span></span>

## <span data-ttu-id="8a933-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a933-126">RELATED LINKS</span></span>
