---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872144"
---
# <span data-ttu-id="02424-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="02424-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02424-102">SYNOPSIS</span></span>
<span data-ttu-id="02424-103">Umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="02424-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02424-104">SYNTAX</span></span>

### <span data-ttu-id="02424-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="02424-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02424-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="02424-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02424-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="02424-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02424-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="02424-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02424-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="02424-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02424-110">Opis</span><span class="sxs-lookup"><span data-stu-id="02424-110">DESCRIPTION</span></span>
<span data-ttu-id="02424-111">Polecenie cmdlet **Set-AzVirtualNetworkGateway** umożliwia zaktualizowanie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="02424-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02424-112">EXAMPLES</span></span>

### <span data-ttu-id="02424-113">Przykład 1: aktualizowanie ASN bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="02424-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="02424-114">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugim poleceniem aktualizuje bramę sieci wirtualnej przechowywaną w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="02424-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="02424-115">Polecenie ustawia również ASN na 1337.</span><span class="sxs-lookup"><span data-stu-id="02424-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="02424-116">Przykład 2: Dodawanie zasad IPsec do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="02424-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="02424-117">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugie polecenie tworzy obiekt zasad IPSec sieci VPN zgodnie z określonymi parametrami protokołu IPSec.</span><span class="sxs-lookup"><span data-stu-id="02424-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="02424-118">Trzecie polecenie aktualizuje bramę sieci wirtualnej przechowywaną w zmiennej $Gateway.</span><span class="sxs-lookup"><span data-stu-id="02424-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="02424-119">Polecenie ustawia również niestandardowe zasady IPSec sieci VPN określone w obiekcie $vpnclientipsecpolicy w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="02424-120">Przykład 3: Dodawanie/aktualizowanie znaczników do istniejącej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="02424-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="02424-121">Pierwsze polecenie pobiera wirtualną bramę sieciową o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugie polecenie aktualizuje Gateway01 bramy sieci wirtualnej za pomocą tagów @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="02424-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="02424-122">Przykład 4: Dodawanie/aktualizowanie konfiguracji uwierzytelniania w usłudze AAD dla VpnClient istniejącej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="02424-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="02424-123">Pierwsze polecenie pobiera bramę sieci wirtualnej o nazwie Gateway01 należącej do grupy zasobów ResourceGroup001 i zapisuje ją w zmiennej o nazwie $Gateway drugie polecenie aktualizuje Gateway01 bramy sieci wirtualnej za pomocą parametrów konfiguracji uwierzytelniania w usłudze AAD: aadTenantUri, aadAudienceId, aadIssuerUri dla VpnClient.</span><span class="sxs-lookup"><span data-stu-id="02424-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="02424-124">Trzecie polecenie usuwa konfigurację uwierzytelniania w usłudze AAD z VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="02424-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02424-125">PARAMETERS</span></span>

