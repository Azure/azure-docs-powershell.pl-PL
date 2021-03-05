---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998789"
---
# <span data-ttu-id="2c793-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="2c793-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="2c793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c793-102">SYNOPSIS</span></span>
<span data-ttu-id="2c793-103">Tworzy nowy obiekt ADB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="2c793-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="2c793-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c793-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c793-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c793-105">DESCRIPTION</span></span>
<span data-ttu-id="2c793-106">Polecenie cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** tworzy nowy obiekt typu PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="2c793-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="2c793-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c793-107">EXAMPLES</span></span>

### <span data-ttu-id="2c793-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c793-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="2c793-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c793-109">PARAMETERS</span></span>

### <span data-ttu-id="2c793-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c793-110">-DefaultProfile</span></span>
<span data-ttu-id="2c793-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c793-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c793-112">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="2c793-112">-Path</span></span>
<span data-ttu-id="2c793-113">Tablica ciągów wartości ścieżek</span><span class="sxs-lookup"><span data-stu-id="2c793-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c793-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c793-114">CommonParameters</span></span>
<span data-ttu-id="2c793-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c793-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c793-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c793-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c793-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c793-117">INPUTS</span></span>

### <span data-ttu-id="2c793-118">Brak</span><span class="sxs-lookup"><span data-stu-id="2c793-118">None</span></span>

## <span data-ttu-id="2c793-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c793-119">OUTPUTS</span></span>

### <span data-ttu-id="2c793-120">Microsoft.Azure.Commands.Dosdb.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="2c793-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="2c793-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c793-121">NOTES</span></span>

## <span data-ttu-id="2c793-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c793-122">RELATED LINKS</span></span>
