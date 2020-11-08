---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 46eb4979c62a5c1f2cb8277ddc1461ee09a339c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053812"
---
# <span data-ttu-id="85a17-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85a17-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="85a17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85a17-102">SYNOPSIS</span></span>
<span data-ttu-id="85a17-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-103">Creates an application gateway.</span></span>

## <span data-ttu-id="85a17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85a17-104">SYNTAX</span></span>

### <span data-ttu-id="85a17-105">IdentityByUserAssignedIdentityId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85a17-105">IdentityByUserAssignedIdentityId (Default)</span></span>
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
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a17-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85a17-106">SetByResourceId</span></span>
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
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a17-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85a17-107">SetByResource</span></span>
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
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a17-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="85a17-108">IdentityByIdentityObject</span></span>
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
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a17-109">Opis</span><span class="sxs-lookup"><span data-stu-id="85a17-109">DESCRIPTION</span></span>
<span data-ttu-id="85a17-110">Polecenie cmdlet **New-AzApplicationGateway** umożliwia utworzenie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85a17-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="85a17-111">Brama aplikacji wymaga wykonania następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="85a17-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="85a17-112">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="85a17-112">A resource group.</span></span>
- <span data-ttu-id="85a17-113">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="85a17-113">A virtual network.</span></span>
- <span data-ttu-id="85a17-114">Pula serwerów zaplecza zawierająca adresy IP serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="85a17-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="85a17-115">Ustawienia puli serwerów wewnętrznych.</span><span class="sxs-lookup"><span data-stu-id="85a17-115">Back-end server pool settings.</span></span> <span data-ttu-id="85a17-116">Każda pula ma takie ustawienia, jak port, protokół i koligacja oparta na plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="85a17-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="85a17-117">Adresy IP frontonu, które są adresami IP otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="85a17-118">Adres IP frontonu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="85a17-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="85a17-119">Porty frontonu, które są portami publicznymi otwartymi na bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="85a17-120">Ruch, który powoduje, że te porty są przekierowywane do serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="85a17-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="85a17-121">Reguła rozsyłania żądań wiążąca odbiornik i pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="85a17-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="85a17-122">Reguła określa pulę serwera zaplecza, do której ma być kierowany ruch, gdy trafi na określony detektor.</span><span class="sxs-lookup"><span data-stu-id="85a17-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="85a17-123">Odbiornik ma port frontonu, adres IP frontonu, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu SSL (Secure Sockets Layer) (Jeśli skonfigurowano odciążanie protokołu SSL).</span><span class="sxs-lookup"><span data-stu-id="85a17-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="85a17-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85a17-124">EXAMPLES</span></span>

### <span data-ttu-id="85a17-125">Przykład 1: Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="85a17-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
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

<span data-ttu-id="85a17-126">W poniższym przykładzie jest tworzona Brama Application Gateway po utworzeniu grupy zasobów i sieci wirtualnej oraz następujących danych:</span><span class="sxs-lookup"><span data-stu-id="85a17-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="85a17-127">Pula serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="85a17-127">A back-end server pool</span></span>
- <span data-ttu-id="85a17-128">Ustawienia puli serwerów wewnętrznych</span><span class="sxs-lookup"><span data-stu-id="85a17-128">Back-end server pool settings</span></span>
- <span data-ttu-id="85a17-129">Porty frontonu</span><span class="sxs-lookup"><span data-stu-id="85a17-129">Front-end ports</span></span>
- <span data-ttu-id="85a17-130">Adresy IP frontonu</span><span class="sxs-lookup"><span data-stu-id="85a17-130">Front-end IP addresses</span></span>
- <span data-ttu-id="85a17-131">Reguła rozsyłania żądań te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="85a17-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="85a17-132">Pierwsze polecenie powoduje utworzenie konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="85a17-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="85a17-133">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="85a17-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="85a17-134">Trzecie polecenie weryfikuje konfigurację podsieci, a czwarte polecenie weryfikuje, że sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="85a17-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="85a17-135">Poniższe polecenia tworzą bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="85a17-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="85a17-136">Pierwsze polecenie tworzy konfigurację adresu IP o nazwie GatewayIp01 dla podsieci utworzonej wcześniej.</span><span class="sxs-lookup"><span data-stu-id="85a17-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="85a17-137">Drugie polecenie tworzy pulę serwerów zaplecza o nazwie Pool01 z listą wewnętrznych adresów IP i przechowuje pulę w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="85a17-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="85a17-138">Trzecie polecenie tworzy ustawienia puli serwerów zaplecza i zapisuje ustawienia w zmiennej $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="85a17-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="85a17-139">Polecenie Dalej tworzy port frontonu na porcie 80, nazywa je FrontEndPort01 i przechowuje port w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="85a17-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="85a17-140">W piątym poleceniu jest tworzony publiczny adres IP przy użyciu polecenia New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="85a17-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="85a17-141">Szóste polecenie tworzy konfigurację adresu IP frontonu przy użyciu $PublicIp, nazywa ją FrontEndPortConfig01 i zapisuje ją w zmiennej $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85a17-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="85a17-142">Polecenie siódme powoduje utworzenie odbiornika przy użyciu $FrontEndPort utworzonych $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="85a17-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="85a17-143">Polecenie ósmy powoduje utworzenie reguły dla odbiornika.</span><span class="sxs-lookup"><span data-stu-id="85a17-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="85a17-144">Dziewiąte polecenie ustawia jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="85a17-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="85a17-145">Polecenie dziesiąte powoduje utworzenie bramy przy użyciu obiektów ustawionych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="85a17-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="85a17-146">Przykład 2: Tworzenie bramy aplikacji przy użyciu tożsamości UserAssigned</span><span class="sxs-lookup"><span data-stu-id="85a17-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
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

