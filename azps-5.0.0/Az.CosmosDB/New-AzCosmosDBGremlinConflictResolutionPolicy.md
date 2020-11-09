---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307105"
---
# <span data-ttu-id="e7038-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7038-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="e7038-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7038-102">SYNOPSIS</span></span>
<span data-ttu-id="e7038-103">Tworzy nowy obiekt typu PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7038-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="e7038-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="e7038-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="e7038-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7038-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7038-106">Opis</span><span class="sxs-lookup"><span data-stu-id="e7038-106">DESCRIPTION</span></span>
<span data-ttu-id="e7038-107">Obiekt odpowiadający ConflictResolutionPolicy API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e7038-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="e7038-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7038-108">EXAMPLES</span></span>

### <span data-ttu-id="e7038-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7038-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="e7038-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7038-110">PARAMETERS</span></span>

### <span data-ttu-id="e7038-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="e7038-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="e7038-112">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="e7038-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="e7038-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7038-113">-DefaultProfile</span></span>
<span data-ttu-id="e7038-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7038-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7038-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e7038-115">-Path</span></span>
<span data-ttu-id="e7038-116">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="e7038-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="e7038-117">-Type</span><span class="sxs-lookup"><span data-stu-id="e7038-117">-Type</span></span>
<span data-ttu-id="e7038-118">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="e7038-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="e7038-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7038-119">CommonParameters</span></span>
<span data-ttu-id="e7038-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7038-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7038-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7038-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7038-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7038-122">INPUTS</span></span>

### <span data-ttu-id="e7038-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e7038-123">None</span></span>

## <span data-ttu-id="e7038-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7038-124">OUTPUTS</span></span>

### <span data-ttu-id="e7038-125">Microsoft. Azure. Commands. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7038-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="e7038-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7038-126">NOTES</span></span>

## <span data-ttu-id="e7038-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7038-127">RELATED LINKS</span></span>
