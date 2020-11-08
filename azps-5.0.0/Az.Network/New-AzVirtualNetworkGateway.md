---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232787"
---
# <span data-ttu-id="d4cbb-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4cbb-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d4cbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cbb-103">Tworzy bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d4cbb-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="d4cbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4cbb-104">SYNTAX</span></span>

### <span data-ttu-id="d4cbb-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d4cbb-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4cbb-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4cbb-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4cbb-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4cbb-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4cbb-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4cbb-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4cbb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d4cbb-109">DESCRIPTION</span></span>
<span data-ttu-id="d4cbb-110">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d4cbb-111">Polecenie cmdlet **New-AzVirtualNetworkGateway** umożliwia utworzenie obiektu bramy na platformie Azure na podstawie nazwy, nazwy grupy zasobów, lokalizacji i konfiguracji IP oraz typu bramy oraz sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="d4cbb-112">Możesz również nadać nazwę SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="d4cbb-113">Jeśli ta brama jest używana w połączeniach punkt-lokacja, należy również uwzględnić pulę adresów klientów VPN, z której mają być przypisywane adresy łączące się z klientami, oraz certyfikat główny klienta sieci VPN używany do uwierzytelniania klientów VPN łączących się z bramą.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="d4cbb-114">Możesz również wybrać opcję dołączania innych funkcji, takich jak BGP i Active-Active.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="d4cbb-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4cbb-115">EXAMPLES</span></span>

### <span data-ttu-id="d4cbb-116">Przykład 1: Tworzenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d4cbb-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="d4cbb-117">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d4cbb-118">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="d4cbb-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="d4cbb-119">Przykład 2: Tworzenie bramy sieci wirtualnej z zewnętrzną konfiguracją RADIUS</span><span class="sxs-lookup"><span data-stu-id="d4cbb-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="d4cbb-120">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d4cbb-121">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="d4cbb-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="d4cbb-122">Powoduje także dodanie zewnętrznego serwera RADIUS o adresie "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="d4cbb-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="d4cbb-123">Ponadto zostaną ustawione trasy niestandardowe określone przez klientów na bramie.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="d4cbb-124">Przykład 3: Tworzenie bramy sieci wirtualnej z ustawieniami P2S</span><span class="sxs-lookup"><span data-stu-id="d4cbb-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="d4cbb-125">Powyższy sposób utworzy grupę zasobów, poproś o publiczny adres IP, Utwórz sieć wirtualną i podsieć i Utwórz wirtualną bramę sieciową z ustawieniami P2S, na przykład VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy itp. na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="d4cbb-126">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typie bramy "VPN," typ sieci VPN "RouteBased", a jednostka SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="d4cbb-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="d4cbb-127">Ustawienia sieci VPN zostaną ustawione w bramie, takiej jak VpnProtocol Set jako IKEv2, VpnClientAddressPool jako "201.169.0.0/16", VpnClientRootCertificate ustawiona jako przekazana: clientRootCertName i niestandardowe zasady IPSec sieci VPN przekazano do obiektu: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="d4cbb-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="d4cbb-128">Ponadto zostaną ustawione trasy niestandardowe określone przez klientów na bramie.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="d4cbb-129">Przykład 4: Tworzenie bramy sieci wirtualnej z konfiguracją uwierzytelniania w usłudze AAD dla VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="d4cbb-130">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d4cbb-131">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="d4cbb-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="d4cbb-132">Umożliwia także konfigurowanie konfiguracji uwierzytelniania w usłudze AAD: AadTenantUri, AadIssuerUri i AadAudienceId dla VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="d4cbb-133">Przykład 5: Tworzenie bramy sieci wirtualnej z usługą VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="d4cbb-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="d4cbb-134">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d4cbb-135">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN typu "RouteBased", SKU "VpnGw4" i VpnGatewayGeneration Generation2 włączone.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="d4cbb-136">Przykład 6: Tworzenie bramy sieci wirtualnej z usługą IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="d4cbb-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="d4cbb-137">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="d4cbb-138">ipconfigurationId1 element ipconfiguration bramy został właśnie utworzony i jest przechowywany w ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="d4cbb-139">Brama będzie nosiła nazwę "gateway1" w grupie zasobów "resourcegroup1resourcegroup1" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami adresów IP Bgppeering adres zapisany w zmiennej "gw1ipconfBgp1", typ bramy "VPN", typ sieci VPN "RouteBased", jednostki SKU "VpnGw4" i VpnGatewayGeneration Generation2 włączone.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="d4cbb-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4cbb-140">PARAMETERS</span></span>