## <span data-ttu-id="85a17-147">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85a17-147">PARAMETERS</span></span>

### <span data-ttu-id="85a17-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85a17-148">-AsJob</span></span>
<span data-ttu-id="85a17-149">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="85a17-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85a17-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="85a17-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="85a17-151">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-151">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a17-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="85a17-153">Konfiguracja autoskalowania</span><span class="sxs-lookup"><span data-stu-id="85a17-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="85a17-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="85a17-154">-BackendAddressPools</span></span>
<span data-ttu-id="85a17-155">Określa listę pul adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-155">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="85a17-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="85a17-157">Określa listę wewnętrznych ustawień HTTP dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="85a17-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a17-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="85a17-159">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="85a17-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="85a17-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a17-160">-DefaultProfile</span></span>
<span data-ttu-id="85a17-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85a17-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85a17-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="85a17-162">-EnableFIPS</span></span>
<span data-ttu-id="85a17-163">Czy włączono opcję FIPS.</span><span class="sxs-lookup"><span data-stu-id="85a17-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="85a17-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="85a17-164">-EnableHttp2</span></span>
<span data-ttu-id="85a17-165">Czy HTTP2 jest włączony.</span><span class="sxs-lookup"><span data-stu-id="85a17-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="85a17-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="85a17-166">-FirewallPolicy</span></span>
<span data-ttu-id="85a17-167">Konfiguracja zapory</span><span class="sxs-lookup"><span data-stu-id="85a17-167">Firewall configuration</span></span>

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

### <span data-ttu-id="85a17-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="85a17-168">-FirewallPolicyId</span></span>
<span data-ttu-id="85a17-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="85a17-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="85a17-170">-Force</span><span class="sxs-lookup"><span data-stu-id="85a17-170">-Force</span></span>
<span data-ttu-id="85a17-171">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="85a17-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85a17-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="85a17-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="85a17-173">Czy skojarzenie siły firewallPolicy jest włączone.</span><span class="sxs-lookup"><span data-stu-id="85a17-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="85a17-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="85a17-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="85a17-175">Określa listę konfiguracji adresów IP frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="85a17-176">-FrontendPorts</span></span>
<span data-ttu-id="85a17-177">Określa listę portów frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-177">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="85a17-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="85a17-179">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-179">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="85a17-180">-HttpListeners</span></span>
<span data-ttu-id="85a17-181">Określa listę detektorów HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-182">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="85a17-182">-Identity</span></span>
<span data-ttu-id="85a17-183">Tożsamość bramy aplikacji, która ma być przypisana do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="85a17-184">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="85a17-184">-Location</span></span>
<span data-ttu-id="85a17-185">Określa region, w którym ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="85a17-186">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85a17-186">-Name</span></span>
<span data-ttu-id="85a17-187">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="85a17-188">-Badania</span><span class="sxs-lookup"><span data-stu-id="85a17-188">-Probes</span></span>
<span data-ttu-id="85a17-189">Określa sondy dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-189">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-190">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="85a17-190">-RedirectConfigurations</span></span>
<span data-ttu-id="85a17-191">Lista konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="85a17-191">The list of redirect configuration</span></span>

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

