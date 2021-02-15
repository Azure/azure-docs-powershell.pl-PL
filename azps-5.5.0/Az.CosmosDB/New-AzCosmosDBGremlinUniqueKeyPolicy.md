---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196794"
---
# <span data-ttu-id="eef7e-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="eef7e-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="eef7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef7e-102">SYNOPSIS</span></span>
<span data-ttu-id="eef7e-103">Tworzy nowy obiekt ADB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="eef7e-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="eef7e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eef7e-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eef7e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="eef7e-105">DESCRIPTION</span></span>
<span data-ttu-id="eef7e-106">Polecenie cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** tworzy nowy obiekt typu PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="eef7e-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="eef7e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eef7e-107">EXAMPLES</span></span>

### <span data-ttu-id="eef7e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eef7e-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="eef7e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eef7e-109">PARAMETERS</span></span>

### <span data-ttu-id="eef7e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef7e-110">-DefaultProfile</span></span>
<span data-ttu-id="eef7e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eef7e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef7e-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="eef7e-112">-UniqueKey</span></span>
<span data-ttu-id="eef7e-113">Tablica obiektów typu PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="eef7e-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="eef7e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef7e-114">CommonParameters</span></span>
<span data-ttu-id="eef7e-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef7e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef7e-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eef7e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef7e-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eef7e-117">INPUTS</span></span>

### <span data-ttu-id="eef7e-118">Brak</span><span class="sxs-lookup"><span data-stu-id="eef7e-118">None</span></span>

## <span data-ttu-id="eef7e-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eef7e-119">OUTPUTS</span></span>

### <span data-ttu-id="eef7e-120">Microsoft.Azure.Commands.Dosdb.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="eef7e-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="eef7e-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eef7e-121">NOTES</span></span>

## <span data-ttu-id="eef7e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eef7e-122">RELATED LINKS</span></span>
