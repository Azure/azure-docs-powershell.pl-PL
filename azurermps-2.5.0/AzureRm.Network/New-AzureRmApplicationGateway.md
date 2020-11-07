---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 73b72c6585fb4c7487b43dc99b3494cdc99bf7a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898321"
---
# <span data-ttu-id="79fe9-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79fe9-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="79fe9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="79fe9-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79fe9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79fe9-104">SYNTAX</span></span>

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
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79fe9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="79fe9-106">Polecenie cmdlet **New-AzureRmApplicationGateway** umożliwia utworzenie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79fe9-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="79fe9-107">Brama aplikacji wymaga wykonania następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="79fe9-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="79fe9-108">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="79fe9-108">A resource group.</span></span>
- <span data-ttu-id="79fe9-109">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="79fe9-109">A virtual network.</span></span>
- <span data-ttu-id="79fe9-110">Pula serwerów zaplecza zawierająca adresy IP serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="79fe9-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="79fe9-111">Ustawienia puli serwerów wewnętrznych.</span><span class="sxs-lookup"><span data-stu-id="79fe9-111">Back-end server pool settings.</span></span> <span data-ttu-id="79fe9-112">Każda pula ma takie ustawienia, jak port, protokół i koligacja oparta na plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="79fe9-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="79fe9-113">Adresy IP frontonu, które są adresami IP otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="79fe9-114">Adres IP frontonu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="79fe9-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="79fe9-115">Porty frontonu, które są portami publicznymi otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="79fe9-116">Ruch, który powoduje, że te porty są przekierowywane do serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="79fe9-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="79fe9-117">Reguła rozsyłania żądań wiążąca odbiornik i pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="79fe9-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="79fe9-118">Reguła określa pulę serwera zaplecza, do której ma być kierowany ruch, gdy trafi na określony detektor.</span><span class="sxs-lookup"><span data-stu-id="79fe9-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="79fe9-119">Odbiornik ma port frontonu, adres IP frontonu, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu SSL (Secure Sockets Layer) (Jeśli skonfigurowano odciążanie protokołu SSL).</span><span class="sxs-lookup"><span data-stu-id="79fe9-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="79fe9-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79fe9-120">EXAMPLES</span></span>

### <span data-ttu-id="79fe9-121">Przykład 1: Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="79fe9-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="79fe9-122">W poniższym przykładzie jest tworzona Brama Application Gateway po utworzeniu grupy zasobów i sieci wirtualnej oraz następujących danych:</span><span class="sxs-lookup"><span data-stu-id="79fe9-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="79fe9-123">Pula serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="79fe9-123">A back-end server pool</span></span>
- <span data-ttu-id="79fe9-124">Ustawienia puli serwerów wewnętrznych</span><span class="sxs-lookup"><span data-stu-id="79fe9-124">Back-end server pool settings</span></span>
- <span data-ttu-id="79fe9-125">Porty frontonu</span><span class="sxs-lookup"><span data-stu-id="79fe9-125">Front-end ports</span></span>
- <span data-ttu-id="79fe9-126">Adresy IP frontonu</span><span class="sxs-lookup"><span data-stu-id="79fe9-126">Front-end IP addresses</span></span>
- <span data-ttu-id="79fe9-127">Reguła rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="79fe9-127">A request routing rule</span></span>

<span data-ttu-id="79fe9-128">Te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="79fe9-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="79fe9-129">Pierwsze polecenie powoduje utworzenie konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="79fe9-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="79fe9-130">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="79fe9-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="79fe9-131">Trzecie polecenie weryfikuje konfigurację podsieci, a czwarte polecenie weryfikuje, że sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="79fe9-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="79fe9-132">Poniższe polecenia tworzą bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79fe9-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="79fe9-133">Pierwsze polecenie tworzy konfigurację adresu IP o nazwie GatewayIp01 dla podsieci utworzonej wcześniej.</span><span class="sxs-lookup"><span data-stu-id="79fe9-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="79fe9-134">Drugie polecenie tworzy pulę serwerów zaplecza o nazwie Pool01 z listą wewnętrznych adresów IP i przechowuje pulę w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="79fe9-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="79fe9-135">Trzecie polecenie tworzy ustawienia puli serwerów zaplecza i zapisuje ustawienia w zmiennej $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="79fe9-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="79fe9-136">Polecenie Dalej tworzy port frontonu na porcie 80, nazywa je FrontEndPort01 i przechowuje port w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="79fe9-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="79fe9-137">W piątym poleceniu jest tworzony publiczny adres IP przy użyciu polecenia New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="79fe9-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="79fe9-138">Szóste polecenie tworzy konfigurację adresu IP frontonu przy użyciu $PublicIp, nazywa ją FrontEndPortConfig01 i zapisuje ją w zmiennej $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="79fe9-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="79fe9-139">Polecenie siódme powoduje utworzenie odbiornika przy użyciu $FrontEndPort utworzonych $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="79fe9-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="79fe9-140">Polecenie ósmy powoduje utworzenie reguły dla odbiornika.</span><span class="sxs-lookup"><span data-stu-id="79fe9-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="79fe9-141">Dziewiąte polecenie ustawia jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="79fe9-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="79fe9-142">Polecenie dziesiąte powoduje utworzenie bramy przy użyciu obiektów ustawionych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="79fe9-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="79fe9-143">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79fe9-143">PARAMETERS</span></span>

