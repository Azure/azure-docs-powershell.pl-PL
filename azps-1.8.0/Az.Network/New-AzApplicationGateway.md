---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 131a068faec659b8215790a1bcdc1609b3494cb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709400"
---
# <span data-ttu-id="34e8d-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e8d-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="34e8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="34e8d-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-103">Creates an application gateway.</span></span>

## <span data-ttu-id="34e8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34e8d-104">SYNTAX</span></span>

### <span data-ttu-id="34e8d-105">IdentityByUserAssignedIdentityId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34e8d-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e8d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="34e8d-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e8d-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="34e8d-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e8d-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="34e8d-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity> [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e8d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="34e8d-109">DESCRIPTION</span></span>
<span data-ttu-id="34e8d-110">Polecenie cmdlet **New-AzApplicationGateway** umożliwia utworzenie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34e8d-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="34e8d-111">Brama aplikacji wymaga wykonania następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="34e8d-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="34e8d-112">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="34e8d-112">A resource group.</span></span>
- <span data-ttu-id="34e8d-113">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="34e8d-113">A virtual network.</span></span>
- <span data-ttu-id="34e8d-114">Pula serwerów zaplecza zawierająca adresy IP serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="34e8d-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="34e8d-115">Ustawienia puli serwerów wewnętrznych.</span><span class="sxs-lookup"><span data-stu-id="34e8d-115">Back-end server pool settings.</span></span> <span data-ttu-id="34e8d-116">Każda pula ma takie ustawienia, jak port, protokół i koligacja oparta na plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="34e8d-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="34e8d-117">Adresy IP frontonu, które są adresami IP otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="34e8d-118">Adres IP frontonu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="34e8d-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="34e8d-119">Porty frontonu, które są portami publicznymi otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="34e8d-120">Ruch, który powoduje, że te porty są przekierowywane do serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="34e8d-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="34e8d-121">Reguła rozsyłania żądań wiążąca odbiornik i pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="34e8d-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="34e8d-122">Reguła określa pulę serwera zaplecza, do której ma być kierowany ruch, gdy trafi na określony detektor.</span><span class="sxs-lookup"><span data-stu-id="34e8d-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="34e8d-123">Odbiornik ma port frontonu, adres IP frontonu, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu SSL (Secure Sockets Layer) (Jeśli skonfigurowano odciążanie protokołu SSL).</span><span class="sxs-lookup"><span data-stu-id="34e8d-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="34e8d-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34e8d-124">EXAMPLES</span></span>

### <span data-ttu-id="34e8d-125">Przykład 1: Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="34e8d-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="34e8d-126">W poniższym przykładzie jest tworzona Brama Application Gateway po utworzeniu grupy zasobów i sieci wirtualnej oraz następujących danych:</span><span class="sxs-lookup"><span data-stu-id="34e8d-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="34e8d-127">Pula serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="34e8d-127">A back-end server pool</span></span>
- <span data-ttu-id="34e8d-128">Ustawienia puli serwerów wewnętrznych</span><span class="sxs-lookup"><span data-stu-id="34e8d-128">Back-end server pool settings</span></span>
- <span data-ttu-id="34e8d-129">Porty frontonu</span><span class="sxs-lookup"><span data-stu-id="34e8d-129">Front-end ports</span></span>
- <span data-ttu-id="34e8d-130">Adresy IP frontonu</span><span class="sxs-lookup"><span data-stu-id="34e8d-130">Front-end IP addresses</span></span>
- <span data-ttu-id="34e8d-131">Reguła rozsyłania żądań te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="34e8d-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="34e8d-132">Pierwsze polecenie powoduje utworzenie konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="34e8d-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="34e8d-133">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="34e8d-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="34e8d-134">Trzecie polecenie weryfikuje konfigurację podsieci, a czwarte polecenie weryfikuje, że sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="34e8d-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="34e8d-135">Poniższe polecenia tworzą bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="34e8d-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="34e8d-136">Pierwsze polecenie tworzy konfigurację adresu IP o nazwie GatewayIp01 dla podsieci utworzonej wcześniej.</span><span class="sxs-lookup"><span data-stu-id="34e8d-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="34e8d-137">Drugie polecenie tworzy pulę serwerów zaplecza o nazwie Pool01 z listą wewnętrznych adresów IP i przechowuje pulę w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="34e8d-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="34e8d-138">Trzecie polecenie tworzy ustawienia puli serwerów zaplecza i zapisuje ustawienia w zmiennej $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="34e8d-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="34e8d-139">Polecenie Dalej tworzy port frontonu na porcie 80, nazywa je FrontEndPort01 i przechowuje port w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="34e8d-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="34e8d-140">W piątym poleceniu jest tworzony publiczny adres IP przy użyciu polecenia New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="34e8d-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="34e8d-141">Szóste polecenie tworzy konfigurację adresu IP frontonu przy użyciu $PublicIp, nazywa ją FrontEndPortConfig01 i zapisuje ją w zmiennej $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="34e8d-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="34e8d-142">Polecenie siódme powoduje utworzenie odbiornika przy użyciu $FrontEndPort utworzonych $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="34e8d-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="34e8d-143">Polecenie ósmy powoduje utworzenie reguły dla odbiornika.</span><span class="sxs-lookup"><span data-stu-id="34e8d-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="34e8d-144">Dziewiąte polecenie ustawia jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="34e8d-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="34e8d-145">Polecenie dziesiąte powoduje utworzenie bramy przy użyciu obiektów ustawionych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="34e8d-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="34e8d-146">Przykład 2: Tworzenie bramy aplikacji przy użyciu tożsamości UserAssigned</span><span class="sxs-lookup"><span data-stu-id="34e8d-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="34e8d-147">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34e8d-147">PARAMETERS</span></span>

