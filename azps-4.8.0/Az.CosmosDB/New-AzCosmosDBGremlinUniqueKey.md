---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224056"
---
# <span data-ttu-id="0b0c8-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0b0c8-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="0b0c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0c8-103">Tworzy nowy obiekt UniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0b0c8-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="0b0c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b0c8-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b0c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b0c8-105">DESCRIPTION</span></span>
<span data-ttu-id="0b0c8-106">Polecenie cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** tworzy nowy obiekt typu PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="0b0c8-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="0b0c8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b0c8-107">EXAMPLES</span></span>

### <span data-ttu-id="0b0c8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b0c8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="0b0c8-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b0c8-109">PARAMETERS</span></span>

### <span data-ttu-id="0b0c8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0c8-110">-DefaultProfile</span></span>
<span data-ttu-id="0b0c8-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b0c8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0c8-112">-Path</span><span class="sxs-lookup"><span data-stu-id="0b0c8-112">-Path</span></span>
<span data-ttu-id="0b0c8-113">Tablica ciągów wartości ścieżki</span><span class="sxs-lookup"><span data-stu-id="0b0c8-113">Array of string of path values</span></span>

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

### <span data-ttu-id="0b0c8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0c8-114">CommonParameters</span></span>
<span data-ttu-id="0b0c8-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0c8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0c8-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b0c8-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0c8-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b0c8-117">INPUTS</span></span>

### <span data-ttu-id="0b0c8-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0b0c8-118">None</span></span>

## <span data-ttu-id="0b0c8-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b0c8-119">OUTPUTS</span></span>

### <span data-ttu-id="0b0c8-120">Microsoft. Azure. Commands. CosmosDB. models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0b0c8-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="0b0c8-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b0c8-121">NOTES</span></span>

## <span data-ttu-id="0b0c8-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b0c8-122">RELATED LINKS</span></span>
