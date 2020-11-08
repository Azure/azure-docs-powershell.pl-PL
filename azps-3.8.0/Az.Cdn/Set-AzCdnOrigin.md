---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051798"
---
# <span data-ttu-id="9bfbe-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9bfbe-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="9bfbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfbe-103">Aktualizuje serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="9bfbe-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="9bfbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bfbe-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bfbe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9bfbe-105">DESCRIPTION</span></span>
<span data-ttu-id="9bfbe-106">Polecenie cmdlet **Set-AzCdnOrigin** aktualizuje serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="9bfbe-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="9bfbe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bfbe-107">EXAMPLES</span></span>

## <span data-ttu-id="9bfbe-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bfbe-108">PARAMETERS</span></span>

### <span data-ttu-id="9bfbe-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9bfbe-109">-CdnOrigin</span></span>
<span data-ttu-id="9bfbe-110">Określa serwer pochodzenia, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bfbe-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9bfbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfbe-111">-DefaultProfile</span></span>
<span data-ttu-id="9bfbe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9bfbe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bfbe-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfbe-113">CommonParameters</span></span>
<span data-ttu-id="9bfbe-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bfbe-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfbe-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bfbe-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfbe-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bfbe-116">INPUTS</span></span>

### <span data-ttu-id="9bfbe-117">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9bfbe-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9bfbe-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bfbe-118">OUTPUTS</span></span>

### <span data-ttu-id="9bfbe-119">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9bfbe-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9bfbe-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bfbe-120">NOTES</span></span>

## <span data-ttu-id="9bfbe-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bfbe-121">RELATED LINKS</span></span>

[<span data-ttu-id="9bfbe-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9bfbe-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


