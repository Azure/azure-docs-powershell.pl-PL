---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991446"
---
# <span data-ttu-id="53850-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="53850-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="53850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53850-102">SYNOPSIS</span></span>
<span data-ttu-id="53850-103">Tworzy nowy indeks ADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="53850-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="53850-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53850-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53850-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="53850-105">DESCRIPTION</span></span>
<span data-ttu-id="53850-106">**New-AzCosmosDBMongoDBIndex** tworzy nowy indeks AADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="53850-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="53850-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53850-107">EXAMPLES</span></span>

### <span data-ttu-id="53850-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53850-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="53850-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53850-109">PARAMETERS</span></span>

### <span data-ttu-id="53850-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53850-110">-DefaultProfile</span></span>
<span data-ttu-id="53850-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53850-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53850-112">- Key</span><span class="sxs-lookup"><span data-stu-id="53850-112">-Key</span></span>
<span data-ttu-id="53850-113">Tablica wartości klucza jako ciągów.</span><span class="sxs-lookup"><span data-stu-id="53850-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53850-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="53850-114">-TtlInSeconds</span></span>
<span data-ttu-id="53850-115">Liczba sekund, po których indeks wygasa.</span><span class="sxs-lookup"><span data-stu-id="53850-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53850-116">— Unikatowe</span><span class="sxs-lookup"><span data-stu-id="53850-116">-Unique</span></span>
<span data-ttu-id="53850-117">Wartość logiczna wskazująca, czy indeks jest unikatowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="53850-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53850-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53850-118">CommonParameters</span></span>
<span data-ttu-id="53850-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53850-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53850-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53850-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53850-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53850-121">INPUTS</span></span>

### <span data-ttu-id="53850-122">Brak</span><span class="sxs-lookup"><span data-stu-id="53850-122">None</span></span>

## <span data-ttu-id="53850-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53850-123">OUTPUTS</span></span>

### <span data-ttu-id="53850-124">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="53850-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="53850-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53850-125">NOTES</span></span>

## <span data-ttu-id="53850-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53850-126">RELATED LINKS</span></span>
