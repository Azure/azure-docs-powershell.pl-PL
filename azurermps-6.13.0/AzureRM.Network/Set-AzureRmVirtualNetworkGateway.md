---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548620"
---
# <span data-ttu-id="e3bfd-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="e3bfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bfd-103">Umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3bfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3bfd-104">SYNTAX</span></span>

### <span data-ttu-id="e3bfd-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e3bfd-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3bfd-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3bfd-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3bfd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3bfd-107">DESCRIPTION</span></span>
<span data-ttu-id="e3bfd-108">Polecenie cmdlet **Set-AzureRmVirtualNetworkGateway** umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="e3bfd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3bfd-109">EXAMPLES</span></span>

### <span data-ttu-id="e3bfd-110">Przykład 1: Ustawianie stanu celu dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3bfd-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="e3bfd-111">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugie polecenie ustawia stan celu bramy sieci wirtualnej przechowywanej w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="e3bfd-112">Polecenie ustawia również ASN na 1337.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="e3bfd-113">Przykład 2: Ustawianie stanu celu dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3bfd-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="e3bfd-114">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugie polecenie tworzy obiekt zasad IPSec sieci VPN zgodnie z określonymi parametrami protokołu IPSec.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="e3bfd-115">Trzecie polecenie ustawia stan celu bramy sieci wirtualnej przechowywanej w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="e3bfd-116">Polecenie ustawia również niestandardowe zasady IPSec sieci VPN określone w obiekcie $vpnclientipsecpolicy w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="e3bfd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3bfd-117">PARAMETERS</span></span>

### <span data-ttu-id="e3bfd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3bfd-118">-AsJob</span></span>
<span data-ttu-id="e3bfd-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e3bfd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3bfd-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="e3bfd-120">-Asn</span></span>
<span data-ttu-id="e3bfd-121">Określa numer autonomiczny (ASN) bramy sieci wirtualnej służący do konfigurowania sesji BGP (Border Gateway Protocol) w tunelach IPsec.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="e3bfd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bfd-122">-DefaultProfile</span></span>
<span data-ttu-id="e3bfd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3bfd-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="e3bfd-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="e3bfd-125">Wyłącza aktywną, aktywną funkcję.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="e3bfd-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="e3bfd-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="e3bfd-127">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="e3bfd-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e3bfd-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="e3bfd-129">Określa domyślną witrynę, która ma być używana do wymuszania tunelowania.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="e3bfd-130">Jeśli określono witrynę domyślną, cały ruch internetowy z wirtualnej sieci prywatnej (VPN) bramy jest przekierowywany do tej witryny.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="e3bfd-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="e3bfd-131">-GatewaySku</span></span>
<span data-ttu-id="e3bfd-132">Określa jednostkę składowania zapasu (SKU) bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="e3bfd-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e3bfd-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3bfd-134">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="e3bfd-134">Basic</span></span>
- <span data-ttu-id="e3bfd-135">Standard</span><span class="sxs-lookup"><span data-stu-id="e3bfd-135">Standard</span></span>
- <span data-ttu-id="e3bfd-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="e3bfd-136">HighPerformance</span></span>
- <span data-ttu-id="e3bfd-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="e3bfd-137">VpnGw1</span></span>
- <span data-ttu-id="e3bfd-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="e3bfd-138">VpnGw2</span></span>
- <span data-ttu-id="e3bfd-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="e3bfd-139">VpnGw3</span></span>
- <span data-ttu-id="e3bfd-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="e3bfd-140">VpnGw1AZ</span></span>
- <span data-ttu-id="e3bfd-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="e3bfd-141">VpnGw2AZ</span></span>
- <span data-ttu-id="e3bfd-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="e3bfd-142">VpnGw3AZ</span></span>
- <span data-ttu-id="e3bfd-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="e3bfd-143">ErGw1AZ</span></span>
- <span data-ttu-id="e3bfd-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="e3bfd-144">ErGw2AZ</span></span>
- <span data-ttu-id="e3bfd-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="e3bfd-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="e3bfd-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e3bfd-146">-PeerWeight</span></span>
<span data-ttu-id="e3bfd-147">Określa wagę dodaną do tras uzyskiwanych za pośrednictwem protokołu BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3bfd-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="e3bfd-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="e3bfd-148">-RadiusServerAddress</span></span>
<span data-ttu-id="e3bfd-149">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="e3bfd-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="e3bfd-150">-RadiusServerSecret</span></span>
<span data-ttu-id="e3bfd-151">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="e3bfd-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="e3bfd-153">Określa obiekt bramy sieci wirtualnej, którego nie można modyfikować.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="e3bfd-154">Możesz użyć polecenia cmdlet Get-AzureRmVirtualNetworkGateway, aby uzyskać obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="e3bfd-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="e3bfd-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="e3bfd-156">Określa przestrzeń adresową używaną przez polecenie cmdlet do przydzielania adresów IP klientów sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="e3bfd-157">Nie powinno to pokrywać się z zakresem sieci wirtualnej ani z zakresu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-157">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="e3bfd-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="e3bfd-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="e3bfd-159">Lista zasad IPSec dla protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bfd-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="e3bfd-160">-VpnClientProtocol</span></span>
<span data-ttu-id="e3bfd-161">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="e3bfd-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bfd-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="e3bfd-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="e3bfd-163">Określa listę odwołanych certyfikatów klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="e3bfd-164">Klient VPN przedstawiający certyfikat zgodny z jednym z tych osób zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="e3bfd-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="e3bfd-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="e3bfd-166">Określa listę certyfikatów głównych klienta sieci VPN, których należy używać do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="e3bfd-167">Nawiązywanie połączeń z klientami sieci VPN jest konieczne prezentowanie certyfikatów generowanych przy użyciu jednego z tych certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="e3bfd-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3bfd-168">-Confirm</span></span>
<span data-ttu-id="e3bfd-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bfd-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bfd-170">-WhatIf</span></span>
<span data-ttu-id="e3bfd-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3bfd-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bfd-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bfd-173">CommonParameters</span></span>
<span data-ttu-id="e3bfd-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3bfd-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bfd-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bfd-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bfd-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3bfd-176">INPUTS</span></span>

### <span data-ttu-id="e3bfd-177">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="e3bfd-178">Parametry: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3bfd-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="e3bfd-179">System. String</span><span class="sxs-lookup"><span data-stu-id="e3bfd-179">System.String</span></span>

### <span data-ttu-id="e3bfd-180">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="e3bfd-181">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e3bfd-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e3bfd-182">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSVpnClientRootCertificate; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3bfd-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e3bfd-183">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSVpnClientRevokedCertificate; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3bfd-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e3bfd-184">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSIpsecPolicy; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3bfd-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e3bfd-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="e3bfd-185">System.UInt32</span></span>

### <span data-ttu-id="e3bfd-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e3bfd-186">System.Int32</span></span>

### <span data-ttu-id="e3bfd-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e3bfd-187">System.Security.SecureString</span></span>

## <span data-ttu-id="e3bfd-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3bfd-188">OUTPUTS</span></span>

### <span data-ttu-id="e3bfd-189">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e3bfd-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3bfd-190">NOTES</span></span>
* <span data-ttu-id="e3bfd-191">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="e3bfd-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e3bfd-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3bfd-192">RELATED LINKS</span></span>

[<span data-ttu-id="e3bfd-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e3bfd-194">Nowe — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e3bfd-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e3bfd-196">Resetowanie — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="e3bfd-197">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3bfd-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


