---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196778"
---
# <span data-ttu-id="f04b5-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="f04b5-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="f04b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f04b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f04b5-103">Tworzy nowy indeks ADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f04b5-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="f04b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f04b5-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f04b5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f04b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f04b5-106">**New-AzCosmosDBMongoDBIndex** tworzy nowy indeks AADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="f04b5-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="f04b5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f04b5-107">EXAMPLES</span></span>

### <span data-ttu-id="f04b5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f04b5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="f04b5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f04b5-109">PARAMETERS</span></span>

### <span data-ttu-id="f04b5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04b5-110">-DefaultProfile</span></span>
<span data-ttu-id="f04b5-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f04b5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f04b5-112">- Key</span><span class="sxs-lookup"><span data-stu-id="f04b5-112">-Key</span></span>
<span data-ttu-id="f04b5-113">Tablica wartości klucza jako ciągów.</span><span class="sxs-lookup"><span data-stu-id="f04b5-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="f04b5-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f04b5-114">-TtlInSeconds</span></span>
<span data-ttu-id="f04b5-115">Liczba sekund, po których indeks wygasa.</span><span class="sxs-lookup"><span data-stu-id="f04b5-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="f04b5-116">— Unikatowe</span><span class="sxs-lookup"><span data-stu-id="f04b5-116">-Unique</span></span>
<span data-ttu-id="f04b5-117">Wartość logiczna wskazująca, czy indeks jest unikatowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="f04b5-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="f04b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04b5-118">CommonParameters</span></span>
<span data-ttu-id="f04b5-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f04b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04b5-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f04b5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04b5-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f04b5-121">INPUTS</span></span>

### <span data-ttu-id="f04b5-122">Brak</span><span class="sxs-lookup"><span data-stu-id="f04b5-122">None</span></span>

## <span data-ttu-id="f04b5-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f04b5-123">OUTPUTS</span></span>

### <span data-ttu-id="f04b5-124">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="f04b5-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="f04b5-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f04b5-125">NOTES</span></span>

## <span data-ttu-id="f04b5-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f04b5-126">RELATED LINKS</span></span>
