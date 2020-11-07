---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899075"
---
# <span data-ttu-id="ed079-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="ed079-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed079-102">SYNOPSIS</span></span>
<span data-ttu-id="ed079-103">Modyfikuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="ed079-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed079-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed079-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed079-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed079-105">DESCRIPTION</span></span>
<span data-ttu-id="ed079-106">Polecenie cmdlet **Set-AzureRmLocalNetworkGateway** modyfikuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="ed079-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="ed079-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed079-107">EXAMPLES</span></span>

### <span data-ttu-id="ed079-108">1:1</span><span class="sxs-lookup"><span data-stu-id="ed079-108">1:</span></span>
```

```

## <span data-ttu-id="ed079-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed079-109">PARAMETERS</span></span>

### <span data-ttu-id="ed079-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed079-110">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed079-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed079-111">-AsJob</span></span>
<span data-ttu-id="ed079-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ed079-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed079-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="ed079-113">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed079-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ed079-114">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed079-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed079-115">-DefaultProfile</span></span>
<span data-ttu-id="ed079-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed079-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed079-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed079-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ed079-118">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed079-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed079-119">CommonParameters</span></span>
<span data-ttu-id="ed079-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed079-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed079-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed079-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed079-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed079-122">INPUTS</span></span>

### <span data-ttu-id="ed079-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="ed079-124">Parametr "LocalNetworkGateway" akceptuje wartość typu "PSLocalNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ed079-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="ed079-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed079-125">OUTPUTS</span></span>

### <span data-ttu-id="ed079-126">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ed079-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed079-127">NOTES</span></span>

## <span data-ttu-id="ed079-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed079-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed079-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ed079-130">Nowe — AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="ed079-131">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed079-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