### <span data-ttu-id="85a17-192">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="85a17-192">-RequestRoutingRules</span></span>
<span data-ttu-id="85a17-193">Określa listę reguł rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-193">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-194">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a17-194">-ResourceGroupName</span></span>
<span data-ttu-id="85a17-195">Określa nazwę grupy zasobów, w której ma zostać utworzona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-195">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="85a17-196">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85a17-196">-RewriteRuleSet</span></span>
<span data-ttu-id="85a17-197">Lista RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85a17-197">The list of RewriteRuleSet</span></span>

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

### <span data-ttu-id="85a17-198">-SKU</span><span class="sxs-lookup"><span data-stu-id="85a17-198">-Sku</span></span>
<span data-ttu-id="85a17-199">Określa jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-199">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="85a17-200">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="85a17-200">-SslCertificates</span></span>
<span data-ttu-id="85a17-201">Określa listę certyfikatów SSL (Secure Sockets Layer) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-201">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-202">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="85a17-202">-SslPolicy</span></span>
<span data-ttu-id="85a17-203">Określa zasady protokołu SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-203">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-204">-Tag</span><span class="sxs-lookup"><span data-stu-id="85a17-204">-Tag</span></span>
<span data-ttu-id="85a17-205">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="85a17-205">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85a17-206">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="85a17-206">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85a17-207">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="85a17-207">-TrustedRootCertificate</span></span>
<span data-ttu-id="85a17-208">Lista zaufanych certyfikatów głównych</span><span class="sxs-lookup"><span data-stu-id="85a17-208">The list of trusted root certificates</span></span>

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

### <span data-ttu-id="85a17-209">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="85a17-209">-UrlPathMaps</span></span>
<span data-ttu-id="85a17-210">Określa mapowania ścieżek adresów URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-210">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="85a17-211">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="85a17-211">-UserAssignedIdentityId</span></span>
<span data-ttu-id="85a17-212">Identyfikator ResourceId przypisanego użytkownikowi tożsamości, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-212">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="85a17-213">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a17-213">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="85a17-214">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="85a17-214">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="85a17-215">Możesz użyć polecenia cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration, aby uzyskać WAF.</span><span class="sxs-lookup"><span data-stu-id="85a17-215">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="85a17-216">-Zone</span><span class="sxs-lookup"><span data-stu-id="85a17-216">-Zone</span></span>
<span data-ttu-id="85a17-217">Lista stref dostępności oznaczająca lokalizację, z której musi pochodzić Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="85a17-217">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="85a17-218">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85a17-218">-Confirm</span></span>
<span data-ttu-id="85a17-219">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a17-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a17-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a17-220">-WhatIf</span></span>
<span data-ttu-id="85a17-221">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a17-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a17-222">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85a17-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a17-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a17-223">CommonParameters</span></span>
<span data-ttu-id="85a17-224">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a17-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a17-225">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85a17-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a17-226">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85a17-226">INPUTS</span></span>

### <span data-ttu-id="85a17-227">System. String</span><span class="sxs-lookup"><span data-stu-id="85a17-227">System.String</span></span>

### <span data-ttu-id="85a17-228">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="85a17-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="85a17-229">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="85a17-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="85a17-230">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="85a17-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="85a17-231">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="85a17-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="85a17-232">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="85a17-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="85a17-233">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="85a17-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="85a17-234">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="85a17-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="85a17-235">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="85a17-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="85a17-236">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="85a17-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="85a17-237">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="85a17-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="85a17-238">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="85a17-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="85a17-239">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="85a17-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="85a17-240">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="85a17-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="85a17-241">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="85a17-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="85a17-242">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="85a17-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="85a17-243">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="85a17-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="85a17-244">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a17-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="85a17-245">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a17-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="85a17-246">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="85a17-246">System.Collections.Hashtable</span></span>

### <span data-ttu-id="85a17-247">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="85a17-247">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="85a17-248">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85a17-248">OUTPUTS</span></span>

### <span data-ttu-id="85a17-249">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85a17-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85a17-250">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85a17-250">NOTES</span></span>

## <span data-ttu-id="85a17-251">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85a17-251">RELATED LINKS</span></span>

[<span data-ttu-id="85a17-252">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85a17-252">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="85a17-253">Nowe — AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="85a17-253">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="85a17-254">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="85a17-254">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="85a17-255">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="85a17-255">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="85a17-256">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85a17-256">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="85a17-257">Nowe — AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a17-257">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85a17-258">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85a17-258">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="85a17-259">Nowe — AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="85a17-259">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="85a17-260">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85a17-260">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="85a17-261">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85a17-261">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
