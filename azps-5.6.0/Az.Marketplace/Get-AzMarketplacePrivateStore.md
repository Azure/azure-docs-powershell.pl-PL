---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: 2dd2ec778a64403b9f13cd923e7b7312e72a6c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003809"
---
# <span data-ttu-id="76aa0-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="76aa0-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="76aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="76aa0-103">Pobierz listę sklepu prywatnego</span><span class="sxs-lookup"><span data-stu-id="76aa0-103">Get private store list</span></span>

## <span data-ttu-id="76aa0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76aa0-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76aa0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="76aa0-106">Uzyskiwanie listy sklepu prywatnego utworzonej w ramach zakresu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="76aa0-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="76aa0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76aa0-107">EXAMPLES</span></span>

### <span data-ttu-id="76aa0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76aa0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="76aa0-109">lista sklepu prywatnego, która została utworzona w ramach zakresu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="76aa0-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="76aa0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76aa0-110">PARAMETERS</span></span>

### <span data-ttu-id="76aa0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76aa0-111">-DefaultProfile</span></span>
<span data-ttu-id="76aa0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76aa0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76aa0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76aa0-113">CommonParameters</span></span>
<span data-ttu-id="76aa0-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76aa0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76aa0-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76aa0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76aa0-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76aa0-116">INPUTS</span></span>

### <span data-ttu-id="76aa0-117">Brak</span><span class="sxs-lookup"><span data-stu-id="76aa0-117">None</span></span>

## <span data-ttu-id="76aa0-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76aa0-118">OUTPUTS</span></span>

### <span data-ttu-id="76aa0-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="76aa0-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="76aa0-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76aa0-120">NOTES</span></span>

## <span data-ttu-id="76aa0-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76aa0-121">RELATED LINKS</span></span>
