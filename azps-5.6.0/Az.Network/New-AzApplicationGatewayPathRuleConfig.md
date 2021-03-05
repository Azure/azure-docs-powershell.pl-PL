---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b343ecbabd66f32be30f4aff1b0a44c7ddf186d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985853"
---
# <span data-ttu-id="11e68-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="11e68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e68-102">SYNOPSIS</span></span>
<span data-ttu-id="11e68-103">Tworzy regułę ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11e68-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="11e68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11e68-104">SYNTAX</span></span>

### <span data-ttu-id="11e68-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11e68-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e68-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="11e68-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e68-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="11e68-107">DESCRIPTION</span></span>
<span data-ttu-id="11e68-108">Polecenie **cmdlet New-AzApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11e68-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="11e68-109">Reguły utworzone za pomocą tego polecenia cmdlet można dodać do zbioru ustawień konfiguracji mapy ścieżki adresu URL, a następnie przypisać do bramy.</span><span class="sxs-lookup"><span data-stu-id="11e68-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="11e68-110">Ustawienia konfiguracji mapy ścieżki są używane do równoważenia obciążenia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11e68-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="11e68-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11e68-111">EXAMPLES</span></span>

### <span data-ttu-id="11e68-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11e68-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="11e68-113">Te polecenia tworzą nową regułę ścieżki bramy aplikacji, a następnie przypisz ją do bramy aplikacji za pomocą polecenia cmdlet **Add-AzApplicationGatewayUrlPathMapConfig.**</span><span class="sxs-lookup"><span data-stu-id="11e68-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="11e68-114">W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="11e68-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="11e68-115">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="11e68-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="11e68-116">Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawień protokołu HTTP zaplecza. te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne do utworzenia obiektu reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="11e68-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="11e68-117">Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywane w zmiennej o nazwie $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="11e68-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="11e68-118">Piąte polecenie korzysta z polecenia **Add-AzApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartej w tych ustawieniach do aplikacji ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="11e68-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="11e68-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11e68-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="11e68-120">To polecenie tworzy regułę ścieżki z nazwą "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings i FirewallPolicy jako $firewallPolicy.ngs oraz regułą nowej ścieżki zawartej w tych ustawieniach do witryny ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="11e68-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="11e68-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11e68-121">PARAMETERS</span></span>