### <span data-ttu-id="d4cbb-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="d4cbb-141">-AadAudienceId</span></span>
<span data-ttu-id="d4cbb-142">Opcja uwierzytelniania w usłudze AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="d4cbb-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="d4cbb-143">-AadIssuerUri</span></span>
<span data-ttu-id="d4cbb-144">Opcja uwierzytelniania w usłudze AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="d4cbb-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="d4cbb-145">-AadTenantUri</span></span>
<span data-ttu-id="d4cbb-146">Opcja uwierzytelniania w usłudze AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="d4cbb-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4cbb-147">-AsJob</span></span>
<span data-ttu-id="d4cbb-148">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d4cbb-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4cbb-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="d4cbb-149">-Asn</span></span>
<span data-ttu-id="d4cbb-150">Protokół ASN bramy sieci wirtualnej dla protokołu BGP przez sieć VPN</span><span class="sxs-lookup"><span data-stu-id="d4cbb-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="d4cbb-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="d4cbb-151">-CustomRoute</span></span>
<span data-ttu-id="d4cbb-152">Trasy niestandardowe AddressPool określone przez klienta</span><span class="sxs-lookup"><span data-stu-id="d4cbb-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="d4cbb-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cbb-153">-DefaultProfile</span></span>
<span data-ttu-id="d4cbb-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4cbb-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d4cbb-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d4cbb-156">Flaga włączenia aktywnej aktywnej funkcji w bramie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d4cbb-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="d4cbb-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d4cbb-157">-EnableBgp</span></span>
<span data-ttu-id="d4cbb-158">Flaga EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d4cbb-158">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d4cbb-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="d4cbb-160">Flaga włączenia prywatnego adresu IP bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d4cbb-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="d4cbb-161">-Force</span><span class="sxs-lookup"><span data-stu-id="d4cbb-161">-Force</span></span>
<span data-ttu-id="d4cbb-162">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="d4cbb-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d4cbb-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d4cbb-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="d4cbb-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d4cbb-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="d4cbb-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d4cbb-165">-GatewaySku</span></span>
<span data-ttu-id="d4cbb-166">Warstwa SKU bramy</span><span class="sxs-lookup"><span data-stu-id="d4cbb-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="d4cbb-167">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="d4cbb-167">-GatewayType</span></span>
<span data-ttu-id="d4cbb-168">Typ tej bramy sieci wirtualnej: sieć VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d4cbb-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="d4cbb-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="d4cbb-170">BgpPeeringAddresses dla bramy sieci wirtualnej bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="d4cbb-171">-Elementy Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="d4cbb-171">-IpConfigurations</span></span>
<span data-ttu-id="d4cbb-172">Elementy Ipconfiguration bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-172">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-173">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d4cbb-173">-Location</span></span>
<span data-ttu-id="d4cbb-174">pozycję.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-174">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-175">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4cbb-175">-Name</span></span>
<span data-ttu-id="d4cbb-176">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-176">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d4cbb-177">-PeerWeight</span></span>
<span data-ttu-id="d4cbb-178">Waga dodana do tras dodanych za pośrednictwem protokołu BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d4cbb-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="d4cbb-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d4cbb-179">-RadiusServerAddress</span></span>
<span data-ttu-id="d4cbb-180">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="d4cbb-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="d4cbb-181">-RadiusServerList</span></span>
<span data-ttu-id="d4cbb-182">P2S wielu zewnętrznych serwerów serwerów RADIUS.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="d4cbb-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d4cbb-183">-RadiusServerSecret</span></span>
<span data-ttu-id="d4cbb-184">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="d4cbb-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4cbb-185">-ResourceGroupName</span></span>
<span data-ttu-id="d4cbb-186">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-186">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4cbb-187">-Tag</span></span>
<span data-ttu-id="d4cbb-188">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-188">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d4cbb-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="d4cbb-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="d4cbb-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="d4cbb-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d4cbb-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d4cbb-192">Lista zasad IPSec dla protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d4cbb-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d4cbb-193">-VpnClientProtocol</span></span>
<span data-ttu-id="d4cbb-194">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="d4cbb-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="d4cbb-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d4cbb-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d4cbb-196">Lista VpnClientCertificates, które mają zostać odwołane.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="d4cbb-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d4cbb-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d4cbb-198">Lista VpnClientRootCertificates, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="d4cbb-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="d4cbb-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="d4cbb-200">Generowanie tej VirtualNetworkej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="d4cbb-201">Nie może mieć wartości none, jeśli Brama nie jest siecią VPN.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-201">Must be None if GatewayType is not VPN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="d4cbb-202">-VpnType</span></span>
<span data-ttu-id="d4cbb-203">Typ sieci VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="d4cbb-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cbb-204">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4cbb-204">-Confirm</span></span>
<span data-ttu-id="d4cbb-205">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4cbb-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4cbb-206">-WhatIf</span></span>
<span data-ttu-id="d4cbb-207">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4cbb-208">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4cbb-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cbb-209">CommonParameters</span></span>
<span data-ttu-id="d4cbb-210">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cbb-211">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4cbb-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cbb-212">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4cbb-212">INPUTS</span></span>

### <span data-ttu-id="d4cbb-213">System. String</span><span class="sxs-lookup"><span data-stu-id="d4cbb-213">System.String</span></span>

### <span data-ttu-id="d4cbb-214">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="d4cbb-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="d4cbb-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4cbb-215">System.Boolean</span></span>

### <span data-ttu-id="d4cbb-216">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4cbb-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d4cbb-217">System. String []</span><span class="sxs-lookup"><span data-stu-id="d4cbb-217">System.String[]</span></span>

### <span data-ttu-id="d4cbb-218">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="d4cbb-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="d4cbb-219">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="d4cbb-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="d4cbb-220">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d4cbb-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d4cbb-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="d4cbb-221">System.UInt32</span></span>

### <span data-ttu-id="d4cbb-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d4cbb-222">System.Int32</span></span>

### <span data-ttu-id="d4cbb-223">Microsoft. Azure. Commands. Network. models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="d4cbb-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="d4cbb-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d4cbb-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d4cbb-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d4cbb-225">System.Security.SecureString</span></span>

## <span data-ttu-id="d4cbb-226">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4cbb-226">OUTPUTS</span></span>

### <span data-ttu-id="d4cbb-227">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d4cbb-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d4cbb-228">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4cbb-228">NOTES</span></span>

## <span data-ttu-id="d4cbb-229">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4cbb-229">RELATED LINKS</span></span>