### <span data-ttu-id="02424-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="02424-126">-AadAudienceId</span></span>
<span data-ttu-id="02424-127">Opcja uwierzytelniania w usłudze AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="02424-127">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02424-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="02424-128">-AadIssuerUri</span></span>
<span data-ttu-id="02424-129">Opcja uwierzytelniania w usłudze AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="02424-129">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02424-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="02424-130">-AadTenantUri</span></span>
<span data-ttu-id="02424-131">Opcja uwierzytelniania w usłudze AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="02424-131">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02424-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02424-132">-AsJob</span></span>
<span data-ttu-id="02424-133">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="02424-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02424-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="02424-134">-Asn</span></span>
<span data-ttu-id="02424-135">Określa numer autonomiczny (ASN) bramy sieci wirtualnej służący do konfigurowania sesji BGP (Border Gateway Protocol) w tunelach IPsec.</span><span class="sxs-lookup"><span data-stu-id="02424-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="02424-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="02424-136">-CustomRoute</span></span>
<span data-ttu-id="02424-137">Trasy niestandardowe AddressPool określone przez klienta</span><span class="sxs-lookup"><span data-stu-id="02424-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="02424-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02424-138">-DefaultProfile</span></span>
<span data-ttu-id="02424-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02424-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02424-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="02424-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="02424-141">Wyłącza aktywną, aktywną funkcję.</span><span class="sxs-lookup"><span data-stu-id="02424-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="02424-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="02424-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="02424-143">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="02424-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="02424-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="02424-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="02424-145">Określa domyślną witrynę, która ma być używana do wymuszania tunelowania.</span><span class="sxs-lookup"><span data-stu-id="02424-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="02424-146">Jeśli określono witrynę domyślną, cały ruch internetowy z wirtualnej sieci prywatnej (VPN) bramy jest przekierowywany do tej witryny.</span><span class="sxs-lookup"><span data-stu-id="02424-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="02424-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="02424-147">-GatewaySku</span></span>
<span data-ttu-id="02424-148">Określa jednostkę składowania zapasu (SKU) bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="02424-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="02424-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02424-150">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="02424-150">Basic</span></span>
- <span data-ttu-id="02424-151">Standard</span><span class="sxs-lookup"><span data-stu-id="02424-151">Standard</span></span>
- <span data-ttu-id="02424-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="02424-152">HighPerformance</span></span>
- <span data-ttu-id="02424-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="02424-153">VpnGw1</span></span>
- <span data-ttu-id="02424-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="02424-154">VpnGw2</span></span>
- <span data-ttu-id="02424-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="02424-155">VpnGw3</span></span>
- <span data-ttu-id="02424-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="02424-156">VpnGw1AZ</span></span>
- <span data-ttu-id="02424-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="02424-157">VpnGw2AZ</span></span>
- <span data-ttu-id="02424-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="02424-158">VpnGw3AZ</span></span>
- <span data-ttu-id="02424-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="02424-159">ErGw1AZ</span></span>
- <span data-ttu-id="02424-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="02424-160">ErGw2AZ</span></span>
- <span data-ttu-id="02424-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="02424-161">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02424-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="02424-162">-PeerWeight</span></span>
<span data-ttu-id="02424-163">Określa wagę dodaną do tras uzyskiwanych za pośrednictwem protokołu BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="02424-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="02424-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="02424-164">-RadiusServerAddress</span></span>
<span data-ttu-id="02424-165">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="02424-165">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02424-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="02424-166">-RadiusServerSecret</span></span>
<span data-ttu-id="02424-167">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="02424-167">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02424-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="02424-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="02424-169">Flaga usunięcia uwierzytelniania w usłudze AAD dla klienta P2S z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="02424-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="02424-170">-Tag</span></span>
<span data-ttu-id="02424-171">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="02424-171">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02424-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="02424-173">Określa obiekt bramy sieci wirtualnej, którego nie można modyfikować.</span><span class="sxs-lookup"><span data-stu-id="02424-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="02424-174">Możesz użyć polecenia cmdlet Get-AzVirtualNetworkGateway, aby uzyskać obiekt bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02424-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="02424-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="02424-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="02424-176">Określa przestrzeń adresową używaną przez polecenie cmdlet do przydzielania adresów IP klientów sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="02424-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="02424-177">Nie powinno to pokrywać się z zakresem sieci wirtualnej ani z zakresu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="02424-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="02424-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="02424-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="02424-179">Lista zasad IPSec dla protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="02424-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="02424-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="02424-180">-VpnClientProtocol</span></span>
<span data-ttu-id="02424-181">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="02424-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="02424-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="02424-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="02424-183">Określa listę odwołanych certyfikatów klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="02424-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="02424-184">Klient VPN przedstawiający certyfikat zgodny z jednym z tych osób zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="02424-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="02424-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="02424-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="02424-186">Określa listę certyfikatów głównych klienta sieci VPN, których należy używać do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="02424-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="02424-187">Nawiązywanie połączeń z klientami sieci VPN jest konieczne prezentowanie certyfikatów generowanych przy użyciu jednego z tych certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="02424-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="02424-188">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02424-188">-Confirm</span></span>
<span data-ttu-id="02424-189">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02424-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02424-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02424-190">-WhatIf</span></span>
<span data-ttu-id="02424-191">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02424-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02424-192">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02424-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02424-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02424-193">CommonParameters</span></span>
<span data-ttu-id="02424-194">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02424-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02424-195">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02424-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02424-196">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02424-196">INPUTS</span></span>

### <span data-ttu-id="02424-197">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="02424-198">System. String</span><span class="sxs-lookup"><span data-stu-id="02424-198">System.String</span></span>

### <span data-ttu-id="02424-199">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="02424-200">System. String []</span><span class="sxs-lookup"><span data-stu-id="02424-200">System.String[]</span></span>

### <span data-ttu-id="02424-201">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="02424-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="02424-202">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="02424-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="02424-203">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="02424-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="02424-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="02424-204">System.UInt32</span></span>

### <span data-ttu-id="02424-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="02424-205">System.Int32</span></span>

### <span data-ttu-id="02424-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="02424-206">System.Security.SecureString</span></span>

## <span data-ttu-id="02424-207">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02424-207">OUTPUTS</span></span>

### <span data-ttu-id="02424-208">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="02424-209">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02424-209">NOTES</span></span>
* <span data-ttu-id="02424-210">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="02424-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="02424-211">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02424-211">RELATED LINKS</span></span>

[<span data-ttu-id="02424-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="02424-213">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="02424-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="02424-215">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="02424-216">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02424-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
