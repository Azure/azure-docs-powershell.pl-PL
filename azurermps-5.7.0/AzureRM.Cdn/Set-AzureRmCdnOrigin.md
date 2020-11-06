---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 179b4b028c7dd9338e75d07f559a61052b3d2bcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527010"
---
# <span data-ttu-id="89142-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="89142-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="89142-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89142-102">SYNOPSIS</span></span>
<span data-ttu-id="89142-103">Aktualizuje serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="89142-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89142-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89142-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89142-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89142-105">DESCRIPTION</span></span>
<span data-ttu-id="89142-106">Polecenie cmdlet **Set-AzureRmCdnOrigin** aktualizuje serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="89142-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="89142-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89142-107">EXAMPLES</span></span>

## <span data-ttu-id="89142-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89142-108">PARAMETERS</span></span>

### <span data-ttu-id="89142-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="89142-109">-CdnOrigin</span></span>
<span data-ttu-id="89142-110">Określa serwer pochodzenia, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89142-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89142-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89142-111">-DefaultProfile</span></span>
<span data-ttu-id="89142-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="89142-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89142-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89142-113">CommonParameters</span></span>
<span data-ttu-id="89142-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89142-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89142-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89142-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89142-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89142-116">INPUTS</span></span>

### <span data-ttu-id="89142-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="89142-117">PSOrigin</span></span>
<span data-ttu-id="89142-118">Parametr "CdnOrigin' akceptuje wartość typu" PSOrigin' z rurociągu</span><span class="sxs-lookup"><span data-stu-id="89142-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="89142-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89142-119">OUTPUTS</span></span>

### <span data-ttu-id="89142-120">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="89142-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="89142-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89142-121">NOTES</span></span>

## <span data-ttu-id="89142-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89142-122">RELATED LINKS</span></span>

[<span data-ttu-id="89142-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="89142-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


