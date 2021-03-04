---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957441"
---
# <span data-ttu-id="c93d3-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c93d3-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="c93d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c93d3-103">Tworzy nowy obiekt ADB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c93d3-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="c93d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c93d3-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c93d3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c93d3-105">DESCRIPTION</span></span>
<span data-ttu-id="c93d3-106">Polecenie cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** tworzy nowy obiekt typu PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c93d3-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="c93d3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c93d3-107">EXAMPLES</span></span>

### <span data-ttu-id="c93d3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c93d3-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="c93d3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c93d3-109">PARAMETERS</span></span>

### <span data-ttu-id="c93d3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93d3-110">-DefaultProfile</span></span>
<span data-ttu-id="c93d3-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c93d3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c93d3-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="c93d3-112">-UniqueKey</span></span>
<span data-ttu-id="c93d3-113">Tablica obiektów typu PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="c93d3-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93d3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93d3-114">CommonParameters</span></span>
<span data-ttu-id="c93d3-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93d3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93d3-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c93d3-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93d3-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c93d3-117">INPUTS</span></span>

### <span data-ttu-id="c93d3-118">Brak</span><span class="sxs-lookup"><span data-stu-id="c93d3-118">None</span></span>

## <span data-ttu-id="c93d3-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c93d3-119">OUTPUTS</span></span>

### <span data-ttu-id="c93d3-120">Microsoft.Azure.Commands.Dosdb.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c93d3-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="c93d3-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c93d3-121">NOTES</span></span>

## <span data-ttu-id="c93d3-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c93d3-122">RELATED LINKS</span></span>
