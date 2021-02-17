---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: d78daedb0d8e5b8767e596316d7da8d252b59805
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405180"
---
# <span data-ttu-id="ded3d-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ded3d-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="ded3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ded3d-102">SYNOPSIS</span></span>
<span data-ttu-id="ded3d-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-103">Creates an application gateway.</span></span>

## <span data-ttu-id="ded3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ded3d-104">SYNTAX</span></span>

### <span data-ttu-id="ded3d-105">IdentityByUserAssignedIdentityId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ded3d-105">IdentityByUserAssignedIdentityId (Default)</span></span>
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

### <span data-ttu-id="ded3d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ded3d-106">SetByResourceId</span></span>
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

### <span data-ttu-id="ded3d-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ded3d-107">SetByResource</span></span>
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

### <span data-ttu-id="ded3d-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="ded3d-108">IdentityByIdentityObject</span></span>
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

## <span data-ttu-id="ded3d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ded3d-109">DESCRIPTION</span></span>
<span data-ttu-id="ded3d-110">Polecenie **cmdlet New-AzApplicationGateway** tworzy bramę aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="ded3d-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="ded3d-111">Brama aplikacji wymaga następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="ded3d-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="ded3d-112">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="ded3d-112">A resource group.</span></span>
- <span data-ttu-id="ded3d-113">Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="ded3d-113">A virtual network.</span></span>
- <span data-ttu-id="ded3d-114">Pula serwerów typu back-end zawierająca adresy IP serwerów back-end.</span><span class="sxs-lookup"><span data-stu-id="ded3d-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="ded3d-115">Ustawienia puli serwerów typu Back-end.</span><span class="sxs-lookup"><span data-stu-id="ded3d-115">Back-end server pool settings.</span></span> <span data-ttu-id="ded3d-116">Każda pula ma ustawienia, takie jak ffinity oparte na portach, protokołach i plikach cookie, które są stosowane do wszystkich serwerów w puli.</span><span class="sxs-lookup"><span data-stu-id="ded3d-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="ded3d-117">Front-end IP addresses, czyli adresy IP otwarte w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="ded3d-118">Adres IP frontoronu może być publicznym adresem IP lub wewnętrznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="ded3d-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="ded3d-119">Porty frontoronowe, czyli porty publiczne otwarte w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="ded3d-120">Ruch, który trafia do tych portów, jest przekierowywany na serwery back-end.</span><span class="sxs-lookup"><span data-stu-id="ded3d-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="ded3d-121">Reguła routingu żądania, która powiązywa słuchacza z pulą serwerów typu back-end.</span><span class="sxs-lookup"><span data-stu-id="ded3d-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="ded3d-122">Reguła określa pulę serwerów końcowych, do której ruch ma być przekierowywowany, gdy trafi w określonego słuchacza.</span><span class="sxs-lookup"><span data-stu-id="ded3d-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="ded3d-123">Słuchacz ma port frontoronowy, adres IP, protokół (HTTP lub HTTPS) i nazwę certyfikatu protokołu Secure Sockets Layer (SSL) (przy konfigurowaniu ładowania SSL).</span><span class="sxs-lookup"><span data-stu-id="ded3d-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="ded3d-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ded3d-124">EXAMPLES</span></span>

