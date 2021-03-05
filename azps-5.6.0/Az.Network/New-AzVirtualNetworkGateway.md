---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977882"
---
# <span data-ttu-id="5341e-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5341e-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="5341e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5341e-102">SYNOPSIS</span></span>
<span data-ttu-id="5341e-103">Tworzy wirtualną bramę sieciową</span><span class="sxs-lookup"><span data-stu-id="5341e-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="5341e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5341e-104">SYNTAX</span></span>

### <span data-ttu-id="5341e-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5341e-105">Default (Default)</span></span>
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

### <span data-ttu-id="5341e-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="5341e-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="5341e-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5341e-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="5341e-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="5341e-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="5341e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5341e-109">DESCRIPTION</span></span>
<span data-ttu-id="5341e-110">Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="5341e-111">Polecenie cmdlet **New-AzVirtualNetworkGateway** tworzy obiekt bramy na platformie Azure na podstawie konfiguracji Nazwa, Nazwa grupy zasobów, Lokalizacja i IP, a także typu bramy i typu sieci VPN (jeśli vpn).</span><span class="sxs-lookup"><span data-stu-id="5341e-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="5341e-112">Możesz również nazwać SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="5341e-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="5341e-113">Jeśli ta brama jest używana na potrzeby połączeń typu "punkt-witryna", konieczne będzie także dołączenie puli adresów klientów sieci VPN, z której będą przypisywane adresy do klientów łączących się, oraz certyfikatu głównego klienta sieci VPN używanego do uwierzytelniania klientów sieci VPN łączących się z bramą.</span><span class="sxs-lookup"><span data-stu-id="5341e-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="5341e-114">Możesz także wybrać, czy uwzględnić inne funkcje, takie jak BGP i Active-Active.</span><span class="sxs-lookup"><span data-stu-id="5341e-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="5341e-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5341e-115">EXAMPLES</span></span>

### <span data-ttu-id="5341e-116">Przykład 1. Tworzenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5341e-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="5341e-117">Powyższe spowoduje utworzenie grupy zasobów, żądanie publicznego adresu IP, utworzenie sieci wirtualnej i podsieci oraz utworzenie wirtualnej bramy sieciowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="5341e-118">Brama będzie nazywana "myNGW" w grupie zasobów "vnet-gateway" w lokalizacji "Zjednoczone Królestwo" z wcześniej utworzonymi konfiguracjami IP zapisanymi w zmiennej "ngwIPConfig", typ bramy "VPN", typ vpn "RouteBased" i wersja SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="5341e-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="5341e-119">Przykład 2. Tworzenie wirtualnej bramy sieciowej z konfiguracją promieni zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="5341e-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="5341e-120">Powyższe spowoduje utworzenie grupy zasobów, żądanie publicznego adresu IP, utworzenie sieci wirtualnej i podsieci oraz utworzenie wirtualnej bramy sieciowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="5341e-121">Brama będzie nazywana "myNGW" w grupie zasobów "vnet-gateway" w lokalizacji "Zjednoczone Królestwo" z wcześniej utworzonymi konfiguracjami IP zapisanymi w zmiennej "ngwIPConfig", typ bramy "VPN", typ vpn "RouteBased" i wersja SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="5341e-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="5341e-122">Dodaje także zewnętrzny serwer promienia z adresem "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="5341e-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="5341e-123">Ponadto skonfiguruje trasy niestandardowe określone przez klientów w bramie.</span><span class="sxs-lookup"><span data-stu-id="5341e-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="5341e-124">Przykład 3. Tworzenie wirtualnej bramy sieciowej z ustawieniami P2S</span><span class="sxs-lookup"><span data-stu-id="5341e-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="5341e-125">Powyższe spowoduje utworzenie grupy zasobów, zażądanie publicznego adresu IP, utworzenie sieci wirtualnej i podsieci oraz utworzenie wirtualnej bramy sieciowej z ustawieniami P2S, np. VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy itp. na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="5341e-126">Brama będzie nazywana "myNGW" w grupie zasobów "vnet-gateway" w lokalizacji "Zjednoczone Królestwo" z wcześniej utworzonymi konfiguracjami IP zapisanymi w zmiennej "ngwIPConfig", typ bramy "VPN", typ vpn "RouteBased" i sku "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="5341e-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="5341e-127">Ustawienia sieci VPN będą ustawione na bramie, takiej jak VpnProtocol, ustawione jako Ikev2, VpnClientAddressPool jako "201.169.0.0/16", vpnClientRootCertificate ustawione jako przekazane: clientRootCertName i niestandardowe zasady ipsec vpn przekazywane w obiekcie:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="5341e-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="5341e-128">Ponadto skonfiguruje trasy niestandardowe określone przez klientów w bramie.</span><span class="sxs-lookup"><span data-stu-id="5341e-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="5341e-129">Przykład 4. Tworzenie wirtualnej bramy sieciowej za pomocą konfiguracji uwierzytelniania AAD dla usługi VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5341e-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="5341e-130">Powyższe spowoduje utworzenie grupy zasobów, żądanie publicznego adresu IP, utworzenie sieci wirtualnej i podsieci oraz utworzenie wirtualnej bramy sieciowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="5341e-131">Brama będzie nazywana "myNGW" w grupie zasobów "vnet-gateway" w lokalizacji "Zjednoczone Królestwo" z wcześniej utworzonymi konfiguracjami IP zapisanymi w zmiennej "ngwIPConfig", typ bramy "VPN", typ vpn "RouteBased" i wersja SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="5341e-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="5341e-132">Konfiguruje też konfiguracje uwierzytelniania AAD: AadTenantUri, AadIssuerUri i AadAudienceId dla klienta VpnClient wirtualnej bramy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5341e-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="5341e-133">Przykład 5. Tworzenie wirtualnej bramy sieciowej przy użyciu sieci VpnGateway Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="5341e-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="5341e-134">Powyższe spowoduje utworzenie grupy zasobów, żądanie publicznego adresu IP, utworzenie sieci wirtualnej i podsieci oraz utworzenie wirtualnej bramy sieciowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="5341e-135">Brama będzie nazywana "myNGW" w grupie zasobów "vnet-gateway" w lokalizacji "Zjednoczone Królestwo", z wcześniej utworzonymi konfiguracjami IP zapisanymi w zmiennej "ngwIPConfig", typ bramy "VPN", typ vpn "RouteBased", wersja SKU "VpnGw4" i VpnGateway Generation2.</span><span class="sxs-lookup"><span data-stu-id="5341e-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="5341e-136">Przykład 6. Tworzenie wirtualnej bramy sieciowej przy użyciu protokołu IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="5341e-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="5341e-137">Powyższe spowoduje utworzenie grupy zasobów, żądanie publicznego adresu IP, utworzenie sieci wirtualnej i podsieci oraz utworzenie wirtualnej bramy sieciowej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="5341e-138">IpconfigurationId1 (1) konfiguracji ipconfiguration bramy właśnie utworzonej i zapisanej w konfiguracji ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="5341e-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="5341e-139">Brama będzie nazywana "bramą1" w grupie zasobów "resourcegroup1resourcegroup1" w lokalizacji "Zjednoczone Królestwo", z wcześniej utworzonymi konfiguracjami IP adresu bgppeering zapisanego w zmiennej "gw1ipconfBgp1", typ bramy "VPN", typ vpn "RouteBased", sku "VpnGw4" i włączono vpnGateway Generation2.</span><span class="sxs-lookup"><span data-stu-id="5341e-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="5341e-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5341e-140">PARAMETERS</span></span>

