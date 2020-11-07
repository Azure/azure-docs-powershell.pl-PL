---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 55ed36aa2ea09e871d4e109a35207f12c43f57d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719280"
---
# <span data-ttu-id="a6705-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="a6705-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6705-102">SYNOPSIS</span></span>
<span data-ttu-id="a6705-103">Tworzy bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a6705-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6705-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6705-104">SYNTAX</span></span>

### <span data-ttu-id="a6705-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a6705-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6705-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6705-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6705-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a6705-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6705-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a6705-108">DESCRIPTION</span></span>
<span data-ttu-id="a6705-109">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a6705-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="a6705-110">Polecenie cmdlet **New-AzureRmVirtualNetworkGateway** umożliwia utworzenie obiektu bramy na platformie Azure na podstawie nazwy, nazwy grupy zasobów, lokalizacji i konfiguracji IP oraz typu bramy oraz sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="a6705-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="a6705-111">Możesz również nadać nazwę SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="a6705-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="a6705-112">Jeśli ta brama jest używana w połączeniach punkt-lokacja, należy również uwzględnić pulę adresów klientów VPN, z której mają być przypisywane adresy łączące się z klientami, oraz certyfikat główny klienta sieci VPN używany do uwierzytelniania klientów VPN łączących się z bramą.</span><span class="sxs-lookup"><span data-stu-id="a6705-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="a6705-113">Możesz również wybrać opcję dołączania innych funkcji, takich jak BGP i Active-Active.</span><span class="sxs-lookup"><span data-stu-id="a6705-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="a6705-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6705-114">EXAMPLES</span></span>

### <span data-ttu-id="a6705-115">1: Tworzenie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a6705-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="a6705-116">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a6705-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="a6705-117">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="a6705-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="a6705-118">2: Tworzenie bramy sieci wirtualnej za pomocą zewnętrznej konfiguracji RADIUS</span><span class="sxs-lookup"><span data-stu-id="a6705-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="a6705-119">Powyższy sposób utworzy grupę zasobów, zażądaj publicznego adresu IP, utworzenia sieci wirtualnej i podsieci oraz utworzenia bramy sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a6705-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="a6705-120">Brama będzie nosiła nazwę "myNGW" w grupie zasobów "VNET-Gateway" w lokalizacji "Wielka Brytania" z wcześniej utworzonymi konfiguracjami protokołu IP zapisaną w zmiennej "ngwIPConfig", typ bramy "VPN", typ sieci VPN "RouteBased" oraz "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="a6705-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="a6705-121">Powoduje także dodanie zewnętrznego serwera RADIUS o adresie "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="a6705-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="a6705-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6705-122">PARAMETERS</span></span>

### <span data-ttu-id="a6705-123">-ASN</span><span class="sxs-lookup"><span data-stu-id="a6705-123">-Asn</span></span>
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

### <span data-ttu-id="a6705-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6705-124">-DefaultProfile</span></span>
<span data-ttu-id="a6705-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6705-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="a6705-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a6705-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="a6705-127">Włączanie funkcji aktywnej.</span><span class="sxs-lookup"><span data-stu-id="a6705-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="a6705-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a6705-128">-EnableBgp</span></span>
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

### <span data-ttu-id="a6705-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a6705-129">-Force</span></span>
<span data-ttu-id="a6705-130">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a6705-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a6705-131">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a6705-131">-GatewayDefaultSite</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-132">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a6705-132">-GatewaySku</span></span>
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

### <span data-ttu-id="a6705-133">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="a6705-133">-GatewayType</span></span>
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

### <span data-ttu-id="a6705-134">-Elementy Ipconfiguration</span><span class="sxs-lookup"><span data-stu-id="a6705-134">-IpConfigurations</span></span>
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

### <span data-ttu-id="a6705-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a6705-135">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6705-136">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a6705-137">-PeerWeight</span></span>
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

### <span data-ttu-id="a6705-138">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a6705-138">-RadiusServerAddress</span></span>
<span data-ttu-id="a6705-139">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="a6705-139">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="a6705-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a6705-140">-RadiusServerSecret</span></span>
<span data-ttu-id="a6705-141">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="a6705-141">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="a6705-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6705-142">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6705-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6705-143">-Tag</span></span>
<span data-ttu-id="a6705-144">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a6705-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6705-145">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a6705-145">For example:</span></span>

<span data-ttu-id="a6705-146">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a6705-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a6705-147">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6705-147">-VpnClientAddressPool</span></span>
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

### <span data-ttu-id="a6705-148">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="a6705-148">-VpnClientProtocol</span></span>
<span data-ttu-id="a6705-149">Lista protokołów tunelowania klienta sieci VPN P2S</span><span class="sxs-lookup"><span data-stu-id="a6705-149">The list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="a6705-150">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="a6705-150">-VpnClientRevokedCertificates</span></span>
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

### <span data-ttu-id="a6705-151">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="a6705-151">-VpnClientRootCertificates</span></span>
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

### <span data-ttu-id="a6705-152">-VpnType</span><span class="sxs-lookup"><span data-stu-id="a6705-152">-VpnType</span></span>
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

### <span data-ttu-id="a6705-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6705-153">-Confirm</span></span>
<span data-ttu-id="a6705-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6705-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6705-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6705-155">-WhatIf</span></span>
<span data-ttu-id="a6705-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6705-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6705-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6705-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6705-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6705-158">CommonParameters</span></span>
<span data-ttu-id="a6705-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6705-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6705-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6705-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6705-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6705-161">INPUTS</span></span>

## <span data-ttu-id="a6705-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6705-162">OUTPUTS</span></span>

### <span data-ttu-id="a6705-163">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a6705-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6705-164">NOTES</span></span>

## <span data-ttu-id="a6705-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6705-165">RELATED LINKS</span></span>

[<span data-ttu-id="a6705-166">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-166">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a6705-167">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-167">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a6705-168">Resetowanie — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-168">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a6705-169">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-169">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a6705-170">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6705-170">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