### <span data-ttu-id="ded3d-125">Przykład 1. Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ded3d-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="ded3d-126">Poniższy przykład tworzy bramę aplikacji, tworząc najpierw grupę zasobów i sieć wirtualną, a także następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="ded3d-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="ded3d-127">Pula serwerów typu back-end</span><span class="sxs-lookup"><span data-stu-id="ded3d-127">A back-end server pool</span></span>
- <span data-ttu-id="ded3d-128">Ustawienia puli serwerów typu Back-end</span><span class="sxs-lookup"><span data-stu-id="ded3d-128">Back-end server pool settings</span></span>
- <span data-ttu-id="ded3d-129">Porty frontoronowe</span><span class="sxs-lookup"><span data-stu-id="ded3d-129">Front-end ports</span></span>
- <span data-ttu-id="ded3d-130">Front-end IP addresses</span><span class="sxs-lookup"><span data-stu-id="ded3d-130">Front-end IP addresses</span></span>
- <span data-ttu-id="ded3d-131">Reguła routingu żądania Te cztery polecenia tworzą sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ded3d-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="ded3d-132">Pierwsze polecenie tworzy konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="ded3d-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="ded3d-133">Drugie polecenie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ded3d-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="ded3d-134">Trzecie polecenie sprawdza konfigurację podsieci, a czwarte polecenie pozwala sprawdzić, czy sieć wirtualna została utworzona pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="ded3d-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="ded3d-135">Poniższe polecenia tworzą bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="ded3d-136">Pierwsze polecenie tworzy konfigurację protokołu IP o nazwie GatewayIp01 dla utworzonej wcześniej podsieci.</span><span class="sxs-lookup"><span data-stu-id="ded3d-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="ded3d-137">Drugie polecenie tworzy pulę serwerów typu Back-end o nazwie Pool01 z listą adresów IP oraz przechowuje pulę w zmiennej $Pool danych.</span><span class="sxs-lookup"><span data-stu-id="ded3d-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="ded3d-138">Trzecie polecenie tworzy ustawienia dla puli serwerów typu back-end i zapisuje ustawienia w $PoolSetting serwera.</span><span class="sxs-lookup"><span data-stu-id="ded3d-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="ded3d-139">Polecenie Forth tworzy port frontonu na porcie 80, nadaje nazwę FrontEndPort01 i przechowuje port w $FrontEndPort zmienną.</span><span class="sxs-lookup"><span data-stu-id="ded3d-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="ded3d-140">Piąte polecenie tworzy publiczny adres IP przy użyciu adresu New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="ded3d-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="ded3d-141">Szóste polecenie tworzy konfigurację frontonu ip przy użyciu protokołu $PublicIp, nadaje nazwę FrontEndPortConfig01 i zapisuje ją w $FrontEndIpConfig danych.</span><span class="sxs-lookup"><span data-stu-id="ded3d-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="ded3d-142">Siódme polecenie tworzy słuchacza przy użyciu poprzednio utworzonego $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="ded3d-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="ded3d-143">Ósme polecenie tworzy regułę dla słuchacza.</span><span class="sxs-lookup"><span data-stu-id="ded3d-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="ded3d-144">Trzynastowe polecenie ustawia zestaw SKU.</span><span class="sxs-lookup"><span data-stu-id="ded3d-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="ded3d-145">Dziesiąte polecenie tworzy bramę przy użyciu obiektów ustawionych w poprzednich poleceniach.</span><span class="sxs-lookup"><span data-stu-id="ded3d-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="ded3d-146">Przykład 2. Tworzenie bramy aplikacji przy użyciu tożsamości z przypisaną tożsamością użytkownika</span><span class="sxs-lookup"><span data-stu-id="ded3d-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="ded3d-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ded3d-147">PARAMETERS</span></span>

### <span data-ttu-id="ded3d-148">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ded3d-148">-AsJob</span></span>
<span data-ttu-id="ded3d-149">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ded3d-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ded3d-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="ded3d-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="ded3d-151">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-151">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ded3d-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="ded3d-153">Konfiguracja skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="ded3d-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="ded3d-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="ded3d-154">-BackendAddressPools</span></span>
<span data-ttu-id="ded3d-155">Określa listę pul adresu końcowego dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-155">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="ded3d-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="ded3d-157">Określa listę ustawień protokołu HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-158">- CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ded3d-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="ded3d-159">Błąd klienta bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ded3d-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="ded3d-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded3d-160">-DefaultProfile</span></span>
<span data-ttu-id="ded3d-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ded3d-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ded3d-162">—EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="ded3d-162">-EnableFIPS</span></span>
<span data-ttu-id="ded3d-163">Czy jest włączona funkcja FIPS.</span><span class="sxs-lookup"><span data-stu-id="ded3d-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="ded3d-164">—EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="ded3d-164">-EnableHttp2</span></span>
<span data-ttu-id="ded3d-165">Czy jest włączony protokół HTTP2.</span><span class="sxs-lookup"><span data-stu-id="ded3d-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="ded3d-166">- FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ded3d-166">-FirewallPolicy</span></span>
<span data-ttu-id="ded3d-167">Konfiguracja zapory</span><span class="sxs-lookup"><span data-stu-id="ded3d-167">Firewall configuration</span></span>

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

### <span data-ttu-id="ded3d-168">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ded3d-168">-FirewallPolicyId</span></span>
<span data-ttu-id="ded3d-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ded3d-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="ded3d-170">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ded3d-170">-Force</span></span>
<span data-ttu-id="ded3d-171">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ded3d-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ded3d-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="ded3d-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="ded3d-173">Czy jest włączone skojarzenie Force firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="ded3d-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="ded3d-174">- FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="ded3d-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="ded3d-175">Określa listę frontoronowych konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="ded3d-176">-FrontendPorts</span></span>
<span data-ttu-id="ded3d-177">Określa listę portów frontonie dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-177">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-178">- GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="ded3d-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="ded3d-179">Określa listę konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-179">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-180">- HttpListeners</span><span class="sxs-lookup"><span data-stu-id="ded3d-180">-HttpListeners</span></span>
<span data-ttu-id="ded3d-181">Określa listę słuchaczy HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-182">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="ded3d-182">-Identity</span></span>
<span data-ttu-id="ded3d-183">Tożsamość bramy aplikacji, która ma zostać przypisana do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="ded3d-184">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ded3d-184">-Location</span></span>
<span data-ttu-id="ded3d-185">Określa region, w którym ma być tworzyć bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-186">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ded3d-186">-Name</span></span>
<span data-ttu-id="ded3d-187">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="ded3d-188">- Nasyć</span><span class="sxs-lookup"><span data-stu-id="ded3d-188">-Probes</span></span>
<span data-ttu-id="ded3d-189">Określa sieci bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-189">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-190">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="ded3d-190">-RedirectConfigurations</span></span>
<span data-ttu-id="ded3d-191">Lista konfiguracji przekierowywania</span><span class="sxs-lookup"><span data-stu-id="ded3d-191">The list of redirect configuration</span></span>

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

