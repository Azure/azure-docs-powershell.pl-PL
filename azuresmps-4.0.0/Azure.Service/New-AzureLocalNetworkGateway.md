---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054973"
---
# <span data-ttu-id="4b203-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4b203-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="4b203-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b203-102">SYNOPSIS</span></span>
<span data-ttu-id="4b203-103">tworzy bramę sieci lokalnej Azure.</span><span class="sxs-lookup"><span data-stu-id="4b203-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="4b203-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b203-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b203-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b203-105">DESCRIPTION</span></span>
<span data-ttu-id="4b203-106">Polecenie cmdlet **New-AzureLocalNetworkGateway** umożliwia utworzenie bramy lokalnego sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="4b203-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="4b203-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b203-107">EXAMPLES</span></span>

## <span data-ttu-id="4b203-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b203-108">PARAMETERS</span></span>

### <span data-ttu-id="4b203-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="4b203-109">-AddressSpace</span></span>
<span data-ttu-id="4b203-110">Określa przestrzeń adresową.</span><span class="sxs-lookup"><span data-stu-id="4b203-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="4b203-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="4b203-111">-Asn</span></span>
<span data-ttu-id="4b203-112">Umożliwia określenie numeru system autonomiczny (ASN).</span><span class="sxs-lookup"><span data-stu-id="4b203-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="4b203-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="4b203-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="4b203-114">Określa adres równorzędny protokołu BGP (Border Gateway Protocol).</span><span class="sxs-lookup"><span data-stu-id="4b203-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="4b203-115">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="4b203-115">-GatewayName</span></span>
<span data-ttu-id="4b203-116">Określa nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="4b203-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="4b203-117">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="4b203-117">-IpAddress</span></span>
<span data-ttu-id="4b203-118">Określa adres IP.</span><span class="sxs-lookup"><span data-stu-id="4b203-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="4b203-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="4b203-119">-PeerWeight</span></span>
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

### <span data-ttu-id="4b203-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="4b203-120">-Profile</span></span>
<span data-ttu-id="4b203-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b203-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4b203-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4b203-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b203-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b203-123">CommonParameters</span></span>
<span data-ttu-id="4b203-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b203-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b203-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b203-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b203-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b203-126">INPUTS</span></span>

## <span data-ttu-id="4b203-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b203-127">OUTPUTS</span></span>

## <span data-ttu-id="4b203-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b203-128">NOTES</span></span>

## <span data-ttu-id="4b203-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b203-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b203-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4b203-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="4b203-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4b203-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="4b203-132">Resetowanie — AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4b203-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


