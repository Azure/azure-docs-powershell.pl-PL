---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 00e1cb4856afc00f13730dbee55de9499d603290
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961761"
---
# <span data-ttu-id="cebdd-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cebdd-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="cebdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cebdd-102">SYNOPSIS</span></span>
<span data-ttu-id="cebdd-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-103">Creates an application gateway.</span></span>

## <span data-ttu-id="cebdd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cebdd-104">SYNTAX</span></span>

### <span data-ttu-id="cebdd-105">IdentityByUserAssignedIdentityId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cebdd-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cebdd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cebdd-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cebdd-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cebdd-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cebdd-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="cebdd-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cebdd-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="cebdd-109">DESCRIPTION</span></span>
<span data-ttu-id="cebdd-110">Polecenie **cmdlet New-AzApplicationGateway** tworzy bramę aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="cebdd-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="cebdd-111">Brama aplikacji wymaga następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="cebdd-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="cebdd-112">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="cebdd-112">A resource group.</span></span>
- <span data-ttu-id="cebdd-113">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="cebdd-113">A virtual network.</span></span>
- <span data-ttu-id="cebdd-114">Pula serwerów typu back-end zawierająca adresy IP serwerów końcowych.</span><span class="sxs-lookup"><span data-stu-id="cebdd-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="cebdd-115">Ustawienia puli serwerów typu Back-end.</span><span class="sxs-lookup"><span data-stu-id="cebdd-115">Back-end server pool settings.</span></span> <span data-ttu-id="cebdd-116">Każda pula ma ustawienia, takie jak ffinity oparte na portach, protokołach i plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="cebdd-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="cebdd-117">Front-end IP addresses, czyli adresy IP otwarte w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="cebdd-118">Adres IP frontoronu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="cebdd-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="cebdd-119">Porty frontoronowe, czyli porty publiczne otwarte w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="cebdd-120">Ruch, który trafia do tych portów, jest przekierowywany na serwery back-end.</span><span class="sxs-lookup"><span data-stu-id="cebdd-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="cebdd-121">Reguła routingu żądania, która powiązywa słuchacza z pulą serwerów typu back-end.</span><span class="sxs-lookup"><span data-stu-id="cebdd-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="cebdd-122">Reguła określa pulę serwerów końcowych, do której ruch ma być przekierowywowany, gdy trafi w określonego słuchacza.</span><span class="sxs-lookup"><span data-stu-id="cebdd-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="cebdd-123">Słuchacz ma port frontoronowy, adres IP, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu Secure Sockets Layer (SSL) (przy konfigurowaniu ładowania SSL).</span><span class="sxs-lookup"><span data-stu-id="cebdd-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="cebdd-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cebdd-124">EXAMPLES</span></span>

### <span data-ttu-id="cebdd-125">Przykład 1. Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cebdd-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="cebdd-126">Poniższy przykład tworzy bramę aplikacji, tworząc najpierw grupę zasobów i sieć wirtualną, a także następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="cebdd-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="cebdd-127">Pula serwerów typu back-end</span><span class="sxs-lookup"><span data-stu-id="cebdd-127">A back-end server pool</span></span>
- <span data-ttu-id="cebdd-128">Ustawienia puli serwerów typu Back-end</span><span class="sxs-lookup"><span data-stu-id="cebdd-128">Back-end server pool settings</span></span>
- <span data-ttu-id="cebdd-129">Porty frontoronowe</span><span class="sxs-lookup"><span data-stu-id="cebdd-129">Front-end ports</span></span>
- <span data-ttu-id="cebdd-130">Front-end IP addresses</span><span class="sxs-lookup"><span data-stu-id="cebdd-130">Front-end IP addresses</span></span>
- <span data-ttu-id="cebdd-131">Reguła routingu żądania Te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="cebdd-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="cebdd-132">Pierwsze polecenie tworzy konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="cebdd-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="cebdd-133">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="cebdd-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="cebdd-134">Trzecie polecenie sprawdza konfigurację podsieci, a czwarte polecenie sprawdza, czy sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="cebdd-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="cebdd-135">Poniższe polecenia tworzą bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="cebdd-136">Pierwsze polecenie tworzy konfigurację protokołu IP o nazwie GatewayIp01 dla utworzonej wcześniej podsieci.</span><span class="sxs-lookup"><span data-stu-id="cebdd-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="cebdd-137">Drugie polecenie tworzy pulę serwerów typu Back-end o nazwie Pool01 z listą adresów IP oraz przechowuje pulę w $Pool danych.</span><span class="sxs-lookup"><span data-stu-id="cebdd-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="cebdd-138">Trzecie polecenie tworzy ustawienia dla puli serwerów typu back-end i przechowuje ustawienia w $PoolSetting danych.</span><span class="sxs-lookup"><span data-stu-id="cebdd-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="cebdd-139">Polecenie Forth tworzy port frontonu na porcie 80, nadaje nazwę FrontEndPort01 i przechowuje port w $FrontEndPort zmienną.</span><span class="sxs-lookup"><span data-stu-id="cebdd-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="cebdd-140">Piąte polecenie tworzy publiczny adres IP przy użyciu adresu New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="cebdd-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="cebdd-141">Szóste polecenie tworzy konfigurację frontonu ip przy użyciu protokołu $PublicIp, nadaje nazwę FrontEndPortConfig01 i zapisuje ją w $FrontEndIpConfig danych.</span><span class="sxs-lookup"><span data-stu-id="cebdd-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="cebdd-142">Siódme polecenie tworzy słuchacza przy użyciu poprzednio utworzonego $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="cebdd-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="cebdd-143">Ósme polecenie tworzy regułę dla słuchacza.</span><span class="sxs-lookup"><span data-stu-id="cebdd-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="cebdd-144">Trzynastowe polecenie ustawia zestaw SKU.</span><span class="sxs-lookup"><span data-stu-id="cebdd-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="cebdd-145">Dziesiąte polecenie tworzy bramę przy użyciu obiektów ustawionych w poprzednich poleceniach.</span><span class="sxs-lookup"><span data-stu-id="cebdd-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="cebdd-146">Przykład 2. Tworzenie bramy aplikacji przy użyciu tożsamości z przypisaną tożsamością użytkownika</span><span class="sxs-lookup"><span data-stu-id="cebdd-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="cebdd-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cebdd-147">PARAMETERS</span></span>

