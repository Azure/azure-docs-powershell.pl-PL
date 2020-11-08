---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054438"
---
# <span data-ttu-id="5043a-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5043a-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="5043a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5043a-102">SYNOPSIS</span></span>
<span data-ttu-id="5043a-103">Resetuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="5043a-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="5043a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5043a-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5043a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5043a-105">DESCRIPTION</span></span>
<span data-ttu-id="5043a-106">Polecenie cmdlet **Reset-AzureLocalNetworkGateway** resetuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="5043a-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="5043a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5043a-107">EXAMPLES</span></span>

## <span data-ttu-id="5043a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5043a-108">PARAMETERS</span></span>

### <span data-ttu-id="5043a-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="5043a-109">-AddressSpace</span></span>
<span data-ttu-id="5043a-110">Określa przestrzeń adresową.</span><span class="sxs-lookup"><span data-stu-id="5043a-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5043a-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="5043a-111">-Asn</span></span>
<span data-ttu-id="5043a-112">Umożliwia określenie numeru system autonomiczny (ASN).</span><span class="sxs-lookup"><span data-stu-id="5043a-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5043a-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5043a-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="5043a-114">Określa adres równorzędny protokołu BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="5043a-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5043a-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5043a-115">-GatewayId</span></span>
<span data-ttu-id="5043a-116">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="5043a-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="5043a-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="5043a-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5043a-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="5043a-118">-Profile</span></span>
<span data-ttu-id="5043a-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5043a-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5043a-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5043a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5043a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5043a-121">CommonParameters</span></span>
<span data-ttu-id="5043a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5043a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5043a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5043a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5043a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5043a-124">INPUTS</span></span>

## <span data-ttu-id="5043a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5043a-125">OUTPUTS</span></span>

## <span data-ttu-id="5043a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5043a-126">NOTES</span></span>

## <span data-ttu-id="5043a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5043a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5043a-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5043a-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="5043a-129">Nowe — AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5043a-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="5043a-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5043a-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


