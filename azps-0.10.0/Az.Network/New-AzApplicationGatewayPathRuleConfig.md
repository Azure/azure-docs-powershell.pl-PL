---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890562"
---
# <span data-ttu-id="f3f7b-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="f3f7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f7b-103">Tworzy regułę ścieżki bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="f3f7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3f7b-104">SYNTAX</span></span>

### <span data-ttu-id="f3f7b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3f7b-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3f7b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f3f7b-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f3f7b-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f7b-108">Polecenie cmdlet **New-AzApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="f3f7b-109">Reguły utworzone przez to polecenie cmdlet można dodać do kolekcji ustawień konfiguracji mapowania ścieżki URL, a następnie przypisywać je do bramy.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="f3f7b-110">Ustawienia konfiguracji mapy ścieżki są używane w równoważeniu obciążenia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="f3f7b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3f7b-111">EXAMPLES</span></span>

### <span data-ttu-id="f3f7b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3f7b-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="f3f7b-113">Te polecenia umożliwiają utworzenie nowej reguły ścieżki bramy Application Gateway, a następnie użycie polecenia cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** w celu przypisania tej reguły do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="f3f7b-114">W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="f3f7b-115">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="f3f7b-116">Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawienia HTTP zaplecza; te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne w celu utworzenia obiektu reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="f3f7b-117">Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywany w zmiennej o nazwie $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="f3f7b-118">W piątym poleceniu użyto polecenia **Add-AzApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartych w tych ustawieniach do ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="f3f7b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3f7b-119">PARAMETERS</span></span>

### <span data-ttu-id="f3f7b-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f3f7b-120">-BackendAddressPool</span></span>
<span data-ttu-id="f3f7b-121">Określa odwołanie obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="f3f7b-122">To odwołanie do obiektu można utworzyć przy użyciu New-AzApplicationGatewayBackendAddressPool polecenia cmdlet i składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="f3f7b-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="f3f7b-123">W powyższym poleceniu są dodawane dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="f3f7b-124">Należy zauważyć, że adres IP jest ujęty w cudzysłów i oddzielony średnikami.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="f3f7b-125">Zmienna wynikowa $AddressPool może być używana jako wartość parametru parametru *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="f3f7b-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="f3f7b-126">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="f3f7b-127">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="f3f7b-128">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendAddressPoolId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f3f7b-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="f3f7b-130">Określa identyfikator istniejącej puli adresów zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="f3f7b-131">Identyfikatory puli adresów można zwracać przy użyciu polecenia cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="f3f7b-132">Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendAddressPoolId* zamiast parametru *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="f3f7b-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="f3f7b-133">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f3f7b-133">For instance:</span></span>

<span data-ttu-id="f3f7b-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="f3f7b-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="f3f7b-135">Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="f3f7b-136">Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f3f7b-137">-BackendHttpSettings</span></span>
<span data-ttu-id="f3f7b-138">Określa odwołanie obiektu do kolekcji ustawień protokołu HTTP zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="f3f7b-139">To odwołanie do obiektu można utworzyć przy użyciu New-AzApplicationGatewayBackendHttpSetting polecenia cmdlet i składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="f3f7b-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="f3f7b-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "ContosoHttpSetings"-port 80-protokół "http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="f3f7b-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="f3f7b-141">Zmienna wynikowa $HttpSettings może być używana jako wartość parametru parametru *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="f3f7b-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="f3f7b-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="f3f7b-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="f3f7b-143">Ustawienia HTTP zaplecza konfigurują właściwości, takie jak port, protokół oraz koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="f3f7b-144">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettingsId* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f3f7b-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f3f7b-146">Określa identyfikator istniejącej kolekcji ustawień protokołu HTTP zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="f3f7b-147">Identyfikatory ustawień HTTP można zwrócić przy użyciu Get-AzApplicationGatewayBackendHttpSetting polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="f3f7b-148">Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendHttpSettingsId* zamiast parametru *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="f3f7b-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="f3f7b-149">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f3f7b-149">For instance:</span></span>

<span data-ttu-id="f3f7b-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="f3f7b-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="f3f7b-151">Ustawienia HTTP zaplecza konfigurują właściwości, takie jak port, protokół oraz koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="f3f7b-152">W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettings* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f7b-153">-DefaultProfile</span></span>
<span data-ttu-id="f3f7b-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f7b-155">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3f7b-155">-Name</span></span>
<span data-ttu-id="f3f7b-156">Określa nazwę konfiguracji reguły ścieżki, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-157">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="f3f7b-157">-Paths</span></span>
<span data-ttu-id="f3f7b-158">Określa co najmniej jeden Regulamin ścieżki bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="f3f7b-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3f7b-159">-RedirectConfiguration</span></span>
<span data-ttu-id="f3f7b-160">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3f7b-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f3f7b-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="f3f7b-162">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3f7b-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f7b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f7b-163">CommonParameters</span></span>
<span data-ttu-id="f3f7b-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f7b-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f7b-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f7b-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3f7b-166">INPUTS</span></span>

###  
<span data-ttu-id="f3f7b-167">Funkcja **New-AzApplicationGatewayPathRuleConfig** nie akceptuje danych wejściowych rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f3f7b-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="f3f7b-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3f7b-168">OUTPUTS</span></span>

###  
<span data-ttu-id="f3f7b-169">**Nowe — AzApplicationGatewayPathRuleConfig** tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="f3f7b-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="f3f7b-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3f7b-170">NOTES</span></span>

## <span data-ttu-id="f3f7b-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3f7b-171">RELATED LINKS</span></span>

[<span data-ttu-id="f3f7b-172">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f3f7b-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3f7b-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f3f7b-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f3f7b-175">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f3f7b-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f3f7b-176">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f3f7b-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f3f7b-177">Nowe — AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="f3f7b-178">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f3f7b-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f3f7b-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f3f7b-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