### <span data-ttu-id="5341e-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="5341e-141">-AadAudienceId</span></span>
<span data-ttu-id="5341e-142">Opcja uwierzytelniania AAD P2S:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="5341e-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="5341e-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="5341e-143">-AadIssuerUri</span></span>
<span data-ttu-id="5341e-144">Opcja uwierzytelniania AAD P2S:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="5341e-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="5341e-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="5341e-145">-AadTenantUri</span></span>
<span data-ttu-id="5341e-146">Opcja uwierzytelniania AAD P2S:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="5341e-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="5341e-147">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5341e-147">-AsJob</span></span>
<span data-ttu-id="5341e-148">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5341e-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5341e-149">— Asn</span><span class="sxs-lookup"><span data-stu-id="5341e-149">-Asn</span></span>
<span data-ttu-id="5341e-150">AsN bramy sieci wirtualnej dla BGP przez sieć VPN</span><span class="sxs-lookup"><span data-stu-id="5341e-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="5341e-151">— CustomRoute</span><span class="sxs-lookup"><span data-stu-id="5341e-151">-CustomRoute</span></span>
<span data-ttu-id="5341e-152">Niestandardowe trasy buforu adresów określone przez klienta</span><span class="sxs-lookup"><span data-stu-id="5341e-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="5341e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5341e-153">-DefaultProfile</span></span>
<span data-ttu-id="5341e-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5341e-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5341e-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="5341e-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="5341e-156">Flaga w celu włączenia funkcji Aktywne aktywne w bramie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5341e-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="5341e-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5341e-157">-EnableBgp</span></span>
<span data-ttu-id="5341e-158">Flaga EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5341e-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="5341e-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5341e-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="5341e-160">Flaga w celu włączenia prywatnego adresu IPAddress w wirtualnej bramie sieciowej</span><span class="sxs-lookup"><span data-stu-id="5341e-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="5341e-161">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5341e-161">-Force</span></span>
<span data-ttu-id="5341e-162">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="5341e-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5341e-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5341e-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="5341e-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5341e-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="5341e-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="5341e-165">-GatewaySku</span></span>
<span data-ttu-id="5341e-166">Warstwa SKU bramy</span><span class="sxs-lookup"><span data-stu-id="5341e-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="5341e-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="5341e-167">-GatewayType</span></span>
<span data-ttu-id="5341e-168">Typ tej bramy sieci wirtualnej: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5341e-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="5341e-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="5341e-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="5341e-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="5341e-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="5341e-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="5341e-171">-IpConfigurations</span></span>
<span data-ttu-id="5341e-172">Konfiguracje IpConfiguration dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5341e-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="5341e-173">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5341e-173">-Location</span></span>
<span data-ttu-id="5341e-174">.</span><span class="sxs-lookup"><span data-stu-id="5341e-174">location.</span></span>

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

