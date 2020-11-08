---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062849"
---
# <span data-ttu-id="a45a2-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a45a2-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="a45a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a45a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a45a2-103">Tworzy nowy obiekt UniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a45a2-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="a45a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a45a2-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a45a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a45a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a45a2-106">Polecenie cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** tworzy nowy obiekt typu PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="a45a2-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="a45a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a45a2-107">EXAMPLES</span></span>

### <span data-ttu-id="a45a2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a45a2-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="a45a2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a45a2-109">PARAMETERS</span></span>

### <span data-ttu-id="a45a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45a2-110">-DefaultProfile</span></span>
<span data-ttu-id="a45a2-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a45a2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a45a2-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="a45a2-112">-UniqueKey</span></span>
<span data-ttu-id="a45a2-113">Tablica obiektów typu PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="a45a2-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="a45a2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45a2-114">CommonParameters</span></span>
<span data-ttu-id="a45a2-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a45a2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45a2-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a45a2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45a2-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a45a2-117">INPUTS</span></span>

### <span data-ttu-id="a45a2-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a45a2-118">None</span></span>

## <span data-ttu-id="a45a2-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a45a2-119">OUTPUTS</span></span>

### <span data-ttu-id="a45a2-120">Microsoft. Azure. Commands. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a45a2-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="a45a2-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a45a2-121">NOTES</span></span>

## <span data-ttu-id="a45a2-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a45a2-122">RELATED LINKS</span></span>
