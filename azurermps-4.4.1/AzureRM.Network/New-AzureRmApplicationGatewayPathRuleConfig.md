---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: bcb712e7bfe0cd619d63378cad89402828eb6d36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551823"
---
# <span data-ttu-id="3378d-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="3378d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3378d-102">SYNOPSIS</span></span>
<span data-ttu-id="3378d-103">Tworzy regułę ścieżki bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3378d-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3378d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3378d-104">SYNTAX</span></span>

### <span data-ttu-id="3378d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3378d-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3378d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3378d-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3378d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3378d-107">DESCRIPTION</span></span>
<span data-ttu-id="3378d-108">Polecenie cmdlet **New-AzureRmApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3378d-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="3378d-109">Reguły utworzone przez to polecenie cmdlet można dodać do kolekcji ustawień konfiguracji mapowania ścieżki URL, a następnie przypisywać je do bramy.</span><span class="sxs-lookup"><span data-stu-id="3378d-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="3378d-110">Ustawienia konfiguracji mapy ścieżki są używane w równoważeniu obciążenia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3378d-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="3378d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3378d-111">EXAMPLES</span></span>

### <span data-ttu-id="3378d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3378d-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="3378d-113">Te polecenia umożliwiają utworzenie nowej reguły ścieżki bramy Application Gateway, a następnie użycie polecenia cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** w celu przypisania tej reguły do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3378d-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="3378d-114">W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="3378d-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="3378d-115">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="3378d-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="3378d-116">Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawienia HTTP zaplecza; te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne w celu utworzenia obiektu reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="3378d-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="3378d-117">Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywany w zmiennej o nazwie $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="3378d-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="3378d-118">W piątym poleceniu użyto polecenia **Add-AzureRmApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartych w tych ustawieniach do ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="3378d-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="3378d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3378d-119">PARAMETERS</span></span>

### <span data-ttu-id="3378d-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3378d-120">-BackendAddressPool</span></span>
<span data-ttu-id="3378d-121">Określa odwołanie obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="3378d-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="3378d-122">To odwołanie do obiektu można utworzyć przy użyciu New-AzureRmApplicationGatewayBackendAddressPool polecenia cmdlet i składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="3378d-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="3378d-123">W powyższym poleceniu są dodawane dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.</span><span class="sxs-lookup"><span data-stu-id="3378d-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="3378d-124">Należy zauważyć, że adres IP jest ujęty w cudzysłów i oddzielony średnikami.</span><span class="sxs-lookup"><span data-stu-id="3378d-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="3378d-125">Zmienna wynikowa $AddressPool może być używana jako wartość parametru parametru *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="3378d-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="3378d-126">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3378d-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="3378d-127">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="3378d-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="3378d-128">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendAddressPoolId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3378d-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="3378d-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3378d-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="3378d-130">Określa identyfikator istniejącej puli adresów zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="3378d-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="3378d-131">Identyfikatory puli adresów można zwracać przy użyciu polecenia cmdlet Get-AzureRmApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="3378d-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="3378d-132">Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendAddressPoolId* zamiast parametru *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="3378d-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="3378d-133">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3378d-133">For instance:</span></span>

<span data-ttu-id="3378d-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="3378d-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="3378d-135">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3378d-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="3378d-136">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="3378d-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="3378d-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3378d-137">-BackendHttpSettings</span></span>
<span data-ttu-id="3378d-138">Określa odwołanie obiektu do kolekcji ustawień protokołu HTTP zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="3378d-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="3378d-139">To odwołanie do obiektu można utworzyć przy użyciu New-AzureRmApplicationGatewayBackendHttpSettings polecenia cmdlet i składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="3378d-139">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="3378d-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-port 80-protokół "http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="3378d-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="3378d-141">Zmienna wynikowa $HttpSettings może być używana jako wartość parametru parametru *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="3378d-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="3378d-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="3378d-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="3378d-143">Ustawienia HTTP zaplecza konfigurują właściwości, takie jak port, protokół oraz koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3378d-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="3378d-144">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettingsId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3378d-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="3378d-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="3378d-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="3378d-146">Określa identyfikator istniejącej kolekcji ustawień protokołu HTTP zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="3378d-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="3378d-147">Identyfikatory ustawień HTTP można zwrócić przy użyciu Get-AzureRmApplicationGatewayBackendHttpSettings polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3378d-147">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="3378d-148">Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendHttpSettingsId* zamiast parametru *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="3378d-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="3378d-149">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3378d-149">For instance:</span></span>

<span data-ttu-id="3378d-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="3378d-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="3378d-151">Ustawienia HTTP zaplecza konfigurują właściwości, takie jak port, protokół oraz koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3378d-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="3378d-152">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettings* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3378d-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="3378d-153">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3378d-153">-Name</span></span>
<span data-ttu-id="3378d-154">Określa nazwę konfiguracji reguły ścieżki, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="3378d-154">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3378d-155">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="3378d-155">-Paths</span></span>
<span data-ttu-id="3378d-156">Określa co najmniej jeden Regulamin ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3378d-156">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3378d-157">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3378d-157">-RedirectConfiguration</span></span>
<span data-ttu-id="3378d-158">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3378d-158">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="3378d-159">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3378d-159">-RedirectConfigurationId</span></span>
<span data-ttu-id="3378d-160">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3378d-160">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="3378d-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3378d-161">-DefaultProfile</span></span>
<span data-ttu-id="3378d-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3378d-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3378d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3378d-163">CommonParameters</span></span>
<span data-ttu-id="3378d-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3378d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3378d-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3378d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3378d-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3378d-166">INPUTS</span></span>

###  
<span data-ttu-id="3378d-167">Funkcja **New-AzureRmApplicationGatewayPathRuleConfig** nie akceptuje danych wejściowych rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3378d-167">**New-AzureRmApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="3378d-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3378d-168">OUTPUTS</span></span>

###  
<span data-ttu-id="3378d-169">**Nowe — AzureRmApplicationGatewayPathRuleConfig** tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="3378d-169">**New-AzureRmApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="3378d-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3378d-170">NOTES</span></span>

## <span data-ttu-id="3378d-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3378d-171">RELATED LINKS</span></span>

[<span data-ttu-id="3378d-172">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3378d-173">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3378d-173">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="3378d-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3378d-175">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3378d-175">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3378d-176">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3378d-176">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="3378d-177">Nowe — AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-177">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="3378d-178">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3378d-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3378d-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3378d-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


