---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191618"
---
# <span data-ttu-id="65206-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65206-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="65206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65206-102">SYNOPSIS</span></span>
<span data-ttu-id="65206-103">Aktualizuje wirtualną bramę sieciową.</span><span class="sxs-lookup"><span data-stu-id="65206-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="65206-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65206-104">SYNTAX</span></span>

### <span data-ttu-id="65206-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="65206-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65206-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="65206-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65206-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="65206-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65206-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="65206-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65206-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="65206-109">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65206-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="65206-110">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65206-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="65206-111">DESCRIPTION</span></span>
<span data-ttu-id="65206-112">Polecenie **cmdlet Set-AzVirtualNetworkGateway** aktualizuje bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="65206-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="65206-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65206-113">EXAMPLES</span></span>

### <span data-ttu-id="65206-114">Przykład 1. Aktualizowanie asn bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="65206-115">Pierwsze polecenie otrzymuje wirtualną bramę sieciową o nazwie Gateway01 należącą do grupy zasobów ResourceGroup001 i przechowuje ją u zmiennej o nazwie $Gateway Drugie polecenie aktualizuje wirtualną bramę sieciową przechowywaną w zmiennym $Gateway.</span><span class="sxs-lookup"><span data-stu-id="65206-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="65206-116">To polecenie ustawia również asn na 1337.</span><span class="sxs-lookup"><span data-stu-id="65206-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="65206-117">Przykład 2. Dodawanie zasad IPsec do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="65206-118">Pierwsze polecenie otrzymuje wirtualną bramę sieciową o nazwie Gateway01 należącą do grupy zasobów ResourceGroup001 i przechowuje ją w zmiennej o nazwie $Gateway Drugie polecenie tworzy obiekt zasad ipsec sieci Vpn zgodnie z określonymi parametrami ipsec.</span><span class="sxs-lookup"><span data-stu-id="65206-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="65206-119">Trzecie polecenie aktualizuje bramę sieci wirtualnej przechowywaną w zmiennym $Gateway.</span><span class="sxs-lookup"><span data-stu-id="65206-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="65206-120">To polecenie ustawia również niestandardowe zasady ipsec sieci vpn określone w obiekcie $vpnclientipsecpolicy w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="65206-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="65206-121">Przykład 3. Dodawanie/aktualizowanie tagów do istniejącej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="65206-122">Pierwsze polecenie otrzymuje wirtualną bramę sieciową o nazwie Gateway01 należącą do grupy zasobów ResourceGroup001 i przechowuje je w zmiennej o nazwie $Gateway Drugie polecenie aktualizuje bramę sieci wirtualnej o tagach @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span><span class="sxs-lookup"><span data-stu-id="65206-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="65206-123">Przykład 4. Dodawanie/aktualizowanie konfiguracji uwierzytelniania AAD dla usługi VpnClient istniejącej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="65206-124">Pierwsze polecenie otrzymuje wirtualną bramę sieciową o nazwie Gateway01 należącą do grupy zasobów ResourceGroup001 i przechowuje je w zmiennej o nazwie $Gateway Drugie polecenie aktualizuje bramę sieci wirtualnej Gateway01 przy użyciu params konfiguracji uwierzytelniania AAD:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span><span class="sxs-lookup"><span data-stu-id="65206-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="65206-125">Trzecie polecenie usuwa konfigurację uwierzytelniania AAD z usługi VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="65206-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="65206-126">Przykład 5. Dodawanie/aktualizowanie adresów IpConfigurationBgpPeeringAddresses do istniejącej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
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
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="65206-127">Pierwsze polecenie otrzymuje wirtualną bramę sieciową o nazwie Gateway01 należącą do grupy zasobów ResourceGroup001 i przechowuje ją u zmiennej o nazwie $Gateway Drugie polecenie przypisuje wartość identyfikatora IpConfiguration Bramy sieci wirtualnej Gateway01 do zmiennej ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="65206-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="65206-128">Trzecie polecenie przypisuje listę adresów do listy adresowej1.</span><span class="sxs-lookup"><span data-stu-id="65206-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="65206-129">Czwarte polecenie utworzyło obiekt PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="65206-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="65206-130">Piąte polecenie ustawiło tę nową utworzoną konfigurację PSIpConfigurationBgpPeeringAddress na Adres IpConfigurationBgpPeeringAddresses i zaktualizuj bramę.</span><span class="sxs-lookup"><span data-stu-id="65206-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="65206-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65206-131">PARAMETERS</span></span>

