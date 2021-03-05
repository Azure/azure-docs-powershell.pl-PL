---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997242"
---
# <span data-ttu-id="4f095-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f095-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4f095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f095-102">SYNOPSIS</span></span>
<span data-ttu-id="4f095-103">Tworzy słuchacza HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f095-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="4f095-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f095-104">SYNTAX</span></span>

### <span data-ttu-id="4f095-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f095-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f095-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4f095-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f095-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f095-107">DESCRIPTION</span></span>
<span data-ttu-id="4f095-108">Polecenie **cmdlet New-AzApplicationGatewayHttpListener** tworzy słuchacza HTTP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4f095-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="4f095-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f095-109">EXAMPLES</span></span>

### <span data-ttu-id="4f095-110">Przykład 1. Tworzenie słuchacza HTTP</span><span class="sxs-lookup"><span data-stu-id="4f095-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="4f095-111">To polecenie tworzy słuchacza HTTP o nazwie Słuchacz01 i przechowuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="4f095-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="4f095-112">Przykład 2. Tworzenie słuchacza HTTP przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="4f095-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="4f095-113">To polecenie tworzy słuchacza HTTP, który korzysta z ładowania SSL, i dostarcza certyfikat SSL w $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="4f095-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="4f095-114">Polecenie przechowuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="4f095-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="4f095-115">Przykład 3. Tworzenie słuchacza protokołu HTTP przy użyciu zasad zapory</span><span class="sxs-lookup"><span data-stu-id="4f095-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="4f095-116">To polecenie tworzy słuchacza HTTP o nazwie Listener01, FirewallPolicy jako $firewallPolicy i przechowuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="4f095-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="4f095-117">Przykład 4. Dodawanie słuchacza protokołu HTTPS przy użyciu protokołu SSL i nazw hostów</span><span class="sxs-lookup"><span data-stu-id="4f095-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="4f095-118">To polecenie tworzy słuchacza HTTP, który korzysta z ładowania SSL i dostarcza certyfikat SSL w zmiennej $SSLCert 01 wraz z dwoma nazwami hosta.</span><span class="sxs-lookup"><span data-stu-id="4f095-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="4f095-119">Polecenie przechowuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="4f095-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="4f095-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f095-120">PARAMETERS</span></span>

### <span data-ttu-id="4f095-121">- CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f095-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="4f095-122">Błąd klienta bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4f095-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="4f095-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f095-123">-DefaultProfile</span></span>
<span data-ttu-id="4f095-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f095-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f095-125">- FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f095-125">-FirewallPolicy</span></span>
<span data-ttu-id="4f095-126">Określa odwołanie do obiektu do zasad zapory najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="4f095-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="4f095-127">Odwołanie do obiektu można utworzyć za pomocą New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f095-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="4f095-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Do zasad zapory utworzonych przy użyciu powyższego polecenia commandlet można odtworzyć na poziomie reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="4f095-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="4f095-129">powyższe polecenie tworzyło domyślne ustawienia zasad i reguły zarządzane.</span><span class="sxs-lookup"><span data-stu-id="4f095-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="4f095-130">Zamiast wartości domyślnych użytkownicy mogą określać ustawienia zasad, wartości ManagedRules, używając New-AzApplicationGatewayFirewallPolicySettings lub New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="4f095-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="4f095-131">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="4f095-131">-FirewallPolicyId</span></span>
<span data-ttu-id="4f095-132">Określa identyfikator istniejącego zasobu zapory aplikacji sieci Web najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="4f095-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="4f095-133">Identyfikatory zasad zapory można zwrócić za pomocą Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f095-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="4f095-134">Po tym identyfikatorze można użyć parametru *FirewallPolicyId* zamiast *parametru FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="4f095-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="4f095-135">Na przykład: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="4f095-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="4f095-136">- FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f095-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4f095-137">Określa obiekt konfiguracji frontoronu IP dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4f095-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="4f095-139">Określa identyfikator konfiguracji frontoronu ip dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="4f095-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f095-140">-FrontendPort</span></span>
<span data-ttu-id="4f095-141">Określa port frontoronowy dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="4f095-142">-FrontendPortId</span></span>
<span data-ttu-id="4f095-143">Określa identyfikator obiektu portu frontoronu dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="4f095-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="4f095-144">-HostName</span></span>
<span data-ttu-id="4f095-145">Określa nazwę hosta słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f095-145">Specifies the host name of the application gateway HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="4f095-146">-HostNames</span></span>
<span data-ttu-id="4f095-147">Nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="4f095-147">Host names</span></span>

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

### <span data-ttu-id="4f095-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4f095-148">-Name</span></span>
<span data-ttu-id="4f095-149">Określa nazwę słuchacza HTTP, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f095-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4f095-150">— Protokół</span><span class="sxs-lookup"><span data-stu-id="4f095-150">-Protocol</span></span>
<span data-ttu-id="4f095-151">Określa protokół używany przez słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="4f095-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4f095-153">-SslCertificate</span></span>
<span data-ttu-id="4f095-154">Określa obiekt certyfikatu SSL dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="4f095-155">-SslCertificateId</span></span>
<span data-ttu-id="4f095-156">Określa identyfikator certyfikatu SSL dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f095-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="4f095-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="4f095-157">-SslProfile</span></span>
<span data-ttu-id="4f095-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="4f095-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f095-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="4f095-159">-SslProfileId</span></span>
<span data-ttu-id="4f095-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="4f095-160">SslProfileId</span></span>

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

### <span data-ttu-id="4f095-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f095-161">CommonParameters</span></span>
<span data-ttu-id="4f095-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f095-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f095-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f095-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f095-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f095-164">INPUTS</span></span>

### <span data-ttu-id="4f095-165">Brak</span><span class="sxs-lookup"><span data-stu-id="4f095-165">None</span></span>

## <span data-ttu-id="4f095-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f095-166">OUTPUTS</span></span>

### <span data-ttu-id="4f095-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f095-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4f095-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f095-168">NOTES</span></span>

## <span data-ttu-id="4f095-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f095-169">RELATED LINKS</span></span>

[<span data-ttu-id="4f095-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f095-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f095-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f095-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f095-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f095-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f095-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f095-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


