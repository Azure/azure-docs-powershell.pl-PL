---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234144"
---
# <span data-ttu-id="d42b2-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="d42b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d42b2-102">SYNOPSIS</span></span>
<span data-ttu-id="d42b2-103">Tworzy regułę ścieżki bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d42b2-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="d42b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d42b2-104">SYNTAX</span></span>

### <span data-ttu-id="d42b2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d42b2-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d42b2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d42b2-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d42b2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d42b2-107">DESCRIPTION</span></span>
<span data-ttu-id="d42b2-108">Polecenie cmdlet **New-AzApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d42b2-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="d42b2-109">Reguły utworzone przez to polecenie cmdlet można dodać do kolekcji ustawień konfiguracji mapowania ścieżki URL, a następnie przypisywać je do bramy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="d42b2-110">Ustawienia konfiguracji mapy ścieżki są używane w równoważeniu obciążenia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d42b2-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="d42b2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d42b2-111">EXAMPLES</span></span>

### <span data-ttu-id="d42b2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d42b2-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="d42b2-113">Te polecenia umożliwiają utworzenie nowej reguły ścieżki bramy Application Gateway, a następnie użycie polecenia cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** w celu przypisania tej reguły do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d42b2-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="d42b2-114">W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="d42b2-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="d42b2-115">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="d42b2-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="d42b2-116">Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawienia HTTP zaplecza; te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne w celu utworzenia obiektu reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="d42b2-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="d42b2-117">Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywany w zmiennej o nazwie $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d42b2-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="d42b2-118">W piątym poleceniu użyto polecenia **Add-AzApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartych w tych ustawieniach do ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="d42b2-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="d42b2-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d42b2-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="d42b2-120">To polecenie tworzy regułę ścieżki o nazwie "Base", ścieżce jako "/Base", BackendAddressPool jako $AddressPool, BackendHttpSettings jako $HttpSettings i FirewallPolicy jako $firewallPolicy. NGS oraz Nowa reguła ścieżki znajdująca się w tych ustawieniach do ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="d42b2-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="d42b2-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d42b2-121">PARAMETERS</span></span>

