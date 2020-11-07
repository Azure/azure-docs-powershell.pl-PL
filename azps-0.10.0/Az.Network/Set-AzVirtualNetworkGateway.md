---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 87840267cf85997da83af590664c473a61f74033
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892713"
---
# <span data-ttu-id="1b6fb-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="1b6fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6fb-103">Umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="1b6fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b6fb-104">SYNTAX</span></span>

### <span data-ttu-id="1b6fb-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1b6fb-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b6fb-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b6fb-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b6fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1b6fb-107">DESCRIPTION</span></span>
<span data-ttu-id="1b6fb-108">Polecenie cmdlet **Set-AzVirtualNetworkGateway** umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="1b6fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b6fb-109">EXAMPLES</span></span>

### <span data-ttu-id="1b6fb-110">Przykład 1: Ustawianie stanu celu dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1b6fb-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="1b6fb-111">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="1b6fb-112">Drugie polecenie ustawia stan celu bramy sieci wirtualnej przechowywanej w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="1b6fb-113">Polecenie ustawia również ASN na 1337.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="1b6fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b6fb-114">PARAMETERS</span></span>

### <span data-ttu-id="1b6fb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b6fb-115">-AsJob</span></span>
<span data-ttu-id="1b6fb-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1b6fb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b6fb-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="1b6fb-117">-Asn</span></span>
<span data-ttu-id="1b6fb-118">Określa numer autonomiczny (ASN) bramy sieci wirtualnej służący do konfigurowania sesji BGP (Border Gateway Protocol) w tunelach IPsec.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="1b6fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6fb-119">-DefaultProfile</span></span>
<span data-ttu-id="1b6fb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="1b6fb-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1b6fb-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="1b6fb-122">Wyłącza aktywną, aktywną funkcję.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-122">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="1b6fb-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1b6fb-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="1b6fb-124">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-124">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="1b6fb-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1b6fb-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="1b6fb-126">Określa domyślną witrynę, która ma być używana do wymuszania tunelowania.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="1b6fb-127">Jeśli określono witrynę domyślną, cały ruch internetowy z wirtualnej sieci prywatnej (VPN) bramy jest przekierowywany do tej witryny.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="1b6fb-128">-GatewaySku</span></span>
<span data-ttu-id="1b6fb-129">Określa jednostkę składowania zapasu (SKU) bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="1b6fb-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1b6fb-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b6fb-131">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="1b6fb-131">Basic</span></span>
- <span data-ttu-id="1b6fb-132">Standard</span><span class="sxs-lookup"><span data-stu-id="1b6fb-132">Standard</span></span>
- <span data-ttu-id="1b6fb-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="1b6fb-133">HighPerformance</span></span>
- <span data-ttu-id="1b6fb-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="1b6fb-134">VpnGw1</span></span>
- <span data-ttu-id="1b6fb-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="1b6fb-135">VpnGw2</span></span>
- <span data-ttu-id="1b6fb-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="1b6fb-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1b6fb-137">-PeerWeight</span></span>
<span data-ttu-id="1b6fb-138">Określa wagę dodaną do tras uzyskiwanych za pośrednictwem protokołu BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1b6fb-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="1b6fb-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1b6fb-139">-RadiusServerAddress</span></span>
<span data-ttu-id="1b6fb-140">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1b6fb-141">-RadiusServerSecret</span></span>
<span data-ttu-id="1b6fb-142">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1b6fb-144">Określa obiekt bramy sieci wirtualnej, którego nie można modyfikować.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="1b6fb-145">Możesz użyć polecenia cmdlet Get-AzVirtualNetworkGateway, aby uzyskać obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-145">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b6fb-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="1b6fb-147">Określa przestrzeń adresową używaną przez polecenie cmdlet do przydzielania adresów IP klientów sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="1b6fb-148">Nie powinno to pokrywać się z zakresem sieci wirtualnej ani z zakresu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="1b6fb-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1b6fb-149">-VpnClientProtocol</span></span>
<span data-ttu-id="1b6fb-150">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="1b6fb-150">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="1b6fb-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="1b6fb-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="1b6fb-152">Określa listę odwołanych certyfikatów klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="1b6fb-153">Klient VPN przedstawiający certyfikat zgodny z jednym z tych osób zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="1b6fb-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="1b6fb-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="1b6fb-155">Określa listę certyfikatów głównych klienta sieci VPN, których należy używać do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="1b6fb-156">Nawiązywanie połączeń z klientami sieci VPN jest konieczne prezentowanie certyfikatów generowanych przy użyciu jednego z tych certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="1b6fb-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b6fb-157">-Confirm</span></span>
<span data-ttu-id="1b6fb-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b6fb-159">-WhatIf</span></span>
<span data-ttu-id="1b6fb-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b6fb-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6fb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6fb-162">CommonParameters</span></span>
<span data-ttu-id="1b6fb-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6fb-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6fb-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6fb-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b6fb-165">INPUTS</span></span>

### <span data-ttu-id="1b6fb-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1b6fb-167">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1b6fb-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="1b6fb-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b6fb-168">OUTPUTS</span></span>

### <span data-ttu-id="1b6fb-169">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1b6fb-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b6fb-170">NOTES</span></span>
* <span data-ttu-id="1b6fb-171">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="1b6fb-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1b6fb-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b6fb-172">RELATED LINKS</span></span>

[<span data-ttu-id="1b6fb-173">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-173">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1b6fb-174">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-174">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1b6fb-175">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-175">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1b6fb-176">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-176">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1b6fb-177">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fb-177">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)