### <span data-ttu-id="34e8d-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34e8d-148">-AsJob</span></span>
<span data-ttu-id="34e8d-149">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34e8d-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34e8d-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="34e8d-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="34e8d-151">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e8d-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="34e8d-153">Konfiguracja autoskalowania</span><span class="sxs-lookup"><span data-stu-id="34e8d-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="34e8d-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="34e8d-154">-BackendAddressPools</span></span>
<span data-ttu-id="34e8d-155">Określa listę pul adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="34e8d-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="34e8d-157">Określa listę wewnętrznych ustawień HTTP dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="34e8d-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e8d-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="34e8d-159">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="34e8d-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e8d-160">-DefaultProfile</span></span>
<span data-ttu-id="34e8d-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34e8d-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e8d-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="34e8d-162">-EnableFIPS</span></span>
<span data-ttu-id="34e8d-163">Czy włączono opcję FIPS.</span><span class="sxs-lookup"><span data-stu-id="34e8d-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="34e8d-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="34e8d-164">-EnableHttp2</span></span>
<span data-ttu-id="34e8d-165">Czy HTTP2 jest włączony.</span><span class="sxs-lookup"><span data-stu-id="34e8d-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="34e8d-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="34e8d-166">-FirewallPolicy</span></span>
<span data-ttu-id="34e8d-167">Konfiguracja zapory</span><span class="sxs-lookup"><span data-stu-id="34e8d-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="34e8d-168">-FirewallPolicyId</span></span>
<span data-ttu-id="34e8d-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="34e8d-169">FirewallPolicyId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-170">-Force</span><span class="sxs-lookup"><span data-stu-id="34e8d-170">-Force</span></span>
<span data-ttu-id="34e8d-171">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34e8d-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34e8d-172">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="34e8d-172">-FrontendIPConfigurations</span></span>
<span data-ttu-id="34e8d-173">Określa listę konfiguracji adresów IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-173">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-174">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="34e8d-174">-FrontendPorts</span></span>
<span data-ttu-id="34e8d-175">Określa listę portów frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-175">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-176">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="34e8d-176">-GatewayIPConfigurations</span></span>
<span data-ttu-id="34e8d-177">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-177">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-178">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="34e8d-178">-HttpListeners</span></span>
<span data-ttu-id="34e8d-179">Określa listę detektorów HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-179">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-180">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="34e8d-180">-Identity</span></span>
<span data-ttu-id="34e8d-181">Tożsamość bramy aplikacji, która ma być przypisana do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-181">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-182">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34e8d-182">-Location</span></span>
<span data-ttu-id="34e8d-183">Określa region, w którym ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-183">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="34e8d-184">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34e8d-184">-Name</span></span>
<span data-ttu-id="34e8d-185">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-185">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="34e8d-186">-Badania</span><span class="sxs-lookup"><span data-stu-id="34e8d-186">-Probes</span></span>
<span data-ttu-id="34e8d-187">Określa sondy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-187">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-188">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="34e8d-188">-RedirectConfigurations</span></span>
<span data-ttu-id="34e8d-189">Lista konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="34e8d-189">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-190">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="34e8d-190">-RequestRoutingRules</span></span>
<span data-ttu-id="34e8d-191">Określa listę reguł rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-191">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e8d-192">-ResourceGroupName</span></span>
<span data-ttu-id="34e8d-193">Określa nazwę grupy zasobów, w której ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-193">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="34e8d-194">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34e8d-194">-RewriteRuleSet</span></span>
<span data-ttu-id="34e8d-195">Lista RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34e8d-195">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-196">-SKU</span><span class="sxs-lookup"><span data-stu-id="34e8d-196">-Sku</span></span>
<span data-ttu-id="34e8d-197">Określa jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-197">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="34e8d-198">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="34e8d-198">-SslCertificates</span></span>
<span data-ttu-id="34e8d-199">Określa listę certyfikatów SSL (Secure Sockets Layer) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-199">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-200">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="34e8d-200">-SslPolicy</span></span>
<span data-ttu-id="34e8d-201">Określa zasady protokołu SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-201">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="34e8d-202">-Tag</span><span class="sxs-lookup"><span data-stu-id="34e8d-202">-Tag</span></span>
<span data-ttu-id="34e8d-203">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="34e8d-203">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34e8d-204">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="34e8d-204">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="34e8d-205">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34e8d-205">-TrustedRootCertificate</span></span>
<span data-ttu-id="34e8d-206">Lista zaufanych certyfikatów głównych</span><span class="sxs-lookup"><span data-stu-id="34e8d-206">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-207">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="34e8d-207">-UrlPathMaps</span></span>
<span data-ttu-id="34e8d-208">Określa mapowania ścieżek adresów URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-208">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-209">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="34e8d-209">-UserAssignedIdentityId</span></span>
<span data-ttu-id="34e8d-210">Identyfikator ResourceId przypisanego użytkownikowi tożsamości, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-210">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-211">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e8d-211">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="34e8d-212">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="34e8d-212">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="34e8d-213">Możesz użyć polecenia cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration, aby uzyskać WAF.</span><span class="sxs-lookup"><span data-stu-id="34e8d-213">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="34e8d-214">-Zone</span><span class="sxs-lookup"><span data-stu-id="34e8d-214">-Zone</span></span>
<span data-ttu-id="34e8d-215">Lista stref dostępności oznaczająca lokalizację, z której musi pochodzić Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34e8d-215">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e8d-216">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34e8d-216">-Confirm</span></span>
<span data-ttu-id="34e8d-217">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e8d-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e8d-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e8d-218">-WhatIf</span></span>
<span data-ttu-id="34e8d-219">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e8d-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e8d-220">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34e8d-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e8d-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e8d-221">CommonParameters</span></span>
<span data-ttu-id="34e8d-222">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e8d-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e8d-223">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e8d-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e8d-224">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34e8d-224">INPUTS</span></span>

