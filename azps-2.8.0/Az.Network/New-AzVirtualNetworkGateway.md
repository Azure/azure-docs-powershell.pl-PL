---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 75857d2c97ace9b06e3f7cdd7f672ac35a6fe34e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869831"
---
# <span data-ttu-id="f88df-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f88df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f88df-102">SYNOPSIS</span></span>
<span data-ttu-id="f88df-103">Tworzy bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f88df-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="f88df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f88df-104">SYNTAX</span></span>

### <span data-ttu-id="f88df-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f88df-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f88df-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f88df-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f88df-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f88df-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f88df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f88df-108">DESCRIPTION</span></span>
<span data-ttu-id="f88df-109">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f88df-110">Polecenie cmdlet **New-AzVirtualNetworkGateway** umożliwia utworzenie obiektu bramy na platformie Azure na podstawie nazwy, nazwy grupy zasobów, lokalizacji i konfiguracji IP oraz typu bramy oraz sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="f88df-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="f88df-111">Możesz również nadać nazwę SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="f88df-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="f88df-112">Jeśli ta brama jest używana w połączeniach punkt-lokacja, należy również uwzględnić pulę adresów klientów VPN, z której mają być przypisywane adresy łączące się z klientami, oraz certyfikat główny klienta sieci VPN używany do uwierzytelniania klientów VPN łączących się z bramą.</span><span class="sxs-lookup"><span data-stu-id="f88df-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="f88df-113">Możesz również wybrać opcję dołączania innych funkcji, takich jak BGP i Active-Active.</span><span class="sxs-lookup"><span data-stu-id="f88df-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="f88df-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f88df-114">EXAMPLES</span></span>

### <span data-ttu-id="f88df-115">1: Tworzenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f88df-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f88df-116">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f88df-117">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="f88df-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="f88df-118">2: Tworzenie bramy sieci wirtualnej za pomocą zewnętrznej konfiguracji RADIUS</span><span class="sxs-lookup"><span data-stu-id="f88df-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f88df-119">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f88df-120">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="f88df-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f88df-121">Powoduje także dodanie zewnętrznego serwera RADIUS o adresie "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="f88df-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="f88df-122">Ponadto zostaną ustawione trasy niestandardowe określone przez klientów na bramie.</span><span class="sxs-lookup"><span data-stu-id="f88df-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f88df-123">3: Tworzenie bramy sieci wirtualnej z ustawieniami P2S</span><span class="sxs-lookup"><span data-stu-id="f88df-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
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

<span data-ttu-id="f88df-124">Powyższy sposób utworzy grupę zasobów, poproś o publiczny adres IP, Utwórz sieć wirtualną i podsieć i Utwórz wirtualną bramę sieciową z ustawieniami P2S, na przykład VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy itp. na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="f88df-125">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typie bramy "VPN," typ sieci VPN "RouteBased", a jednostka SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="f88df-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="f88df-126">Ustawienia sieci VPN zostaną ustawione w bramie, takiej jak VpnProtocol Set jako IKEv2, VpnClientAddressPool jako "201.169.0.0/16", VpnClientRootCertificate ustawiona jako przekazana: clientRootCertName i niestandardowe zasady IPSec sieci VPN przekazano do obiektu: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="f88df-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="f88df-127">Ponadto zostaną ustawione trasy niestandardowe określone przez klientów na bramie.</span><span class="sxs-lookup"><span data-stu-id="f88df-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f88df-128">4: Tworzenie bramy sieci wirtualnej z konfiguracją uwierzytelniania w usłudze AAD dla VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f88df-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="f88df-129">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f88df-130">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="f88df-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f88df-131">Umożliwia także konfigurowanie konfiguracji uwierzytelniania w usłudze AAD: AadTenantUri, AadIssuerUri i AadAudienceId dla VpnClient bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f88df-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="f88df-132">5: Tworzenie bramy sieci wirtualnej z usługą VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f88df-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f88df-133">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f88df-134">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN typu "RouteBased", SKU "VpnGw4" i VpnGatewayGeneration Generation2 włączone.</span><span class="sxs-lookup"><span data-stu-id="f88df-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="f88df-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f88df-135">PARAMETERS</span></span>

### <span data-ttu-id="f88df-136">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="f88df-136">-AadAudienceId</span></span>
<span data-ttu-id="f88df-137">Opcja uwierzytelniania w usłudze AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="f88df-137">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="f88df-138">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="f88df-138">-AadIssuerUri</span></span>
<span data-ttu-id="f88df-139">Opcja uwierzytelniania w usłudze AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="f88df-139">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="f88df-140">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="f88df-140">-AadTenantUri</span></span>
<span data-ttu-id="f88df-141">Opcja uwierzytelniania w usłudze AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="f88df-141">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="f88df-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f88df-142">-AsJob</span></span>
<span data-ttu-id="f88df-143">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f88df-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f88df-144">-ASN</span><span class="sxs-lookup"><span data-stu-id="f88df-144">-Asn</span></span>

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

