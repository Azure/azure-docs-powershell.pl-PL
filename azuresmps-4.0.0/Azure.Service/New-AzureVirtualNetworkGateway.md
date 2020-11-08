---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055152"
---
# <span data-ttu-id="ad3ca-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad3ca-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="ad3ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3ca-103">Tworzy bramę sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="ad3ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad3ca-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ad3ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad3ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3ca-106">Polecenie cmdlet **New-AzureVirtualNetworkGateway** tworzy bramę sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="ad3ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad3ca-107">EXAMPLES</span></span>

## <span data-ttu-id="ad3ca-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad3ca-108">PARAMETERS</span></span>

### <span data-ttu-id="ad3ca-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="ad3ca-109">-Asn</span></span>
<span data-ttu-id="ad3ca-110">Umożliwia określenie numeru system autonomiczny (ASN).</span><span class="sxs-lookup"><span data-stu-id="ad3ca-110">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="ad3ca-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ad3ca-111">-Force</span></span>
<span data-ttu-id="ad3ca-112">Nie potwierdzaj tworzenia bramy sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ad3ca-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

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

### <span data-ttu-id="ad3ca-113">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="ad3ca-113">-GatewayName</span></span>
<span data-ttu-id="ad3ca-114">Określa nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="ad3ca-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="ad3ca-115">-GatewaySKU</span></span>
<span data-ttu-id="ad3ca-116">Określa jednostkę SKU bramy sieci wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="ad3ca-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ad3ca-117">Valid values are:</span></span>

- <span data-ttu-id="ad3ca-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="ad3ca-118">Default</span></span>
- <span data-ttu-id="ad3ca-119">Standard</span><span class="sxs-lookup"><span data-stu-id="ad3ca-119">Standard</span></span>
- <span data-ttu-id="ad3ca-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="ad3ca-120">HighPerformance</span></span>

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

### <span data-ttu-id="ad3ca-121">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="ad3ca-121">-GatewayType</span></span>
<span data-ttu-id="ad3ca-122">Określa typ bramy.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="ad3ca-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad3ca-123">-Location</span></span>
<span data-ttu-id="ad3ca-124">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-124">Specifies the location.</span></span>

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

### <span data-ttu-id="ad3ca-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ad3ca-125">-PeerWeight</span></span>
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

### <span data-ttu-id="ad3ca-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="ad3ca-126">-Profile</span></span>
<span data-ttu-id="ad3ca-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad3ca-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad3ca-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="ad3ca-129">-VnetId</span></span>
<span data-ttu-id="ad3ca-130">Określa identyfikator sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="ad3ca-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ad3ca-131">-VNetName</span></span>
<span data-ttu-id="ad3ca-132">Określa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="ad3ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3ca-133">CommonParameters</span></span>
<span data-ttu-id="ad3ca-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3ca-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3ca-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3ca-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad3ca-136">INPUTS</span></span>

## <span data-ttu-id="ad3ca-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad3ca-137">OUTPUTS</span></span>

## <span data-ttu-id="ad3ca-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad3ca-138">NOTES</span></span>

## <span data-ttu-id="ad3ca-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad3ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad3ca-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad3ca-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="ad3ca-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad3ca-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="ad3ca-142">Zmienianie rozmiaru — AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad3ca-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
