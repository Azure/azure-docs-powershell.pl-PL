---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546191"
---
# <span data-ttu-id="27474-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="27474-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27474-102">SYNOPSIS</span></span>
<span data-ttu-id="27474-103">Umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27474-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27474-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27474-104">SYNTAX</span></span>

### <span data-ttu-id="27474-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="27474-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27474-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="27474-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27474-107">Opis</span><span class="sxs-lookup"><span data-stu-id="27474-107">DESCRIPTION</span></span>
<span data-ttu-id="27474-108">Polecenie cmdlet **Set-AzureRmVirtualNetworkGateway** umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27474-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="27474-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27474-109">EXAMPLES</span></span>

### <span data-ttu-id="27474-110">Przykład 1: Ustawianie stanu celu dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="27474-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="27474-111">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway</span><span class="sxs-lookup"><span data-stu-id="27474-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="27474-112">Drugie polecenie ustawia stan celu bramy sieci wirtualnej przechowywanej w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="27474-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="27474-113">Polecenie ustawia również ASN na 1337.</span><span class="sxs-lookup"><span data-stu-id="27474-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="27474-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27474-114">PARAMETERS</span></span>

### <span data-ttu-id="27474-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="27474-115">-Asn</span></span>
<span data-ttu-id="27474-116">Określa numer autonomiczny (ASN) bramy sieci wirtualnej służący do konfigurowania sesji BGP (Border Gateway Protocol) w tunelach IPsec.</span><span class="sxs-lookup"><span data-stu-id="27474-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27474-117">-DefaultProfile</span></span>
<span data-ttu-id="27474-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27474-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27474-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="27474-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="27474-120">Wyłącza aktywną, aktywną funkcję.</span><span class="sxs-lookup"><span data-stu-id="27474-120">Disables the active-active feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27474-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="27474-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="27474-122">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="27474-122">Enables the active-active feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27474-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="27474-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="27474-124">Określa domyślną witrynę, która ma być używana do wymuszania tunelowania.</span><span class="sxs-lookup"><span data-stu-id="27474-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="27474-125">Jeśli określono witrynę domyślną, cały ruch internetowy z wirtualnej sieci prywatnej (VPN) bramy jest przekierowywany do tej witryny.</span><span class="sxs-lookup"><span data-stu-id="27474-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="27474-126">-GatewaySku</span></span>
<span data-ttu-id="27474-127">Określa jednostkę składowania zapasu (SKU) bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27474-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="27474-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="27474-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27474-129">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="27474-129">Basic</span></span>
- <span data-ttu-id="27474-130">Standard</span><span class="sxs-lookup"><span data-stu-id="27474-130">Standard</span></span>
- <span data-ttu-id="27474-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="27474-131">HighPerformance</span></span>
- <span data-ttu-id="27474-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="27474-132">VpnGw1</span></span>
- <span data-ttu-id="27474-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="27474-133">VpnGw2</span></span>
- <span data-ttu-id="27474-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="27474-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="27474-135">-PeerWeight</span></span>
<span data-ttu-id="27474-136">Określa wagę dodaną do tras uzyskiwanych za pośrednictwem protokołu BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="27474-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="27474-137">-RadiusServerAddress</span></span>
<span data-ttu-id="27474-138">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="27474-138">P2S External Radius server address.</span></span>
```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="27474-139">-RadiusServerSecret</span></span>
<span data-ttu-id="27474-140">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="27474-140">P2S External Radius server secret.</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="27474-142">Określa obiekt bramy sieci wirtualnej, którego nie można modyfikować.</span><span class="sxs-lookup"><span data-stu-id="27474-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="27474-143">Możesz użyć polecenia cmdlet Get-AzureRmVirtualNetworkGateway, aby uzyskać obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27474-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="27474-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="27474-145">Określa przestrzeń adresową używaną przez polecenie cmdlet do przydzielania adresów IP klientów sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="27474-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="27474-146">Nie powinno to pokrywać się z zakresem sieci wirtualnej ani z zakresu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="27474-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="27474-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="27474-147">-VpnClientProtocol</span></span>
<span data-ttu-id="27474-148">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="27474-148">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="27474-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="27474-150">Określa listę odwołanych certyfikatów klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="27474-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="27474-151">Klient VPN przedstawiający certyfikat zgodny z jednym z tych osób zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="27474-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="27474-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="27474-153">Określa listę certyfikatów głównych klienta sieci VPN, których należy używać do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="27474-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="27474-154">Nawiązywanie połączeń z klientami sieci VPN jest konieczne prezentowanie certyfikatów generowanych przy użyciu jednego z tych certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="27474-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27474-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27474-155">-Confirm</span></span>
<span data-ttu-id="27474-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27474-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27474-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27474-157">-WhatIf</span></span>
<span data-ttu-id="27474-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27474-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27474-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27474-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27474-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27474-160">CommonParameters</span></span>
<span data-ttu-id="27474-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27474-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27474-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27474-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27474-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27474-163">INPUTS</span></span>

### <span data-ttu-id="27474-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="27474-165">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="27474-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="27474-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27474-166">OUTPUTS</span></span>

### <span data-ttu-id="27474-167">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="27474-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27474-168">NOTES</span></span>
* <span data-ttu-id="27474-169">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="27474-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="27474-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27474-170">RELATED LINKS</span></span>

[<span data-ttu-id="27474-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="27474-172">Nowe — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="27474-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="27474-174">Resetowanie — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="27474-175">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27474-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


