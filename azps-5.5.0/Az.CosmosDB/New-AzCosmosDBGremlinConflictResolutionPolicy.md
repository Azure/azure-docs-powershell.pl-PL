---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198963"
---
# <span data-ttu-id="67064-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="67064-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="67064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67064-102">SYNOPSIS</span></span>
<span data-ttu-id="67064-103">Tworzy nowy obiekt typu PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="67064-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="67064-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="67064-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="67064-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67064-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67064-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="67064-106">DESCRIPTION</span></span>
<span data-ttu-id="67064-107">Obiekt odpowiadający interfejsowi API Gremlin conflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="67064-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="67064-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67064-108">EXAMPLES</span></span>

### <span data-ttu-id="67064-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67064-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="67064-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67064-110">PARAMETERS</span></span>

### <span data-ttu-id="67064-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="67064-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="67064-112">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="67064-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="67064-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67064-113">-DefaultProfile</span></span>
<span data-ttu-id="67064-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67064-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67064-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="67064-115">-Path</span></span>
<span data-ttu-id="67064-116">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="67064-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="67064-117">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="67064-117">-Type</span></span>
<span data-ttu-id="67064-118">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="67064-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="67064-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67064-119">CommonParameters</span></span>
<span data-ttu-id="67064-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67064-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67064-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67064-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67064-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67064-122">INPUTS</span></span>

### <span data-ttu-id="67064-123">Brak</span><span class="sxs-lookup"><span data-stu-id="67064-123">None</span></span>

## <span data-ttu-id="67064-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67064-124">OUTPUTS</span></span>

### <span data-ttu-id="67064-125">Microsoft.Azure.Commands.DoceńDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="67064-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="67064-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67064-126">NOTES</span></span>

## <span data-ttu-id="67064-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67064-127">RELATED LINKS</span></span>