### <span data-ttu-id="f88df-145">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="f88df-145">-CustomRoute</span></span>
<span data-ttu-id="f88df-146">Trasy niestandardowe AddressPool określone przez klienta</span><span class="sxs-lookup"><span data-stu-id="f88df-146">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="f88df-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88df-147">-DefaultProfile</span></span>
<span data-ttu-id="f88df-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f88df-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f88df-149">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="f88df-149">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="f88df-150">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="f88df-150">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="f88df-151">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f88df-151">-EnableBgp</span></span>

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

### <span data-ttu-id="f88df-152">-Force</span><span class="sxs-lookup"><span data-stu-id="f88df-152">-Force</span></span>
<span data-ttu-id="f88df-153">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88df-153">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f88df-154">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f88df-154">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="f88df-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="f88df-155">-GatewaySku</span></span>

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

### <span data-ttu-id="f88df-156">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="f88df-156">-GatewayType</span></span>

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

### <span data-ttu-id="f88df-157">-Elementy Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="f88df-157">-IpConfigurations</span></span>

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

### <span data-ttu-id="f88df-158">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f88df-158">-Location</span></span>

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

### <span data-ttu-id="f88df-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f88df-159">-Name</span></span>

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

### <span data-ttu-id="f88df-160">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f88df-160">-PeerWeight</span></span>

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

### <span data-ttu-id="f88df-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f88df-161">-RadiusServerAddress</span></span>
<span data-ttu-id="f88df-162">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f88df-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="f88df-163">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f88df-163">-RadiusServerSecret</span></span>
<span data-ttu-id="f88df-164">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f88df-164">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="f88df-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88df-165">-ResourceGroupName</span></span>

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

### <span data-ttu-id="f88df-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="f88df-166">-Tag</span></span>
<span data-ttu-id="f88df-167">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f88df-167">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f88df-168">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f88df-168">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f88df-169">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f88df-169">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="f88df-170">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f88df-170">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f88df-171">Lista zasad IPSec dla protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="f88df-171">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f88df-172">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="f88df-172">-VpnClientProtocol</span></span>
<span data-ttu-id="f88df-173">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="f88df-173">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="f88df-174">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="f88df-174">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="f88df-175">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="f88df-175">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="f88df-176">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f88df-176">-VpnGatewayGeneration</span></span>
<span data-ttu-id="f88df-177">Generowanie tej VirtualNetworkej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="f88df-177">The generation for this VirtualNetwork VPN gateway.</span></span> <span data-ttu-id="f88df-178">Nie może mieć wartości none, jeśli Brama nie jest siecią VPN.</span><span class="sxs-lookup"><span data-stu-id="f88df-178">Must be None if GatewayType is not VPN.</span></span> <span data-ttu-id="f88df-179">Po ustawieniu tej właściwości nie można zmienić w okresie istnienia bramy.</span><span class="sxs-lookup"><span data-stu-id="f88df-179">Once set, this property cannot be changed over the lifetime of the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, Generation1, Generation2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88df-180">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f88df-180">-VpnType</span></span>

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

### <span data-ttu-id="f88df-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f88df-181">-Confirm</span></span>
<span data-ttu-id="f88df-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f88df-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88df-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f88df-183">-WhatIf</span></span>
<span data-ttu-id="f88df-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f88df-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f88df-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f88df-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88df-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88df-186">CommonParameters</span></span>
<span data-ttu-id="f88df-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88df-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88df-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88df-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88df-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f88df-189">INPUTS</span></span>

### <span data-ttu-id="f88df-190">System. String</span><span class="sxs-lookup"><span data-stu-id="f88df-190">System.String</span></span>

### <span data-ttu-id="f88df-191">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f88df-191">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="f88df-192">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f88df-192">System.Boolean</span></span>

### <span data-ttu-id="f88df-193">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-193">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f88df-194">System. String []</span><span class="sxs-lookup"><span data-stu-id="f88df-194">System.String[]</span></span>

### <span data-ttu-id="f88df-195">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="f88df-195">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="f88df-196">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="f88df-196">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="f88df-197">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f88df-197">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f88df-198">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f88df-198">System.UInt32</span></span>

### <span data-ttu-id="f88df-199">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f88df-199">System.Int32</span></span>

### <span data-ttu-id="f88df-200">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f88df-200">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f88df-201">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f88df-201">System.Security.SecureString</span></span>

## <span data-ttu-id="f88df-202">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f88df-202">OUTPUTS</span></span>

### <span data-ttu-id="f88df-203">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-203">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f88df-204">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f88df-204">NOTES</span></span>

## <span data-ttu-id="f88df-205">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f88df-205">RELATED LINKS</span></span>

[<span data-ttu-id="f88df-206">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-206">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f88df-207">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-207">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f88df-208">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-208">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f88df-209">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-209">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f88df-210">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f88df-210">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