### <span data-ttu-id="d42b2-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d42b2-122">-BackendAddressPool</span></span>
<span data-ttu-id="d42b2-123">Określa odwołanie obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="d42b2-124">To odwołanie do obiektu można utworzyć przy użyciu New-AzApplicationGatewayBackendAddressPool polecenia cmdlet i składni podobnej do następującej: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="d42b2-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="d42b2-125">W powyższym poleceniu są dodawane dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.</span><span class="sxs-lookup"><span data-stu-id="d42b2-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="d42b2-126">Należy zauważyć, że adres IP jest ujęty w cudzysłów i oddzielony średnikami.</span><span class="sxs-lookup"><span data-stu-id="d42b2-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="d42b2-127">Zmienna wynikowa $AddressPool może być używana jako wartość parametru parametru *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="d42b2-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="d42b2-128">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d42b2-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="d42b2-129">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="d42b2-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="d42b2-130">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendAddressPoolId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d42b2-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d42b2-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="d42b2-132">Określa identyfikator istniejącej puli adresów zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="d42b2-133">Identyfikatory puli adresów można zwracać przy użyciu polecenia cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="d42b2-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="d42b2-134">Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendAddressPoolId* zamiast parametru *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="d42b2-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="d42b2-135">Na przykład:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d42b2-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="d42b2-136">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="d42b2-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="d42b2-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d42b2-137">-BackendHttpSettings</span></span>
<span data-ttu-id="d42b2-138">Określa odwołanie obiektu do kolekcji ustawień protokołu HTTP zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="d42b2-139">To odwołanie do obiektu można utworzyć przy użyciu New-AzApplicationGatewayBackendHttpSettings polecenia cmdlet i składni podobnej do następującej: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-port 80-protokół "http"-CookieBasedAffinity "Disabled zmienna, $HttpSettings może być używana jako wartość parametru *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings ustawień protokołu HTTP zaplecza Konfigurowanie właściwości, takich jak port, protokół i koligacja oparta na plikach cookie dla puli wewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="d42b2-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="d42b2-140">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettingsId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d42b2-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d42b2-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="d42b2-142">Określa identyfikator istniejącej kolekcji ustawień protokołu HTTP zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="d42b2-143">Identyfikatory ustawień HTTP można zwrócić przy użyciu Get-AzApplicationGatewayBackendHttpSettings polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d42b2-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="d42b2-144">Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendHttpSettingsId* zamiast parametru *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="d42b2-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="d42b2-145">Na przykład:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Ustawienia protokołu HTTP zaplecza Konfigurowanie właściwości, takich jak port, protokół i koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d42b2-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="d42b2-146">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettings* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d42b2-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="d42b2-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d42b2-147">-FirewallPolicy</span></span>
<span data-ttu-id="d42b2-148">Określa odwołanie obiektu do zasad zapory najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="d42b2-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="d42b2-149">Odwołanie do obiektu można utworzyć przy użyciu New-AzApplicationGatewayWebApplicationFirewallPolicy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d42b2-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="d42b2-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-resourceName "rgName" zasada zapory utworzona przy użyciu powyższego unifiedgroup może być określona na poziomie reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="d42b2-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="d42b2-151">Powyższe polecenie utworzy domyślne ustawienia zasad i reguły zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d42b2-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="d42b2-152">Zamiast wartości domyślnych użytkownicy mogą określać PolicySettings, ManagedRules, odpowiednio, za pomocą New-AzApplicationGatewayFirewallPolicySettings i New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="d42b2-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d42b2-153">-FirewallPolicyId</span></span>
<span data-ttu-id="d42b2-154">Określa identyfikator istniejącego zasobu zapory aplikacji sieci Web najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="d42b2-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="d42b2-155">Identyfikatory zasad zapory można zwracać przy użyciu polecenia cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="d42b2-156">Gdy mamy identyfikator, możesz użyć parametru *FirewallPolicyId* zamiast parametru *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="d42b2-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="d42b2-157">Na przykład:-FirewallPolicyId "/subscriptions/<abonament-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="d42b2-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42b2-158">-DefaultProfile</span></span>
<span data-ttu-id="d42b2-159">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d42b2-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d42b2-160">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d42b2-160">-Name</span></span>
<span data-ttu-id="d42b2-161">Określa nazwę konfiguracji reguły ścieżki, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="d42b2-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-162">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="d42b2-162">-Paths</span></span>
<span data-ttu-id="d42b2-163">Określa co najmniej jeden Regulamin ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d42b2-163">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d42b2-164">-RedirectConfiguration</span></span>
<span data-ttu-id="d42b2-165">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d42b2-165">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d42b2-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="d42b2-167">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d42b2-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d42b2-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d42b2-168">-RewriteRuleSet</span></span>
<span data-ttu-id="d42b2-169">Aplikacja Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d42b2-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42b2-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d42b2-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="d42b2-171">Identyfikator bramy Application RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d42b2-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="d42b2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42b2-172">CommonParameters</span></span>
<span data-ttu-id="d42b2-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d42b2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42b2-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42b2-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42b2-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d42b2-175">INPUTS</span></span>

### <span data-ttu-id="d42b2-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d42b2-176">None</span></span>

## <span data-ttu-id="d42b2-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d42b2-177">OUTPUTS</span></span>

### <span data-ttu-id="d42b2-178">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="d42b2-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="d42b2-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d42b2-179">NOTES</span></span>

## <span data-ttu-id="d42b2-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d42b2-180">RELATED LINKS</span></span>

[<span data-ttu-id="d42b2-181">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d42b2-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d42b2-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d42b2-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d42b2-184">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d42b2-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d42b2-185">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d42b2-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="d42b2-186">Nowe — AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="d42b2-187">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d42b2-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d42b2-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d42b2-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


