---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: b6a7854d3ddf3c3d444418e08717577a8a2ac172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717571"
---
# <span data-ttu-id="36da2-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36da2-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="36da2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36da2-102">SYNOPSIS</span></span>
<span data-ttu-id="36da2-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36da2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36da2-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36da2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36da2-105">DESCRIPTION</span></span>
<span data-ttu-id="36da2-106">Polecenie cmdlet **New-AzureRmApplicationGateway** umożliwia utworzenie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36da2-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="36da2-107">Brama aplikacji wymaga wykonania następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="36da2-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="36da2-108">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="36da2-108">A resource group.</span></span>
- <span data-ttu-id="36da2-109">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="36da2-109">A virtual network.</span></span>
- <span data-ttu-id="36da2-110">Pula serwerów zaplecza zawierająca adresy IP serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="36da2-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="36da2-111">Ustawienia puli serwerów wewnętrznych.</span><span class="sxs-lookup"><span data-stu-id="36da2-111">Back-end server pool settings.</span></span> <span data-ttu-id="36da2-112">Każda pula ma takie ustawienia, jak port, protokół i koligacja oparta na plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="36da2-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="36da2-113">Adresy IP frontonu, które są adresami IP otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="36da2-114">Adres IP frontonu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="36da2-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="36da2-115">Porty frontonu, które są portami publicznymi otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="36da2-116">Ruch, który powoduje, że te porty są przekierowywane do serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="36da2-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="36da2-117">Reguła rozsyłania żądań wiążąca odbiornik i pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="36da2-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="36da2-118">Reguła określa pulę serwera zaplecza, do której ma być kierowany ruch, gdy trafi na określony detektor.</span><span class="sxs-lookup"><span data-stu-id="36da2-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="36da2-119">Odbiornik ma port frontonu, adres IP frontonu, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu SSL (Secure Sockets Layer) (Jeśli skonfigurowano odciążanie protokołu SSL).</span><span class="sxs-lookup"><span data-stu-id="36da2-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="36da2-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36da2-120">EXAMPLES</span></span>

