---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221346"
---
# <span data-ttu-id="65050-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="65050-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="65050-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65050-102">SYNOPSIS</span></span>
<span data-ttu-id="65050-103">Tworzy nowy obiekt typu PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="65050-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="65050-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="65050-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="65050-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65050-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65050-106">Opis</span><span class="sxs-lookup"><span data-stu-id="65050-106">DESCRIPTION</span></span>
<span data-ttu-id="65050-107">Obiekt odpowiadający ConflictResolutionPolicy API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="65050-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="65050-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65050-108">EXAMPLES</span></span>

### <span data-ttu-id="65050-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65050-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="65050-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65050-110">PARAMETERS</span></span>

### <span data-ttu-id="65050-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="65050-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="65050-112">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="65050-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="65050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65050-113">-DefaultProfile</span></span>
<span data-ttu-id="65050-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65050-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65050-115">-Path</span><span class="sxs-lookup"><span data-stu-id="65050-115">-Path</span></span>
<span data-ttu-id="65050-116">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="65050-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="65050-117">-Type</span><span class="sxs-lookup"><span data-stu-id="65050-117">-Type</span></span>
<span data-ttu-id="65050-118">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="65050-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="65050-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65050-119">CommonParameters</span></span>
<span data-ttu-id="65050-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65050-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65050-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65050-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65050-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65050-122">INPUTS</span></span>

### <span data-ttu-id="65050-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="65050-123">None</span></span>

## <span data-ttu-id="65050-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65050-124">OUTPUTS</span></span>

### <span data-ttu-id="65050-125">Microsoft. Azure. Commands. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="65050-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="65050-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65050-126">NOTES</span></span>

## <span data-ttu-id="65050-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65050-127">RELATED LINKS</span></span>
