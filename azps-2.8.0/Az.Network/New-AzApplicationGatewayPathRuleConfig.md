---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 6592f79291c069ade40b30277461f5e0e218b937
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407050"
---
# <span data-ttu-id="1b353-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="1b353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b353-102">SYNOPSIS</span></span>
<span data-ttu-id="1b353-103">Tworzy regułę ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b353-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="1b353-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b353-104">SYNTAX</span></span>

### <span data-ttu-id="1b353-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b353-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b353-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b353-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b353-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b353-107">DESCRIPTION</span></span>
<span data-ttu-id="1b353-108">Polecenie **cmdlet New-AzApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b353-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="1b353-109">Reguły utworzone za pomocą tego polecenia cmdlet można dodać do zbioru ustawień konfiguracji mapy ścieżki adresu URL, a następnie przypisać do bramy.</span><span class="sxs-lookup"><span data-stu-id="1b353-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="1b353-110">Ustawienia konfiguracji mapy ścieżki są używane do równoważenia obciążenia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b353-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="1b353-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b353-111">EXAMPLES</span></span>

### <span data-ttu-id="1b353-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b353-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="1b353-113">Te polecenia tworzą nową regułę ścieżki bramy aplikacji, a następnie przypisz ją do bramy aplikacji za pomocą polecenia cmdlet **Add-AzApplicationGatewayUrlPathMapConfig.**</span><span class="sxs-lookup"><span data-stu-id="1b353-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="1b353-114">W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="1b353-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="1b353-115">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="1b353-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="1b353-116">Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawień protokołu HTTP zaplecza. te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne do utworzenia obiektu reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="1b353-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="1b353-117">Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywany w zmiennej o nazwie $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1b353-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="1b353-118">Piąte polecenie korzysta z polecenia **Add-AzApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartej w tych ustawieniach do aplikacji ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="1b353-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="1b353-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b353-119">PARAMETERS</span></span>

### <span data-ttu-id="1b353-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b353-120">-BackendAddressPool</span></span>
<span data-ttu-id="1b353-121">Określa odwołanie do obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="1b353-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="1b353-122">To odwołanie do obiektu można utworzyć przy użyciu polecenia cmdlet New-AzApplicationGatewayBackendAddressPool składni podobnej do tej: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="1b353-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="1b353-123">Poprzednie polecenie dodaje dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.</span><span class="sxs-lookup"><span data-stu-id="1b353-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="1b353-124">Zwróć uwagę, że adres IP jest ujęty w cudzysłów i oddzielony przecinkami.</span><span class="sxs-lookup"><span data-stu-id="1b353-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="1b353-125">Następnie można użyć $AddressPool jako wartości parametru *parametru DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="1b353-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="1b353-126">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1b353-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="1b353-127">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="1b353-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="1b353-128">W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendAddressPoolId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1b353-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="1b353-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1b353-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="1b353-130">Określa identyfikator istniejącej puli adresów zaplecza, którą można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="1b353-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="1b353-131">Identyfikatory puli adresów można zwrócić za pomocą Get-AzApplicationGatewayBackendAddressPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b353-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="1b353-132">Po tym identyfikatorze można użyć parametru *DefaultBackendAddressPoolId* zamiast *parametru DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="1b353-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="1b353-133">Na przykład: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10//resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendAddressPools/ContosoAddressPools" Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1b353-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="1b353-134">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="1b353-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="1b353-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1b353-135">-BackendHttpSettings</span></span>
<span data-ttu-id="1b353-136">Określa odwołanie do obiektu do zbioru ustawień http zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="1b353-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="1b353-137">To odwołanie do obiektu można utworzyć przy użyciu polecenia cmdlet New-AzApplicationGatewayBackendHttpSettings o składni podobnej do tej: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Zmienna wynikowa. $HttpSettings następnie może być używana jako wartość parametru *parametru DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Ustawienia protokołu HTTP zaplecza konfigurują właściwości, takie jak port, protokół i chowalność oparta na plikach cookie puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1b353-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="1b353-138">W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendHttpSettingsId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1b353-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="1b353-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="1b353-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="1b353-140">Określa identyfikator istniejącej kolekcji ustawień protokołu HTTP zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="1b353-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="1b353-141">Identyfikatory ustawień protokołu HTTP można zwrócić za pomocą Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b353-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="1b353-142">Po wytyczaniu identyfikatora można użyć parametru *DefaultBackendHttpSettingsId* zamiast parametru *DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="1b353-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="1b353-143">Na przykład: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10//resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Ustawienia protokołu HTTP zaplecza konfigurują właściwości, takie jak port, protokół, i powiążność opartą na plikach cookie dla puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1b353-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="1b353-144">W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendHttpSettings* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1b353-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="1b353-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b353-145">-DefaultProfile</span></span>
<span data-ttu-id="1b353-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b353-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b353-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1b353-147">-Name</span></span>
<span data-ttu-id="1b353-148">Określa nazwę konfiguracji reguły ścieżki, którą tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b353-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1b353-149">— Ścieżki</span><span class="sxs-lookup"><span data-stu-id="1b353-149">-Paths</span></span>
<span data-ttu-id="1b353-150">Określa co najmniej jedną regułę ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b353-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="1b353-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b353-151">-RedirectConfiguration</span></span>
<span data-ttu-id="1b353-152">RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b353-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="1b353-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1b353-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="1b353-154">Identyfikator konfiguracji przekierowywania przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b353-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="1b353-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b353-155">-RewriteRuleSet</span></span>
<span data-ttu-id="1b353-156">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b353-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="1b353-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="1b353-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="1b353-158">Identyfikator bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b353-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="1b353-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b353-159">CommonParameters</span></span>
<span data-ttu-id="1b353-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b353-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b353-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b353-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b353-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b353-162">INPUTS</span></span>

### <span data-ttu-id="1b353-163">Brak</span><span class="sxs-lookup"><span data-stu-id="1b353-163">None</span></span>

## <span data-ttu-id="1b353-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b353-164">OUTPUTS</span></span>

### <span data-ttu-id="1b353-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="1b353-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="1b353-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b353-166">NOTES</span></span>

## <span data-ttu-id="1b353-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b353-167">RELATED LINKS</span></span>

[<span data-ttu-id="1b353-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1b353-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b353-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="1b353-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1b353-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b353-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="1b353-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="1b353-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1b353-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1b353-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1b353-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


