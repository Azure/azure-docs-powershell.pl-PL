---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708928"
---
# <span data-ttu-id="55261-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="55261-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55261-102">SYNOPSIS</span></span>
<span data-ttu-id="55261-103">Umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55261-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="55261-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55261-104">SYNTAX</span></span>

### <span data-ttu-id="55261-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="55261-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55261-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="55261-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55261-107">Opis</span><span class="sxs-lookup"><span data-stu-id="55261-107">DESCRIPTION</span></span>
<span data-ttu-id="55261-108">Polecenie cmdlet **Set-AzVirtualNetworkGateway** umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55261-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="55261-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55261-109">EXAMPLES</span></span>

### <span data-ttu-id="55261-110">Przykład 1: aktualizowanie ASN bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="55261-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="55261-111">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugim poleceniem aktualizuje bramę sieci wirtualnej przechowywaną w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="55261-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="55261-112">Polecenie ustawia również ASN na 1337.</span><span class="sxs-lookup"><span data-stu-id="55261-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="55261-113">Przykład 2: Dodawanie zasad IPsec do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="55261-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="55261-114">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugie polecenie tworzy obiekt zasad IPSec sieci VPN zgodnie z określonymi parametrami protokołu IPSec.</span><span class="sxs-lookup"><span data-stu-id="55261-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="55261-115">Trzecie polecenie aktualizuje bramę sieci wirtualnej przechowywaną w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="55261-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="55261-116">Polecenie ustawia również niestandardowe zasady IPSec sieci VPN określone w obiekcie $vpnclientipsecpolicy w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55261-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="55261-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55261-117">PARAMETERS</span></span>

### <span data-ttu-id="55261-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55261-118">-AsJob</span></span>
<span data-ttu-id="55261-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="55261-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55261-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="55261-120">-Asn</span></span>
<span data-ttu-id="55261-121">Określa numer autonomiczny (ASN) bramy sieci wirtualnej służący do konfigurowania sesji BGP (Border Gateway Protocol) w tunelach IPsec.</span><span class="sxs-lookup"><span data-stu-id="55261-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="55261-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55261-122">-DefaultProfile</span></span>
<span data-ttu-id="55261-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55261-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55261-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="55261-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="55261-125">Wyłącza aktywną, aktywną funkcję.</span><span class="sxs-lookup"><span data-stu-id="55261-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="55261-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="55261-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="55261-127">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="55261-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="55261-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="55261-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="55261-129">Określa domyślną witrynę, która ma być używana do wymuszania tunelowania.</span><span class="sxs-lookup"><span data-stu-id="55261-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="55261-130">Jeśli określono witrynę domyślną, cały ruch internetowy z wirtualnej sieci prywatnej (VPN) bramy jest przekierowywany do tej witryny.</span><span class="sxs-lookup"><span data-stu-id="55261-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="55261-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="55261-131">-GatewaySku</span></span>
<span data-ttu-id="55261-132">Określa jednostkę składowania zapasu (SKU) bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55261-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="55261-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="55261-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55261-134">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="55261-134">Basic</span></span>
- <span data-ttu-id="55261-135">Standard</span><span class="sxs-lookup"><span data-stu-id="55261-135">Standard</span></span>
- <span data-ttu-id="55261-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="55261-136">HighPerformance</span></span>
- <span data-ttu-id="55261-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="55261-137">VpnGw1</span></span>
- <span data-ttu-id="55261-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="55261-138">VpnGw2</span></span>
- <span data-ttu-id="55261-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="55261-139">VpnGw3</span></span>
- <span data-ttu-id="55261-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="55261-140">VpnGw1AZ</span></span>
- <span data-ttu-id="55261-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="55261-141">VpnGw2AZ</span></span>
- <span data-ttu-id="55261-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="55261-142">VpnGw3AZ</span></span>
- <span data-ttu-id="55261-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="55261-143">ErGw1AZ</span></span>
- <span data-ttu-id="55261-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="55261-144">ErGw2AZ</span></span>
- <span data-ttu-id="55261-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="55261-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55261-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="55261-146">-PeerWeight</span></span>
<span data-ttu-id="55261-147">Określa wagę dodaną do tras uzyskiwanych za pośrednictwem protokołu BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="55261-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="55261-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="55261-148">-RadiusServerAddress</span></span>
<span data-ttu-id="55261-149">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="55261-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="55261-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="55261-150">-RadiusServerSecret</span></span>
<span data-ttu-id="55261-151">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="55261-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="55261-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="55261-153">Określa obiekt bramy sieci wirtualnej, którego nie można modyfikować.</span><span class="sxs-lookup"><span data-stu-id="55261-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="55261-154">Możesz użyć polecenia cmdlet Get-AzVirtualNetworkGateway, aby uzyskać obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55261-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="55261-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="55261-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="55261-156">Określa przestrzeń adresową używaną przez polecenie cmdlet do przydzielania adresów IP klientów sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="55261-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="55261-157">Nie powinno to pokrywać się z zakresem sieci wirtualnej ani z zakresu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="55261-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55261-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="55261-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="55261-159">Lista zasad IPSec dla protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="55261-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55261-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="55261-160">-VpnClientProtocol</span></span>
<span data-ttu-id="55261-161">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="55261-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55261-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="55261-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="55261-163">Określa listę odwołanych certyfikatów klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="55261-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="55261-164">Klient VPN przedstawiający certyfikat zgodny z jednym z tych osób zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="55261-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55261-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="55261-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="55261-166">Określa listę certyfikatów głównych klienta sieci VPN, których należy używać do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="55261-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="55261-167">Nawiązywanie połączeń z klientami sieci VPN jest konieczne prezentowanie certyfikatów generowanych przy użyciu jednego z tych certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="55261-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55261-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55261-168">-Confirm</span></span>
<span data-ttu-id="55261-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55261-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55261-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55261-170">-WhatIf</span></span>
<span data-ttu-id="55261-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55261-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55261-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55261-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55261-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55261-173">CommonParameters</span></span>
<span data-ttu-id="55261-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55261-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55261-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55261-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55261-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55261-176">INPUTS</span></span>

### <span data-ttu-id="55261-177">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="55261-178">System. String</span><span class="sxs-lookup"><span data-stu-id="55261-178">System.String</span></span>

### <span data-ttu-id="55261-179">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="55261-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="55261-180">System.String[]</span></span>

### <span data-ttu-id="55261-181">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="55261-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="55261-182">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="55261-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="55261-183">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="55261-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="55261-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="55261-184">System.UInt32</span></span>

### <span data-ttu-id="55261-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55261-185">System.Int32</span></span>

### <span data-ttu-id="55261-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="55261-186">System.Security.SecureString</span></span>

## <span data-ttu-id="55261-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55261-187">OUTPUTS</span></span>

### <span data-ttu-id="55261-188">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="55261-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55261-189">NOTES</span></span>
* <span data-ttu-id="55261-190">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="55261-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="55261-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55261-191">RELATED LINKS</span></span>

[<span data-ttu-id="55261-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="55261-193">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="55261-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="55261-195">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="55261-196">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55261-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