### <span data-ttu-id="11e68-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11e68-122">-BackendAddressPool</span></span>
<span data-ttu-id="11e68-123">Określa odwołanie do obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="11e68-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="11e68-124">To odwołanie do obiektu można utworzyć przy użyciu polecenia cmdlet New-AzApplicationGatewayBackendAddressPool składni podobnej do tej: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="11e68-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="11e68-125">Poprzednie polecenie dodaje dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.</span><span class="sxs-lookup"><span data-stu-id="11e68-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="11e68-126">Zwróć uwagę, że adres IP jest ujęty w cudzysłów i oddzielony przecinkami.</span><span class="sxs-lookup"><span data-stu-id="11e68-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="11e68-127">Zmienna wynikowa ($AddressPool) może być następnie używana jako wartość parametru *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="11e68-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="11e68-128">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="11e68-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="11e68-129">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="11e68-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="11e68-130">W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendAddressPoolId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="11e68-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="11e68-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="11e68-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="11e68-132">Określa identyfikator istniejącej puli adresów zaplecza, którą można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="11e68-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="11e68-133">Identyfikatory puli adresów można zwrócić za pomocą Get-AzApplicationGatewayBackendAddressPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e68-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="11e68-134">Po tym identyfikatorze można użyć parametru *DefaultBackendAddressPoolId zamiast* *parametru DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="11e68-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="11e68-135">Na przykład: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10//resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendAddressPools/ContosoAddressPools" Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="11e68-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="11e68-136">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="11e68-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="11e68-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="11e68-137">-BackendHttpSettings</span></span>
<span data-ttu-id="11e68-138">Określa odwołanie do obiektu do zbioru ustawień http zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="11e68-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="11e68-139">To odwołanie do obiektu można utworzyć przy użyciu polecenia cmdlet New-AzApplicationGatewayBackendHttpSettings o składni podobnej do tej: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Zmienna wynikowa. $HttpSettings następnie może być używana jako wartość parametru *parametru DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Ustawienia protokołu HTTP zaplecza konfigurują właściwości, takie jak port, protokół i chowalność oparta na plikach cookie puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="11e68-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="11e68-140">W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendHttpSettingsId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="11e68-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="11e68-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="11e68-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="11e68-142">Określa identyfikator istniejącej kolekcji ustawień protokołu HTTP zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="11e68-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="11e68-143">Identyfikatory ustawień protokołu HTTP można zwrócić za pomocą Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e68-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="11e68-144">Po wytyczaniu identyfikatora można użyć parametru *DefaultBackendHttpSettingsId* zamiast *parametru DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="11e68-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="11e68-145">Na przykład: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10//resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Ustawienia protokołu HTTP zaplecza konfigurują właściwości, takie jak port, protokół, i powiążność opartą na plikach cookie dla puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="11e68-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="11e68-146">W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendHttpSettings* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="11e68-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="11e68-147">- FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="11e68-147">-FirewallPolicy</span></span>
<span data-ttu-id="11e68-148">Określa odwołanie do obiektu do zasad zapory najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="11e68-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="11e68-149">Odwołanie do obiektu można utworzyć za pomocą New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e68-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="11e68-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Do zasad zapory utworzonych przy użyciu powyższego polecenia commandlet można odtworzyć na poziomie reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="11e68-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="11e68-151">powyższe polecenie tworzyło domyślne ustawienia zasad i reguły zarządzane.</span><span class="sxs-lookup"><span data-stu-id="11e68-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="11e68-152">Zamiast wartości domyślnych użytkownicy mogą określać ustawienia zasad, wartości ManagedRules, używając New-AzApplicationGatewayFirewallPolicySettings lub New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="11e68-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e68-153">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="11e68-153">-FirewallPolicyId</span></span>
<span data-ttu-id="11e68-154">Określa identyfikator istniejącego zasobu zapory aplikacji sieci Web najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="11e68-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="11e68-155">Identyfikatory zasad zapory można zwrócić za pomocą Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e68-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="11e68-156">Po tym identyfikatorze można użyć parametru *FirewallPolicyId* zamiast *parametru FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="11e68-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="11e68-157">Na przykład: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="11e68-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e68-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e68-158">-DefaultProfile</span></span>
<span data-ttu-id="11e68-159">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11e68-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e68-160">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11e68-160">-Name</span></span>
<span data-ttu-id="11e68-161">Określa nazwę konfiguracji reguły ścieżki, którą tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e68-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11e68-162">— Ścieżki</span><span class="sxs-lookup"><span data-stu-id="11e68-162">-Paths</span></span>
<span data-ttu-id="11e68-163">Określa co najmniej jedną regułę ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11e68-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="11e68-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11e68-164">-RedirectConfiguration</span></span>
<span data-ttu-id="11e68-165">RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="11e68-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="11e68-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="11e68-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="11e68-167">Identyfikator konfiguracji przekierowywania przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="11e68-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="11e68-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11e68-168">-RewriteRuleSet</span></span>
<span data-ttu-id="11e68-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11e68-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="11e68-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="11e68-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="11e68-171">Identyfikator bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11e68-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="11e68-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e68-172">CommonParameters</span></span>
<span data-ttu-id="11e68-173">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e68-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e68-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e68-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e68-175">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11e68-175">INPUTS</span></span>

### <span data-ttu-id="11e68-176">Brak</span><span class="sxs-lookup"><span data-stu-id="11e68-176">None</span></span>

## <span data-ttu-id="11e68-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11e68-177">OUTPUTS</span></span>

### <span data-ttu-id="11e68-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="11e68-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="11e68-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11e68-179">NOTES</span></span>

## <span data-ttu-id="11e68-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11e68-180">RELATED LINKS</span></span>

[<span data-ttu-id="11e68-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11e68-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11e68-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="11e68-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11e68-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11e68-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="11e68-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="11e68-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="11e68-186">New-azApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="11e68-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11e68-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11e68-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11e68-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