### <span data-ttu-id="65206-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="65206-132">-AadAudienceId</span></span>
<span data-ttu-id="65206-133">Opcja uwierzytelniania AAD P2S:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="65206-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="65206-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="65206-134">-AadIssuerUri</span></span>
<span data-ttu-id="65206-135">Opcja uwierzytelniania AAD P2S:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="65206-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="65206-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="65206-136">-AadTenantUri</span></span>
<span data-ttu-id="65206-137">Opcja uwierzytelniania AAD P2S:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="65206-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="65206-138">— AsJob</span><span class="sxs-lookup"><span data-stu-id="65206-138">-AsJob</span></span>
<span data-ttu-id="65206-139">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="65206-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65206-140">— Asn</span><span class="sxs-lookup"><span data-stu-id="65206-140">-Asn</span></span>
<span data-ttu-id="65206-141">AsN bramy sieci wirtualnej, która służy do skonfigurowania sesji BGP w przypadku podkołowy IPsec</span><span class="sxs-lookup"><span data-stu-id="65206-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="65206-142">- CustomRoute</span><span class="sxs-lookup"><span data-stu-id="65206-142">-CustomRoute</span></span>
<span data-ttu-id="65206-143">Niestandardowe trasy buforu adresów określone przez klienta</span><span class="sxs-lookup"><span data-stu-id="65206-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="65206-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65206-144">-DefaultProfile</span></span>
<span data-ttu-id="65206-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65206-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65206-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="65206-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="65206-147">Oflaguj, aby wyłączyć funkcję Aktywne aktywne w bramie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="65206-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="65206-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="65206-149">Flaga w celu włączenia funkcji Aktywne aktywne w bramie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="65206-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="65206-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="65206-151">Flaga w celu włączenia funkcji Aktywne aktywne w bramie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-151">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65206-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="65206-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="65206-153">Witryna domyślna do wymusania na wymusze wydychania.</span><span class="sxs-lookup"><span data-stu-id="65206-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="65206-154">Jeśli zostanie określona witryna domyślna, cały ruch internetowy z sieci vnet bramy jest przekierowyowyny do tej witryny.</span><span class="sxs-lookup"><span data-stu-id="65206-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="65206-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="65206-155">-GatewaySku</span></span>
<span data-ttu-id="65206-156">SKU bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="65206-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="65206-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="65206-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="65206-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65206-159">- PeerWeight</span><span class="sxs-lookup"><span data-stu-id="65206-159">-PeerWeight</span></span>
<span data-ttu-id="65206-160">Waga dodana do tras poznanych za pośrednictwem BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="65206-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="65206-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="65206-161">-RadiusServerAddress</span></span>
<span data-ttu-id="65206-162">Adres serwera o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="65206-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="65206-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="65206-163">-RadiusServerList</span></span>
<span data-ttu-id="65206-164">P2S multiple external Radius servers.</span><span class="sxs-lookup"><span data-stu-id="65206-164">P2S multiple external Radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65206-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="65206-165">-RadiusServerSecret</span></span>
<span data-ttu-id="65206-166">Tajny serwer o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="65206-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="65206-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="65206-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="65206-168">Oflaguj, aby usunąć uwierzytelnianie AAD dla klienta P2S z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="65206-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="65206-169">— Tag</span><span class="sxs-lookup"><span data-stu-id="65206-169">-Tag</span></span>
<span data-ttu-id="65206-170">Adres serwera o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="65206-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="65206-171">— VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65206-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="65206-172">Obiekt bramy sieci wirtualnej, w przypadku których są bazowe modyfikacje.</span><span class="sxs-lookup"><span data-stu-id="65206-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="65206-173">Można to pobrać za pomocą programu Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65206-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="65206-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="65206-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="65206-175">Miejsce na adresy, z których można przydzielić adresy IP klientów sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="65206-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="65206-176">Nie powinno to nakładać się na sieć wirtualną ani zakresy lokalne.</span><span class="sxs-lookup"><span data-stu-id="65206-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="65206-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="65206-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="65206-178">Lista zasad IPSec dla protokołów klienckich SIECI VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="65206-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="65206-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="65206-179">-VpnClientProtocol</span></span>
<span data-ttu-id="65206-180">Lista protokołów odsyłki klienta VPN P2S</span><span class="sxs-lookup"><span data-stu-id="65206-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="65206-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="65206-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="65206-182">Lista odwołanych certyfikatów klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="65206-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="65206-183">Klient SIECI VPN prezentujący certyfikat, który jest taki, jak jeden z nich, zostanie mu z dala od komputera.</span><span class="sxs-lookup"><span data-stu-id="65206-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="65206-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="65206-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="65206-185">Lista certyfikatów głównych klienta sieci VPN, których można używać do uwierzytelniania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="65206-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="65206-186">Klienci sieci VPN łączący muszą prezentować certyfikaty wygenerowane na podstawie jednego z tych certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="65206-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="65206-187">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65206-187">-Confirm</span></span>
<span data-ttu-id="65206-188">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65206-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65206-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65206-189">-WhatIf</span></span>
<span data-ttu-id="65206-190">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65206-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65206-191">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65206-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65206-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65206-192">CommonParameters</span></span>
<span data-ttu-id="65206-193">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65206-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65206-194">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65206-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65206-195">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65206-195">INPUTS</span></span>

### <span data-ttu-id="65206-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65206-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="65206-197">System.String</span><span class="sxs-lookup"><span data-stu-id="65206-197">System.String</span></span>

### <span data-ttu-id="65206-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65206-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="65206-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="65206-199">System.String[]</span></span>

### <span data-ttu-id="65206-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="65206-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="65206-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="65206-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="65206-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="65206-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="65206-203">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="65206-203">System.UInt32</span></span>

### <span data-ttu-id="65206-204">System.Int32</span><span class="sxs-lookup"><span data-stu-id="65206-204">System.Int32</span></span>

### <span data-ttu-id="65206-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="65206-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="65206-206">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="65206-206">System.Security.SecureString</span></span>

## <span data-ttu-id="65206-207">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65206-207">OUTPUTS</span></span>

### <span data-ttu-id="65206-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65206-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="65206-209">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65206-209">NOTES</span></span>

## <span data-ttu-id="65206-210">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65206-210">RELATED LINKS</span></span>
