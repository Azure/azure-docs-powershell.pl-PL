---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543703"
---
# <span data-ttu-id="1a598-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a598-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="1a598-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a598-102">SYNOPSIS</span></span>
<span data-ttu-id="1a598-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a598-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a598-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
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
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a598-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a598-105">DESCRIPTION</span></span>
<span data-ttu-id="1a598-106">Polecenie cmdlet **New-AzureRmApplicationGateway** umożliwia utworzenie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a598-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="1a598-107">Brama aplikacji wymaga wykonania następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="1a598-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="1a598-108">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a598-108">A resource group.</span></span>
- <span data-ttu-id="1a598-109">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="1a598-109">A virtual network.</span></span>
- <span data-ttu-id="1a598-110">Pula serwerów zaplecza zawierająca adresy IP serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1a598-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="1a598-111">Ustawienia puli serwerów wewnętrznych.</span><span class="sxs-lookup"><span data-stu-id="1a598-111">Back-end server pool settings.</span></span> <span data-ttu-id="1a598-112">Każda pula ma takie ustawienia, jak port, protokół i koligacja oparta na plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="1a598-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="1a598-113">Adresy IP frontonu, które są adresami IP otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="1a598-114">Adres IP frontonu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="1a598-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="1a598-115">Porty frontonu, które są portami publicznymi otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="1a598-116">Ruch, który powoduje, że te porty są przekierowywane do serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1a598-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="1a598-117">Reguła rozsyłania żądań wiążąca odbiornik i pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1a598-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="1a598-118">Reguła określa pulę serwera zaplecza, do której ma być kierowany ruch, gdy trafi na określony detektor.</span><span class="sxs-lookup"><span data-stu-id="1a598-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="1a598-119">Odbiornik ma port frontonu, adres IP frontonu, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu SSL (Secure Sockets Layer) (Jeśli skonfigurowano odciążanie protokołu SSL).</span><span class="sxs-lookup"><span data-stu-id="1a598-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="1a598-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a598-120">EXAMPLES</span></span>

### <span data-ttu-id="1a598-121">Przykład 1: Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1a598-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="1a598-122">W poniższym przykładzie jest tworzona Brama Application Gateway po utworzeniu grupy zasobów i sieci wirtualnej oraz następujących danych:</span><span class="sxs-lookup"><span data-stu-id="1a598-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="1a598-123">Pula serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="1a598-123">A back-end server pool</span></span>
- <span data-ttu-id="1a598-124">Ustawienia puli serwerów wewnętrznych</span><span class="sxs-lookup"><span data-stu-id="1a598-124">Back-end server pool settings</span></span>
- <span data-ttu-id="1a598-125">Porty frontonu</span><span class="sxs-lookup"><span data-stu-id="1a598-125">Front-end ports</span></span>
- <span data-ttu-id="1a598-126">Adresy IP frontonu</span><span class="sxs-lookup"><span data-stu-id="1a598-126">Front-end IP addresses</span></span>
- <span data-ttu-id="1a598-127">Reguła rozsyłania żądań te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="1a598-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="1a598-128">Pierwsze polecenie powoduje utworzenie konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="1a598-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="1a598-129">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="1a598-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="1a598-130">Trzecie polecenie weryfikuje konfigurację podsieci, a czwarte polecenie weryfikuje, że sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="1a598-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="1a598-131">Poniższe polecenia tworzą bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1a598-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="1a598-132">Pierwsze polecenie tworzy konfigurację adresu IP o nazwie GatewayIp01 dla podsieci utworzonej wcześniej.</span><span class="sxs-lookup"><span data-stu-id="1a598-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="1a598-133">Drugie polecenie tworzy pulę serwerów zaplecza o nazwie Pool01 z listą wewnętrznych adresów IP i przechowuje pulę w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="1a598-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="1a598-134">Trzecie polecenie tworzy ustawienia puli serwerów zaplecza i zapisuje ustawienia w zmiennej $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="1a598-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="1a598-135">Polecenie Dalej tworzy port frontonu na porcie 80, nazywa je FrontEndPort01 i przechowuje port w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="1a598-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="1a598-136">W piątym poleceniu jest tworzony publiczny adres IP przy użyciu polecenia New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="1a598-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="1a598-137">Szóste polecenie tworzy konfigurację adresu IP frontonu przy użyciu $PublicIp, nazywa ją FrontEndPortConfig01 i zapisuje ją w zmiennej $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1a598-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="1a598-138">Polecenie siódme powoduje utworzenie odbiornika przy użyciu $FrontEndPort utworzonych $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1a598-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="1a598-139">Polecenie ósmy powoduje utworzenie reguły dla odbiornika.</span><span class="sxs-lookup"><span data-stu-id="1a598-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="1a598-140">Dziewiąte polecenie ustawia jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="1a598-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="1a598-141">Polecenie dziesiąte powoduje utworzenie bramy przy użyciu obiektów ustawionych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="1a598-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="1a598-142">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a598-142">PARAMETERS</span></span>

