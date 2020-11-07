---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 7a818ba86092200c31d9d0a217042e6f6dce4857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717615"
---
# <span data-ttu-id="57365-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="57365-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57365-102">SYNOPSIS</span></span>
<span data-ttu-id="57365-103">Tworzy bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57365-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57365-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57365-104">SYNTAX</span></span>

### <span data-ttu-id="57365-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="57365-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57365-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="57365-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57365-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57365-107">DESCRIPTION</span></span>
<span data-ttu-id="57365-108">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="57365-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="57365-109">Polecenie cmdlet **New-AzureRmVirtualNetworkGateway** umożliwia utworzenie obiektu bramy na platformie Azure na podstawie nazwy, nazwy grupy zasobów, lokalizacji i konfiguracji IP oraz typu bramy oraz sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="57365-109">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="57365-110">Możesz również nadać nazwę SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="57365-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="57365-111">Jeśli ta brama jest używana w połączeniach punkt-lokacja, należy również uwzględnić pulę adresów klientów VPN, z której mają być przypisywane adresy łączące się z klientami, oraz certyfikat główny klienta sieci VPN używany do uwierzytelniania klientów VPN łączących się z bramą.</span><span class="sxs-lookup"><span data-stu-id="57365-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="57365-112">Możesz również wybrać opcję dołączania innych funkcji, takich jak BGP i Active-Active.</span><span class="sxs-lookup"><span data-stu-id="57365-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="57365-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57365-113">EXAMPLES</span></span>

### <span data-ttu-id="57365-114">1: Tworzenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="57365-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="57365-115">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="57365-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="57365-116">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="57365-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="57365-117">2: Tworzenie bramy sieci wirtualnej za pomocą zewnętrznej konfiguracji RADIUS</span><span class="sxs-lookup"><span data-stu-id="57365-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="57365-118">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="57365-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="57365-119">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="57365-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="57365-120">Powoduje także dodanie zewnętrznego serwera RADIUS o adresie "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="57365-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="57365-121">1: Tworzenie bramy sieci wirtualnej z ustawieniami P2S</span><span class="sxs-lookup"><span data-stu-id="57365-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzureRmVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="57365-122">Powyższy sposób utworzy grupę zasobów, poproś o publiczny adres IP, Utwórz sieć wirtualną i podsieć i Utwórz wirtualną bramę sieciową z ustawieniami P2S, na przykład VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy itp. na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="57365-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="57365-123">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typie bramy "VPN," typ sieci VPN "RouteBased", a jednostka SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="57365-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="57365-124">Ustawienia sieci VPN zostaną ustawione w bramie, takiej jak VpnProtocol Set jako IKEv2, VpnClientAddressPool jako "201.169.0.0/16", VpnClientRootCertificate ustawiona jako przekazana: clientRootCertName i niestandardowe zasady IPSec sieci VPN przekazano do obiektu: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="57365-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="57365-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57365-125">PARAMETERS</span></span>

### <span data-ttu-id="57365-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57365-126">-AsJob</span></span>
<span data-ttu-id="57365-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57365-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57365-128">-ASN</span><span class="sxs-lookup"><span data-stu-id="57365-128">-Asn</span></span>

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

### <span data-ttu-id="57365-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57365-129">-DefaultProfile</span></span>
<span data-ttu-id="57365-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57365-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57365-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="57365-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="57365-132">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="57365-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="57365-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="57365-133">-EnableBgp</span></span>

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

### <span data-ttu-id="57365-134">-Force</span><span class="sxs-lookup"><span data-stu-id="57365-134">-Force</span></span>
<span data-ttu-id="57365-135">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="57365-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57365-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="57365-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="57365-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="57365-137">-GatewaySku</span></span>

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

### <span data-ttu-id="57365-138">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="57365-138">-GatewayType</span></span>

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

### <span data-ttu-id="57365-139">-Elementy Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="57365-139">-IpConfigurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57365-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="57365-140">-Location</span></span>

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

### <span data-ttu-id="57365-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57365-141">-Name</span></span>

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

### <span data-ttu-id="57365-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="57365-142">-PeerWeight</span></span>

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

### <span data-ttu-id="57365-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="57365-143">-RadiusServerAddress</span></span>
<span data-ttu-id="57365-144">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="57365-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="57365-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="57365-145">-RadiusServerSecret</span></span>
<span data-ttu-id="57365-146">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="57365-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="57365-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57365-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="57365-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="57365-148">-Tag</span></span>
<span data-ttu-id="57365-149">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="57365-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="57365-150">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="57365-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="57365-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="57365-151">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="57365-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="57365-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="57365-153">Lista zasad IPSec dla protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="57365-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="57365-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="57365-154">-VpnClientProtocol</span></span>
<span data-ttu-id="57365-155">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="57365-155">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="57365-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="57365-156">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="57365-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="57365-157">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="57365-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="57365-158">-VpnType</span></span>

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

### <span data-ttu-id="57365-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57365-159">-Confirm</span></span>
<span data-ttu-id="57365-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57365-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57365-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57365-161">-WhatIf</span></span>
<span data-ttu-id="57365-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57365-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57365-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57365-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57365-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57365-164">CommonParameters</span></span>
<span data-ttu-id="57365-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57365-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57365-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57365-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57365-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57365-167">INPUTS</span></span>

### <span data-ttu-id="57365-168">System. String</span><span class="sxs-lookup"><span data-stu-id="57365-168">System.String</span></span>

### <span data-ttu-id="57365-169">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSVirtualNetworkGatewayIpConfiguration; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57365-169">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="57365-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57365-170">System.Boolean</span></span>

### <span data-ttu-id="57365-171">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="57365-172">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="57365-172">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="57365-173">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSVpnClientRootCertificate; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57365-173">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="57365-174">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSVpnClientRevokedCertificate; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57365-174">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="57365-175">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSIpsecPolicy; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57365-175">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="57365-176">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="57365-176">System.UInt32</span></span>

### <span data-ttu-id="57365-177">System. Int32</span><span class="sxs-lookup"><span data-stu-id="57365-177">System.Int32</span></span>

### <span data-ttu-id="57365-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="57365-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="57365-179">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="57365-179">System.Security.SecureString</span></span>

## <span data-ttu-id="57365-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57365-180">OUTPUTS</span></span>

### <span data-ttu-id="57365-181">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="57365-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57365-182">NOTES</span></span>

## <span data-ttu-id="57365-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57365-183">RELATED LINKS</span></span>

[<span data-ttu-id="57365-184">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-184">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57365-185">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-185">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57365-186">Resetowanie — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-186">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57365-187">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-187">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57365-188">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57365-188">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
