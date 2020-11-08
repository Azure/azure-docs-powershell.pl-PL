---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062938"
---
# <span data-ttu-id="ac89f-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ac89f-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="ac89f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac89f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac89f-103">Aktualizuje serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ac89f-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="ac89f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac89f-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac89f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac89f-105">DESCRIPTION</span></span>
<span data-ttu-id="ac89f-106">Polecenie cmdlet **Set-AzCdnOrigin** aktualizuje serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="ac89f-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="ac89f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac89f-107">EXAMPLES</span></span>

## <span data-ttu-id="ac89f-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac89f-108">PARAMETERS</span></span>

### <span data-ttu-id="ac89f-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ac89f-109">-CdnOrigin</span></span>
<span data-ttu-id="ac89f-110">Określa serwer pochodzenia, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac89f-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac89f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac89f-111">-DefaultProfile</span></span>
<span data-ttu-id="ac89f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ac89f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac89f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac89f-113">CommonParameters</span></span>
<span data-ttu-id="ac89f-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac89f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac89f-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac89f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac89f-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac89f-116">INPUTS</span></span>

### <span data-ttu-id="ac89f-117">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ac89f-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="ac89f-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac89f-118">OUTPUTS</span></span>

### <span data-ttu-id="ac89f-119">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ac89f-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="ac89f-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac89f-120">NOTES</span></span>

## <span data-ttu-id="ac89f-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac89f-121">RELATED LINKS</span></span>

[<span data-ttu-id="ac89f-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ac89f-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