### <span data-ttu-id="79fe9-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79fe9-144">-AsJob</span></span>
<span data-ttu-id="79fe9-145">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="79fe9-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="79fe9-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="79fe9-147">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="79fe9-148">-BackendAddressPools</span></span>
<span data-ttu-id="79fe9-149">Określa listę pul adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="79fe9-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="79fe9-151">Określa listę wewnętrznych ustawień HTTP dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79fe9-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fe9-152">-DefaultProfile</span></span>
<span data-ttu-id="79fe9-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79fe9-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-154">-Force</span><span class="sxs-lookup"><span data-stu-id="79fe9-154">-Force</span></span>
<span data-ttu-id="79fe9-155">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79fe9-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="79fe9-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="79fe9-157">Określa listę konfiguracji adresów IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="79fe9-158">-FrontendPorts</span></span>
<span data-ttu-id="79fe9-159">Określa listę portów frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-159">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="79fe9-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="79fe9-161">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-161">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="79fe9-162">-HttpListeners</span></span>
<span data-ttu-id="79fe9-163">Określa listę detektorów HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-164">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="79fe9-164">-Location</span></span>
<span data-ttu-id="79fe9-165">Określa region, w którym ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-165">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-166">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79fe9-166">-Name</span></span>
<span data-ttu-id="79fe9-167">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-167">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-168">-Badania</span><span class="sxs-lookup"><span data-stu-id="79fe9-168">-Probes</span></span>
<span data-ttu-id="79fe9-169">Określa sondy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-169">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="79fe9-170">-RedirectConfigurations</span></span>
<span data-ttu-id="79fe9-171">Lista konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="79fe9-171">The list of redirect configuration</span></span>

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

### <span data-ttu-id="79fe9-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="79fe9-172">-RequestRoutingRules</span></span>
<span data-ttu-id="79fe9-173">Określa listę reguł rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-173">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79fe9-174">-ResourceGroupName</span></span>
<span data-ttu-id="79fe9-175">Określa nazwę grupy zasobów, w której ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="79fe9-176">-Sku</span></span>
<span data-ttu-id="79fe9-177">Określa jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="79fe9-178">-SslCertificates</span></span>
<span data-ttu-id="79fe9-179">Określa listę certyfikatów SSL (Secure Sockets Layer) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="79fe9-180">-SslPolicy</span></span>
<span data-ttu-id="79fe9-181">Określa zasady protokołu SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-181">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="79fe9-182">-Tag</span></span>
<span data-ttu-id="79fe9-183">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="79fe9-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79fe9-184">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="79fe9-184">For example:</span></span>

<span data-ttu-id="79fe9-185">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="79fe9-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="79fe9-186">-UrlPathMaps</span></span>
<span data-ttu-id="79fe9-187">Określa mapowania ścieżek adresów URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79fe9-187">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="79fe9-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="79fe9-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="79fe9-189">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="79fe9-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="79fe9-190">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration, aby uzyskać WAF.</span><span class="sxs-lookup"><span data-stu-id="79fe9-190">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-191">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79fe9-191">-Confirm</span></span>
<span data-ttu-id="79fe9-192">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79fe9-192">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fe9-193">-WhatIf</span></span>
<span data-ttu-id="79fe9-194">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79fe9-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79fe9-195">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79fe9-195">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fe9-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fe9-196">CommonParameters</span></span>
<span data-ttu-id="79fe9-197">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79fe9-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fe9-198">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fe9-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fe9-199">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79fe9-199">INPUTS</span></span>

## <span data-ttu-id="79fe9-200">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79fe9-200">OUTPUTS</span></span>

### <span data-ttu-id="79fe9-201">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79fe9-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79fe9-202">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79fe9-202">NOTES</span></span>

## <span data-ttu-id="79fe9-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79fe9-203">RELATED LINKS</span></span>

[<span data-ttu-id="79fe9-204">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79fe9-204">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79fe9-205">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="79fe9-205">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="79fe9-206">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="79fe9-206">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="79fe9-207">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="79fe9-207">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="79fe9-208">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="79fe9-208">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="79fe9-209">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="79fe9-209">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="79fe9-210">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="79fe9-210">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="79fe9-211">Nowe — AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="79fe9-211">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="79fe9-212">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79fe9-212">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="79fe9-213">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="79fe9-213">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