### <span data-ttu-id="cebdd-148">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cebdd-148">-AsJob</span></span>
<span data-ttu-id="cebdd-149">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cebdd-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cebdd-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="cebdd-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="cebdd-151">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-151">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="cebdd-153">Konfiguracja skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="cebdd-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="cebdd-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="cebdd-154">-BackendAddressPools</span></span>
<span data-ttu-id="cebdd-155">Określa listę pul adresu końcowego dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-155">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="cebdd-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="cebdd-157">Określa listę ustawień protokołu HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-158">- CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="cebdd-159">Błąd klienta bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cebdd-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="cebdd-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebdd-160">-DefaultProfile</span></span>
<span data-ttu-id="cebdd-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cebdd-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cebdd-162">—EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="cebdd-162">-EnableFIPS</span></span>
<span data-ttu-id="cebdd-163">Czy jest włączona funkcja FIPS.</span><span class="sxs-lookup"><span data-stu-id="cebdd-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="cebdd-164">—EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="cebdd-164">-EnableHttp2</span></span>
<span data-ttu-id="cebdd-165">Czy jest włączony protokół HTTP2.</span><span class="sxs-lookup"><span data-stu-id="cebdd-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="cebdd-166">- FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cebdd-166">-FirewallPolicy</span></span>
<span data-ttu-id="cebdd-167">Konfiguracja zapory</span><span class="sxs-lookup"><span data-stu-id="cebdd-167">Firewall configuration</span></span>

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

### <span data-ttu-id="cebdd-168">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cebdd-168">-FirewallPolicyId</span></span>
<span data-ttu-id="cebdd-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cebdd-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="cebdd-170">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cebdd-170">-Force</span></span>
<span data-ttu-id="cebdd-171">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cebdd-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cebdd-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="cebdd-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="cebdd-173">Czy jest włączone skojarzenie Force firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="cebdd-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="cebdd-174">- FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="cebdd-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="cebdd-175">Określa listę frontoronowych konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="cebdd-176">-FrontendPorts</span></span>
<span data-ttu-id="cebdd-177">Określa listę portów frontonie dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-177">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-178">- GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="cebdd-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="cebdd-179">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-179">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-180">- HttpListeners</span><span class="sxs-lookup"><span data-stu-id="cebdd-180">-HttpListeners</span></span>
<span data-ttu-id="cebdd-181">Określa listę słuchaczy HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-182">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="cebdd-182">-Identity</span></span>
<span data-ttu-id="cebdd-183">Tożsamość bramy aplikacji, która ma zostać przypisana do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="cebdd-184">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cebdd-184">-Location</span></span>
<span data-ttu-id="cebdd-185">Określa region, w którym ma być tworzyć bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-186">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cebdd-186">-Name</span></span>
<span data-ttu-id="cebdd-187">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="cebdd-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="cebdd-189">Lista konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="cebdd-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebdd-190">- Namysłowy</span><span class="sxs-lookup"><span data-stu-id="cebdd-190">-Probes</span></span>
<span data-ttu-id="cebdd-191">Określa sieci bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-191">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="cebdd-192">-RedirectConfigurations</span></span>
<span data-ttu-id="cebdd-193">Lista konfiguracji przekierowywania</span><span class="sxs-lookup"><span data-stu-id="cebdd-193">The list of redirect configuration</span></span>

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