### <span data-ttu-id="ded3d-192">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="ded3d-192">-RequestRoutingRules</span></span>
<span data-ttu-id="ded3d-193">Określa listę reguł routingu żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-193">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-194">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded3d-194">-ResourceGroupName</span></span>
<span data-ttu-id="ded3d-195">Określa nazwę grupy zasobów, w której ma być tworzyć bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-195">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-196">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ded3d-196">-RewriteRuleSet</span></span>
<span data-ttu-id="ded3d-197">Lista zestawu rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ded3d-197">The list of RewriteRuleSet</span></span>

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

### <span data-ttu-id="ded3d-198">- SKU</span><span class="sxs-lookup"><span data-stu-id="ded3d-198">-Sku</span></span>
<span data-ttu-id="ded3d-199">Określa jednostkę przechowywania zapasów (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-199">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-200">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="ded3d-200">-SslCertificates</span></span>
<span data-ttu-id="ded3d-201">Określa listę certyfikatów Secure Sockets Layer (SSL) dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-201">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-202">- SslPolicy</span><span class="sxs-lookup"><span data-stu-id="ded3d-202">-SslPolicy</span></span>
<span data-ttu-id="ded3d-203">Określa zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-203">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-204">— Tag</span><span class="sxs-lookup"><span data-stu-id="ded3d-204">-Tag</span></span>
<span data-ttu-id="ded3d-205">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="ded3d-205">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ded3d-206">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ded3d-206">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ded3d-207">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ded3d-207">-TrustedRootCertificate</span></span>
<span data-ttu-id="ded3d-208">Lista zaufanych certyfikatów głównych</span><span class="sxs-lookup"><span data-stu-id="ded3d-208">The list of trusted root certificates</span></span>

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

### <span data-ttu-id="ded3d-209">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="ded3d-209">-UrlPathMaps</span></span>
<span data-ttu-id="ded3d-210">Określa mapy ścieżek adresu URL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-210">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="ded3d-211">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="ded3d-211">-UserAssignedIdentityId</span></span>
<span data-ttu-id="ded3d-212">Identyfikator Zasobu przypisanej tożsamości użytkownika, który ma zostać przypisany do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-212">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="ded3d-213">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ded3d-213">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="ded3d-214">Określa konfigurację zapory aplikacji sieci Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="ded3d-214">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="ded3d-215">Aby uzyskać dostęp do Get-AzApplicationGatewayWebApplicationFirewallConfiguration WAF, możesz użyć tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded3d-215">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="ded3d-216">— Strefa</span><span class="sxs-lookup"><span data-stu-id="ded3d-216">-Zone</span></span>
<span data-ttu-id="ded3d-217">Lista stref dostępności oznaczających, skąd musi pochodzić brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ded3d-217">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="ded3d-218">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ded3d-218">-Confirm</span></span>
<span data-ttu-id="ded3d-219">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ded3d-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded3d-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded3d-220">-WhatIf</span></span>
<span data-ttu-id="ded3d-221">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded3d-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ded3d-222">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ded3d-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded3d-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded3d-223">CommonParameters</span></span>
<span data-ttu-id="ded3d-224">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded3d-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded3d-225">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ded3d-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded3d-226">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ded3d-226">INPUTS</span></span>

### <span data-ttu-id="ded3d-227">System.String</span><span class="sxs-lookup"><span data-stu-id="ded3d-227">System.String</span></span>

### <span data-ttu-id="ded3d-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ded3d-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="ded3d-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ded3d-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="ded3d-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="ded3d-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="ded3d-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="ded3d-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="ded3d-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="ded3d-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="ded3d-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="ded3d-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="ded3d-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="ded3d-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="ded3d-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="ded3d-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="ded3d-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="ded3d-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ded3d-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="ded3d-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ded3d-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="ded3d-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ded3d-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="ded3d-246">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ded3d-246">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ded3d-247">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ded3d-247">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="ded3d-248">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ded3d-248">OUTPUTS</span></span>

### <span data-ttu-id="ded3d-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ded3d-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ded3d-250">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ded3d-250">NOTES</span></span>

## <span data-ttu-id="ded3d-251">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ded3d-251">RELATED LINKS</span></span>

[<span data-ttu-id="ded3d-252">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ded3d-252">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="ded3d-253">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ded3d-253">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ded3d-254">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ded3d-254">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ded3d-255">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ded3d-255">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ded3d-256">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ded3d-256">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ded3d-257">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ded3d-257">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ded3d-258">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ded3d-258">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="ded3d-259">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ded3d-259">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="ded3d-260">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ded3d-260">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
