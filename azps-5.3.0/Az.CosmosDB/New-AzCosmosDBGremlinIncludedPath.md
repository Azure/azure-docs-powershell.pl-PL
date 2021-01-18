---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501738"
---
# <span data-ttu-id="bcfce-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="bcfce-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="bcfce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcfce-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfce-103">Tworzy nowy obiekt typu PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="bcfce-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="bcfce-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="bcfce-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="bcfce-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcfce-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcfce-106">Opis</span><span class="sxs-lookup"><span data-stu-id="bcfce-106">DESCRIPTION</span></span>
<span data-ttu-id="bcfce-107">Obiekt odpowiadający IncludedPath API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="bcfce-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="bcfce-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcfce-108">EXAMPLES</span></span>

### <span data-ttu-id="bcfce-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bcfce-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="bcfce-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcfce-110">PARAMETERS</span></span>

### <span data-ttu-id="bcfce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfce-111">-DefaultProfile</span></span>
<span data-ttu-id="bcfce-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcfce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcfce-113">-Index</span><span class="sxs-lookup"><span data-stu-id="bcfce-113">-Index</span></span>
<span data-ttu-id="bcfce-114">Lista indeksów dla tej ścieżki</span><span class="sxs-lookup"><span data-stu-id="bcfce-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="bcfce-115">-Path</span><span class="sxs-lookup"><span data-stu-id="bcfce-115">-Path</span></span>
<span data-ttu-id="bcfce-116">Ścieżka, do której odnosi się zachowanie indeksowania.</span><span class="sxs-lookup"><span data-stu-id="bcfce-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="bcfce-117">Ścieżki indeksu zwykle zaczynają się od katalogu głównego i kończą się symbolem wieloznacznym (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="bcfce-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="bcfce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfce-118">CommonParameters</span></span>
<span data-ttu-id="bcfce-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcfce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfce-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcfce-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfce-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcfce-121">INPUTS</span></span>

### <span data-ttu-id="bcfce-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bcfce-122">None</span></span>

## <span data-ttu-id="bcfce-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcfce-123">OUTPUTS</span></span>

### <span data-ttu-id="bcfce-124">Microsoft. Azure. Commands. CosmosDB. models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="bcfce-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="bcfce-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcfce-125">NOTES</span></span>

## <span data-ttu-id="bcfce-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcfce-126">RELATED LINKS</span></span>