### <span data-ttu-id="34e8d-225">System. String</span><span class="sxs-lookup"><span data-stu-id="34e8d-225">System.String</span></span>

### <span data-ttu-id="34e8d-226">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="34e8d-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="34e8d-227">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="34e8d-227">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="34e8d-228">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="34e8d-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="34e8d-229">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="34e8d-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="34e8d-230">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="34e8d-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="34e8d-231">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="34e8d-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="34e8d-232">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="34e8d-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="34e8d-233">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="34e8d-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="34e8d-234">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="34e8d-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="34e8d-235">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="34e8d-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="34e8d-236">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="34e8d-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="34e8d-237">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="34e8d-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="34e8d-238">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="34e8d-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="34e8d-239">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="34e8d-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="34e8d-240">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="34e8d-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="34e8d-241">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="34e8d-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="34e8d-242">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e8d-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="34e8d-243">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e8d-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="34e8d-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="34e8d-244">System.Collections.Hashtable</span></span>

## <span data-ttu-id="34e8d-245">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34e8d-245">OUTPUTS</span></span>

### <span data-ttu-id="34e8d-246">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e8d-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34e8d-247">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34e8d-247">NOTES</span></span>

## <span data-ttu-id="34e8d-248">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34e8d-248">RELATED LINKS</span></span>

[<span data-ttu-id="34e8d-249">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34e8d-249">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="34e8d-250">Nowe — AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="34e8d-250">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="34e8d-251">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="34e8d-251">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="34e8d-252">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="34e8d-252">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="34e8d-253">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="34e8d-253">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="34e8d-254">Nowe — AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e8d-254">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="34e8d-255">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34e8d-255">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="34e8d-256">Nowe — AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="34e8d-256">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="34e8d-257">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34e8d-257">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="34e8d-258">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34e8d-258">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)