### <span data-ttu-id="cebdd-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="cebdd-194">-RequestRoutingRules</span></span>
<span data-ttu-id="cebdd-195">Określa listę reguł routingu żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-195">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cebdd-196">-ResourceGroupName</span></span>
<span data-ttu-id="cebdd-197">Określa nazwę grupy zasobów, w której ma być tworzyć bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cebdd-198">-RewriteRuleSet</span></span>
<span data-ttu-id="cebdd-199">Lista zestawu rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cebdd-199">The list of RewriteRuleSet</span></span>

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

### <span data-ttu-id="cebdd-200">- SKU</span><span class="sxs-lookup"><span data-stu-id="cebdd-200">-Sku</span></span>
<span data-ttu-id="cebdd-201">Określa jednostkę przechowywania zapasów (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="cebdd-202">-SslCertificates</span></span>
<span data-ttu-id="cebdd-203">Określa listę certyfikatów Secure Sockets Layer (SSL) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-204">- SslPolicy</span><span class="sxs-lookup"><span data-stu-id="cebdd-204">-SslPolicy</span></span>
<span data-ttu-id="cebdd-205">Określa zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-205">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="cebdd-206">-SslProfiles</span></span>
<span data-ttu-id="cebdd-207">Lista profilów SSL</span><span class="sxs-lookup"><span data-stu-id="cebdd-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebdd-208">— Tag</span><span class="sxs-lookup"><span data-stu-id="cebdd-208">-Tag</span></span>
<span data-ttu-id="cebdd-209">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="cebdd-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cebdd-210">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="cebdd-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cebdd-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="cebdd-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="cebdd-212">Lista łańcuchów certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="cebdd-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebdd-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cebdd-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="cebdd-214">Lista zaufanych certyfikatów głównych</span><span class="sxs-lookup"><span data-stu-id="cebdd-214">The list of trusted root certificates</span></span>

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

### <span data-ttu-id="cebdd-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="cebdd-215">-UrlPathMaps</span></span>
<span data-ttu-id="cebdd-216">Określa mapy ścieżek adresów URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-216">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="cebdd-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="cebdd-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="cebdd-218">Identyfikator Zasobu przypisanej tożsamości użytkownika, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="cebdd-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="cebdd-220">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="cebdd-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="cebdd-221">Aby uzyskać dostęp do Get-AzApplicationGatewayWebApplicationFirewallConfiguration WAF, możesz użyć tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cebdd-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="cebdd-222">— Strefa</span><span class="sxs-lookup"><span data-stu-id="cebdd-222">-Zone</span></span>
<span data-ttu-id="cebdd-223">Lista stref dostępności oznaczających, skąd musi pochodzić brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cebdd-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="cebdd-224">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cebdd-224">-Confirm</span></span>
<span data-ttu-id="cebdd-225">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cebdd-225">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cebdd-226">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cebdd-226">-WhatIf</span></span>
<span data-ttu-id="cebdd-227">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cebdd-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cebdd-228">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cebdd-228">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cebdd-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebdd-229">CommonParameters</span></span>
<span data-ttu-id="cebdd-230">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebdd-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebdd-231">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cebdd-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebdd-232">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cebdd-232">INPUTS</span></span>

### <span data-ttu-id="cebdd-233">System.String</span><span class="sxs-lookup"><span data-stu-id="cebdd-233">System.String</span></span>

### <span data-ttu-id="cebdd-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cebdd-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="cebdd-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="cebdd-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="cebdd-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="cebdd-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="cebdd-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="cebdd-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="cebdd-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="cebdd-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="cebdd-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="cebdd-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="cebdd-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="cebdd-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="cebdd-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="cebdd-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="cebdd-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="cebdd-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="cebdd-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="cebdd-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="cebdd-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="cebdd-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cebdd-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cebdd-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cebdd-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="cebdd-254">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cebdd-254">OUTPUTS</span></span>

### <span data-ttu-id="cebdd-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cebdd-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cebdd-256">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cebdd-256">NOTES</span></span>

## <span data-ttu-id="cebdd-257">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cebdd-257">RELATED LINKS</span></span>

[<span data-ttu-id="cebdd-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cebdd-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="cebdd-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cebdd-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="cebdd-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cebdd-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cebdd-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cebdd-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cebdd-262">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cebdd-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cebdd-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebdd-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cebdd-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cebdd-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="cebdd-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cebdd-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="cebdd-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cebdd-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="cebdd-267">New-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cebdd-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
