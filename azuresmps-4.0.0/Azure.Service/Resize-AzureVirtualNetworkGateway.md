---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055052"
---
# <span data-ttu-id="d383e-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d383e-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="d383e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d383e-102">SYNOPSIS</span></span>
<span data-ttu-id="d383e-103">Zmienia rozmiar bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d383e-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="d383e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d383e-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d383e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d383e-105">DESCRIPTION</span></span>
<span data-ttu-id="d383e-106">Polecenie cmdlet Resize-AzureVirtualNetworkGateway zmienia rozmiar bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d383e-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="d383e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d383e-107">EXAMPLES</span></span>

## <span data-ttu-id="d383e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d383e-108">PARAMETERS</span></span>

### <span data-ttu-id="d383e-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d383e-109">-GatewayId</span></span>
<span data-ttu-id="d383e-110">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="d383e-110">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d383e-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="d383e-111">-GatewaySKU</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d383e-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="d383e-112">-Profile</span></span>
<span data-ttu-id="d383e-113">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d383e-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d383e-114">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d383e-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d383e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d383e-115">CommonParameters</span></span>
<span data-ttu-id="d383e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d383e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d383e-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d383e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d383e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d383e-118">INPUTS</span></span>

## <span data-ttu-id="d383e-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d383e-119">OUTPUTS</span></span>

## <span data-ttu-id="d383e-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d383e-120">NOTES</span></span>

## <span data-ttu-id="d383e-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d383e-121">RELATED LINKS</span></span>

[<span data-ttu-id="d383e-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d383e-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d383e-123">Nowe — AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d383e-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d383e-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d383e-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="d383e-125">Resetowanie — AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d383e-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


