---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198962"
---
# <span data-ttu-id="ed27d-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed27d-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="ed27d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed27d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed27d-103">Tworzy nowy obiekt typu PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ed27d-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="ed27d-104">Może być przekazywana jako wartość parametru Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="ed27d-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="ed27d-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed27d-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed27d-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed27d-106">DESCRIPTION</span></span>
<span data-ttu-id="ed27d-107">Obiekt odpowiadający obiektowi interfejsu API Sql ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ed27d-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="ed27d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed27d-108">EXAMPLES</span></span>

### <span data-ttu-id="ed27d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed27d-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="ed27d-110">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="ed27d-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="ed27d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed27d-111">PARAMETERS</span></span>

### <span data-ttu-id="ed27d-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="ed27d-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="ed27d-113">Do podanych, gdy typ jest niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="ed27d-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="ed27d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed27d-114">-DefaultProfile</span></span>
<span data-ttu-id="ed27d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed27d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed27d-116">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="ed27d-116">-Path</span></span>
<span data-ttu-id="ed27d-117">Ma być podany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="ed27d-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="ed27d-118">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="ed27d-118">-Type</span></span>
<span data-ttu-id="ed27d-119">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ed27d-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="ed27d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed27d-120">CommonParameters</span></span>
<span data-ttu-id="ed27d-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed27d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed27d-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed27d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed27d-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed27d-123">INPUTS</span></span>

### <span data-ttu-id="ed27d-124">Brak</span><span class="sxs-lookup"><span data-stu-id="ed27d-124">None</span></span>

## <span data-ttu-id="ed27d-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed27d-125">OUTPUTS</span></span>

### <span data-ttu-id="ed27d-126">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ed27d-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="ed27d-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed27d-127">NOTES</span></span>

## <span data-ttu-id="ed27d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed27d-128">RELATED LINKS</span></span>