### <span data-ttu-id="1a598-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a598-143">-AsJob</span></span>
<span data-ttu-id="1a598-144">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1a598-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a598-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="1a598-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="1a598-146">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-146">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-147">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a598-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="1a598-148">Konfiguracja autoskalowania</span><span class="sxs-lookup"><span data-stu-id="1a598-148">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a598-149">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="1a598-149">-BackendAddressPools</span></span>
<span data-ttu-id="1a598-150">Określa listę pul adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-150">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="1a598-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="1a598-152">Określa listę wewnętrznych ustawień HTTP dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1a598-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a598-153">-DefaultProfile</span></span>
<span data-ttu-id="1a598-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a598-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a598-155">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="1a598-155">-EnableFIPS</span></span>
<span data-ttu-id="1a598-156">Czy włączono opcję FIPS.</span><span class="sxs-lookup"><span data-stu-id="1a598-156">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="1a598-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="1a598-157">-EnableHttp2</span></span>
<span data-ttu-id="1a598-158">Czy HTTP2 jest włączony.</span><span class="sxs-lookup"><span data-stu-id="1a598-158">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="1a598-159">-Force</span><span class="sxs-lookup"><span data-stu-id="1a598-159">-Force</span></span>
<span data-ttu-id="1a598-160">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a598-160">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a598-161">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="1a598-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="1a598-162">Określa listę konfiguracji adresów IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-163">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="1a598-163">-FrontendPorts</span></span>
<span data-ttu-id="1a598-164">Określa listę portów frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-164">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-165">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="1a598-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="1a598-166">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-166">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="1a598-167">-HttpListeners</span></span>
<span data-ttu-id="1a598-168">Określa listę detektorów HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-169">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1a598-169">-Location</span></span>
<span data-ttu-id="1a598-170">Określa region, w którym ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-170">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="1a598-171">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a598-171">-Name</span></span>
<span data-ttu-id="1a598-172">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-172">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="1a598-173">-Badania</span><span class="sxs-lookup"><span data-stu-id="1a598-173">-Probes</span></span>
<span data-ttu-id="1a598-174">Określa sondy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-174">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-175">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="1a598-175">-RedirectConfigurations</span></span>
<span data-ttu-id="1a598-176">Lista konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="1a598-176">The list of redirect configuration</span></span>

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

### <span data-ttu-id="1a598-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="1a598-177">-RequestRoutingRules</span></span>
<span data-ttu-id="1a598-178">Określa listę reguł rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-178">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a598-179">-ResourceGroupName</span></span>
<span data-ttu-id="1a598-180">Określa nazwę grupy zasobów, w której ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="1a598-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="1a598-181">-Sku</span></span>
<span data-ttu-id="1a598-182">Określa jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="1a598-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="1a598-183">-SslCertificates</span></span>
<span data-ttu-id="1a598-184">Określa listę certyfikatów SSL (Secure Sockets Layer) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="1a598-185">-SslPolicy</span></span>
<span data-ttu-id="1a598-186">Określa zasady protokołu SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-186">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a598-187">-Tag</span></span>
<span data-ttu-id="1a598-188">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1a598-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1a598-189">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1a598-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1a598-190">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a598-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="1a598-191">Lista zaufanych certyfikatów głównych</span><span class="sxs-lookup"><span data-stu-id="1a598-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a598-192">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="1a598-192">-UrlPathMaps</span></span>
<span data-ttu-id="1a598-193">Określa mapowania ścieżek adresów URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-193">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="1a598-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a598-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="1a598-195">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="1a598-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="1a598-196">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration, aby uzyskać WAF.</span><span class="sxs-lookup"><span data-stu-id="1a598-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="1a598-197">-Zone</span><span class="sxs-lookup"><span data-stu-id="1a598-197">-Zone</span></span>
<span data-ttu-id="1a598-198">Lista stref dostępności oznaczająca lokalizację, z której musi pochodzić Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1a598-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a598-199">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a598-199">-Confirm</span></span>
<span data-ttu-id="1a598-200">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a598-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a598-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a598-201">-WhatIf</span></span>
<span data-ttu-id="1a598-202">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a598-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a598-203">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a598-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a598-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a598-204">CommonParameters</span></span>
<span data-ttu-id="1a598-205">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a598-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a598-206">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a598-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a598-207">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a598-207">INPUTS</span></span>

### <span data-ttu-id="1a598-208">System. String</span><span class="sxs-lookup"><span data-stu-id="1a598-208">System.String</span></span>

### <span data-ttu-id="1a598-209">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1a598-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="1a598-210">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1a598-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="1a598-211">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayIPConfiguration; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-212">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewaySslCertificate; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-213">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayAuthenticationCertificate; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-214">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayFrontendIPConfiguration; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-215">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayFrontendPort; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-216">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayProbe; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-217">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayBackendAddressPool; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-218">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayBackendHttpSettings; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-219">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayHttpListener; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-220">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayUrlPathMap; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-221">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayRequestRoutingRule; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-222">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayRedirectConfiguration; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a598-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1a598-223">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a598-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="1a598-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1a598-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1a598-225">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a598-225">OUTPUTS</span></span>

### <span data-ttu-id="1a598-226">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a598-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a598-227">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a598-227">NOTES</span></span>

## <span data-ttu-id="1a598-228">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a598-228">RELATED LINKS</span></span>

[<span data-ttu-id="1a598-229">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1a598-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1a598-230">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1a598-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="1a598-231">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1a598-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1a598-232">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1a598-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1a598-233">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a598-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1a598-234">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a598-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1a598-235">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1a598-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1a598-236">Nowe — AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1a598-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="1a598-237">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1a598-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="1a598-238">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1a598-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