### <span data-ttu-id="36da2-121">Przykład 1: Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="36da2-121">Example 1: Create an application gateway</span></span>
```
PS C:\>$ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} PS C:\>$Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet PS C:\>$GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name $PublicIpName -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name $listenerName  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $ FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="36da2-122">W poniższym przykładzie jest tworzona Brama Application Gateway po utworzeniu grupy zasobów i sieci wirtualnej oraz następujących danych:</span><span class="sxs-lookup"><span data-stu-id="36da2-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="36da2-123">Pula serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="36da2-123">A back-end server pool</span></span>
- <span data-ttu-id="36da2-124">Ustawienia puli serwerów wewnętrznych</span><span class="sxs-lookup"><span data-stu-id="36da2-124">Back-end server pool settings</span></span>
- <span data-ttu-id="36da2-125">Porty frontonu</span><span class="sxs-lookup"><span data-stu-id="36da2-125">Front-end ports</span></span>
- <span data-ttu-id="36da2-126">Adresy IP frontonu</span><span class="sxs-lookup"><span data-stu-id="36da2-126">Front-end IP addresses</span></span>
- <span data-ttu-id="36da2-127">Reguła rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="36da2-127">A request routing rule</span></span>

<span data-ttu-id="36da2-128">Te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="36da2-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="36da2-129">Pierwsze polecenie powoduje utworzenie konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="36da2-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="36da2-130">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="36da2-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="36da2-131">Trzecie polecenie weryfikuje konfigurację podsieci, a czwarte polecenie weryfikuje, że sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="36da2-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="36da2-132">Poniższe polecenia tworzą bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="36da2-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="36da2-133">Pierwsze polecenie tworzy konfigurację adresu IP o nazwie GatewayIp01 dla podsieci utworzonej wcześniej.</span><span class="sxs-lookup"><span data-stu-id="36da2-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="36da2-134">Drugie polecenie tworzy pulę serwerów zaplecza o nazwie Pool01 z listą wewnętrznych adresów IP i przechowuje pulę w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="36da2-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="36da2-135">Trzecie polecenie tworzy ustawienia puli serwerów zaplecza i zapisuje ustawienia w zmiennej $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="36da2-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="36da2-136">Polecenie Dalej tworzy port frontonu na porcie 80, nazywa je FrontEndPort01 i przechowuje port w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="36da2-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="36da2-137">W piątym poleceniu jest tworzony publiczny adres IP przy użyciu polecenia New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="36da2-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="36da2-138">Szóste polecenie tworzy konfigurację adresu IP frontonu przy użyciu $PublicIp, nazywa ją FrontEndPortConfig01 i zapisuje ją w zmiennej $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="36da2-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="36da2-139">Polecenie siódme powoduje utworzenie odbiornika przy użyciu $FrontEndPort utworzonych $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="36da2-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="36da2-140">Polecenie ósmy powoduje utworzenie reguły dla odbiornika.</span><span class="sxs-lookup"><span data-stu-id="36da2-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="36da2-141">Dziewiąte polecenie ustawia jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="36da2-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="36da2-142">Polecenie dziesiąte powoduje utworzenie bramy przy użyciu obiektów ustawionych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="36da2-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="36da2-143">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36da2-143">PARAMETERS</span></span>

### <span data-ttu-id="36da2-144">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="36da2-144">-AuthenticationCertificates</span></span>
<span data-ttu-id="36da2-145">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-145">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-146">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="36da2-146">-BackendAddressPools</span></span>
<span data-ttu-id="36da2-147">Określa listę pul adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-147">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-148">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="36da2-148">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="36da2-149">Określa listę wewnętrznych ustawień HTTP dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="36da2-149">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-150">-Force</span><span class="sxs-lookup"><span data-stu-id="36da2-150">-Force</span></span>
<span data-ttu-id="36da2-151">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="36da2-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36da2-152">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="36da2-152">-FrontendIPConfigurations</span></span>
<span data-ttu-id="36da2-153">Określa listę konfiguracji adresów IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-153">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-154">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="36da2-154">-FrontendPorts</span></span>
<span data-ttu-id="36da2-155">Określa listę portów frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-155">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-156">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="36da2-156">-GatewayIPConfigurations</span></span>
<span data-ttu-id="36da2-157">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-157">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-158">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="36da2-158">-HttpListeners</span></span>
<span data-ttu-id="36da2-159">Określa listę detektorów HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-159">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36da2-160">-Location</span></span>
<span data-ttu-id="36da2-161">Określa region, w którym ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-161">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="36da2-162">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36da2-162">-Name</span></span>
<span data-ttu-id="36da2-163">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-163">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="36da2-164">-Badania</span><span class="sxs-lookup"><span data-stu-id="36da2-164">-Probes</span></span>
<span data-ttu-id="36da2-165">Określa sondy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-165">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-166">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="36da2-166">-RedirectConfigurations</span></span>
<span data-ttu-id="36da2-167">Lista konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="36da2-167">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-168">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="36da2-168">-RequestRoutingRules</span></span>
<span data-ttu-id="36da2-169">Określa listę reguł rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-169">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36da2-170">-ResourceGroupName</span></span>
<span data-ttu-id="36da2-171">Określa nazwę grupy zasobów, w której ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-171">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="36da2-172">-SKU</span><span class="sxs-lookup"><span data-stu-id="36da2-172">-Sku</span></span>
<span data-ttu-id="36da2-173">Określa jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-173">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-174">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="36da2-174">-SslCertificates</span></span>
<span data-ttu-id="36da2-175">Określa listę certyfikatów SSL (Secure Sockets Layer) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-175">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-176">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="36da2-176">-SslPolicy</span></span>
<span data-ttu-id="36da2-177">Określa zasady protokołu SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-177">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="36da2-178">-Tag</span></span>
<span data-ttu-id="36da2-179">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="36da2-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36da2-180">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="36da2-180">For example:</span></span>

<span data-ttu-id="36da2-181">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="36da2-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36da2-182">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="36da2-182">-UrlPathMaps</span></span>
<span data-ttu-id="36da2-183">Określa mapowania ścieżek adresów URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36da2-183">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-184">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36da2-184">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="36da2-185">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="36da2-185">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="36da2-186">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration, aby uzyskać WAF.</span><span class="sxs-lookup"><span data-stu-id="36da2-186">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36da2-187">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36da2-187">-Confirm</span></span>
<span data-ttu-id="36da2-188">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36da2-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36da2-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36da2-189">-WhatIf</span></span>
<span data-ttu-id="36da2-190">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36da2-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36da2-191">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36da2-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36da2-192">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36da2-192">-DefaultProfile</span></span>
<span data-ttu-id="36da2-193">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36da2-193">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36da2-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36da2-194">CommonParameters</span></span>
<span data-ttu-id="36da2-195">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36da2-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36da2-196">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36da2-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36da2-197">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36da2-197">INPUTS</span></span>

## <span data-ttu-id="36da2-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36da2-198">OUTPUTS</span></span>

### <span data-ttu-id="36da2-199">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36da2-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36da2-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36da2-200">NOTES</span></span>

## <span data-ttu-id="36da2-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36da2-201">RELATED LINKS</span></span>

[<span data-ttu-id="36da2-202">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="36da2-202">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="36da2-203">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="36da2-203">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="36da2-204">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="36da2-204">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="36da2-205">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="36da2-205">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="36da2-206">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36da2-206">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="36da2-207">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="36da2-207">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="36da2-208">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36da2-208">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="36da2-209">Nowe — AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="36da2-209">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="36da2-210">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36da2-210">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="36da2-211">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="36da2-211">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
