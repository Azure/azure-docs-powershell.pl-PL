---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329893"
---
# <span data-ttu-id="2347c-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="2347c-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="2347c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2347c-102">SYNOPSIS</span></span>
<span data-ttu-id="2347c-103">Pobierz prywatną listę sklepów</span><span class="sxs-lookup"><span data-stu-id="2347c-103">Get private store list</span></span>

## <span data-ttu-id="2347c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2347c-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2347c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2347c-105">DESCRIPTION</span></span>
<span data-ttu-id="2347c-106">Pobieranie listy sklepów prywatnych, które zostały utworzone w ramach zakresu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="2347c-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="2347c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2347c-107">EXAMPLES</span></span>

### <span data-ttu-id="2347c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2347c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="2347c-109">Lista sklepów prywatnych, które zostały utworzone w ramach zakresu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="2347c-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="2347c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2347c-110">PARAMETERS</span></span>

### <span data-ttu-id="2347c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2347c-111">-DefaultProfile</span></span>
<span data-ttu-id="2347c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2347c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2347c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2347c-113">CommonParameters</span></span>
<span data-ttu-id="2347c-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2347c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2347c-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2347c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2347c-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2347c-116">INPUTS</span></span>

### <span data-ttu-id="2347c-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2347c-117">None</span></span>

## <span data-ttu-id="2347c-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2347c-118">OUTPUTS</span></span>

### <span data-ttu-id="2347c-119">Microsoft. Azure. Commands. Marketplace. modele. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="2347c-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="2347c-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2347c-120">NOTES</span></span>

## <span data-ttu-id="2347c-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2347c-121">RELATED LINKS</span></span>