### <span data-ttu-id="5341e-175">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5341e-175">-Name</span></span>
<span data-ttu-id="5341e-176">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5341e-176">The resource name.</span></span>

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

### <span data-ttu-id="5341e-177">- PeerWeight</span><span class="sxs-lookup"><span data-stu-id="5341e-177">-PeerWeight</span></span>
<span data-ttu-id="5341e-178">Waga dodana do tras poznanych za pośrednictwem BGP z tej bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5341e-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="5341e-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="5341e-179">-RadiusServerAddress</span></span>
<span data-ttu-id="5341e-180">Adres serwera o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="5341e-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="5341e-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="5341e-181">-RadiusServerList</span></span>
<span data-ttu-id="5341e-182">P2S multiple external Radius server servers.</span><span class="sxs-lookup"><span data-stu-id="5341e-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="5341e-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="5341e-183">-RadiusServerSecret</span></span>
<span data-ttu-id="5341e-184">Serwer O2S o promieniu zewnętrznym tajny.</span><span class="sxs-lookup"><span data-stu-id="5341e-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="5341e-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5341e-185">-ResourceGroupName</span></span>
<span data-ttu-id="5341e-186">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5341e-186">The resource group name.</span></span>

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

### <span data-ttu-id="5341e-187">— Tag</span><span class="sxs-lookup"><span data-stu-id="5341e-187">-Tag</span></span>
<span data-ttu-id="5341e-188">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="5341e-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5341e-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="5341e-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="5341e-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="5341e-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="5341e-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="5341e-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="5341e-192">Lista zasad IPSec dla protokołów klienckich SIECI VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="5341e-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="5341e-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="5341e-193">-VpnClientProtocol</span></span>
<span data-ttu-id="5341e-194">Lista protokołów odsyłki klienta P2S VPN</span><span class="sxs-lookup"><span data-stu-id="5341e-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="5341e-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="5341e-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="5341e-196">Lista vpnClientCertificates do odwołania.</span><span class="sxs-lookup"><span data-stu-id="5341e-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="5341e-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="5341e-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="5341e-198">Lista VpnClientRootCertificates do dodania.</span><span class="sxs-lookup"><span data-stu-id="5341e-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="5341e-199">-VpnGateway Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="5341e-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="5341e-200">Generowanie tej bramy VPN w środowisku VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="5341e-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="5341e-201">Jeśli gatewayType nie ma połączenia VPN, musi być typu None.</span><span class="sxs-lookup"><span data-stu-id="5341e-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="5341e-202">- VpnType</span><span class="sxs-lookup"><span data-stu-id="5341e-202">-VpnType</span></span>
<span data-ttu-id="5341e-203">Typ połączenia Vpn:PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="5341e-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="5341e-204">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5341e-204">-Confirm</span></span>
<span data-ttu-id="5341e-205">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5341e-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5341e-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5341e-206">-WhatIf</span></span>
<span data-ttu-id="5341e-207">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5341e-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5341e-208">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5341e-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5341e-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5341e-209">CommonParameters</span></span>
<span data-ttu-id="5341e-210">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5341e-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5341e-211">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5341e-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5341e-212">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5341e-212">INPUTS</span></span>

### <span data-ttu-id="5341e-213">System.String</span><span class="sxs-lookup"><span data-stu-id="5341e-213">System.String</span></span>

### <span data-ttu-id="5341e-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="5341e-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="5341e-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5341e-215">System.Boolean</span></span>

### <span data-ttu-id="5341e-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5341e-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="5341e-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5341e-217">System.String[]</span></span>

### <span data-ttu-id="5341e-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="5341e-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="5341e-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="5341e-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="5341e-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="5341e-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="5341e-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="5341e-221">System.UInt32</span></span>

### <span data-ttu-id="5341e-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5341e-222">System.Int32</span></span>

### <span data-ttu-id="5341e-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="5341e-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="5341e-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5341e-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5341e-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="5341e-225">System.Security.SecureString</span></span>

## <span data-ttu-id="5341e-226">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5341e-226">OUTPUTS</span></span>

### <span data-ttu-id="5341e-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5341e-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5341e-228">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5341e-228">NOTES</span></span>

## <span data-ttu-id="5341e-229">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5341e-229">RELATED LINKS</span></span>
