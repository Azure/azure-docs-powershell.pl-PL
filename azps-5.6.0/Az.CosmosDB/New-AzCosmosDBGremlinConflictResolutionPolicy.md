---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007969"
---
# <span data-ttu-id="9db63-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9db63-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="9db63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9db63-102">SYNOPSIS</span></span>
<span data-ttu-id="9db63-103">Tworzy nowy obiekt typu PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9db63-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="9db63-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="9db63-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="9db63-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9db63-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9db63-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="9db63-106">DESCRIPTION</span></span>
<span data-ttu-id="9db63-107">Obiekt odpowiadający interfejsowi API Gremlin conflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9db63-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="9db63-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9db63-108">EXAMPLES</span></span>

### <span data-ttu-id="9db63-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9db63-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="9db63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9db63-110">PARAMETERS</span></span>

### <span data-ttu-id="9db63-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="9db63-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="9db63-112">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="9db63-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="9db63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-113">-DefaultProfile</span></span>
<span data-ttu-id="9db63-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9db63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db63-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="9db63-115">-Path</span></span>
<span data-ttu-id="9db63-116">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="9db63-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="9db63-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="9db63-117">-Type</span></span>
<span data-ttu-id="9db63-118">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="9db63-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="9db63-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db63-119">CommonParameters</span></span>
<span data-ttu-id="9db63-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db63-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db63-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9db63-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db63-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9db63-122">INPUTS</span></span>

### <span data-ttu-id="9db63-123">Brak</span><span class="sxs-lookup"><span data-stu-id="9db63-123">None</span></span>

## <span data-ttu-id="9db63-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9db63-124">OUTPUTS</span></span>

### <span data-ttu-id="9db63-125">Microsoft.Azure.Commands.DoceńDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9db63-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="9db63-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9db63-126">NOTES</span></span>

## <span data-ttu-id="9db63-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9db63-127">RELATED LINKS</span></span>
