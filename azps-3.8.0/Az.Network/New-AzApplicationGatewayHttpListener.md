---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053765"
---
# <span data-ttu-id="d470d-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d470d-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d470d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d470d-102">SYNOPSIS</span></span>
<span data-ttu-id="d470d-103">Tworzy odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d470d-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="d470d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d470d-104">SYNTAX</span></span>

### <span data-ttu-id="d470d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d470d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d470d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d470d-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d470d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d470d-107">DESCRIPTION</span></span>
<span data-ttu-id="d470d-108">Polecenie cmdlet **New-AzApplicationGatewayHttpListener** umożliwia utworzenie odbiornika HTTP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d470d-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="d470d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d470d-109">EXAMPLES</span></span>

### <span data-ttu-id="d470d-110">Przykład 1: Tworzenie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="d470d-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="d470d-111">To polecenie tworzy odbiornik HTTP o nazwie Listener01 i zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="d470d-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="d470d-112">Przykład 2: Tworzenie odbiornika HTTP przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="d470d-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="d470d-113">To polecenie tworzy odbiornik HTTP używający odciążania SSL i dostarcza certyfikat SSL w zmiennej $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="d470d-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="d470d-114">Polecenie zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="d470d-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="d470d-115">Przykład 3: Tworzenie odbiornika HTTP z zasadami zapory</span><span class="sxs-lookup"><span data-stu-id="d470d-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="d470d-116">To polecenie tworzy odbiornik HTTP o nazwie Listener01, FirewallPolicy jako $firewallPolicy i zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="d470d-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="d470d-117">Przykład 4: Dodawanie odbiornika HTTPS przy użyciu protokołu SSL i nazw hostów</span><span class="sxs-lookup"><span data-stu-id="d470d-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="d470d-118">To polecenie tworzy odbiornik HTTP używający odciążania SSL i dostarcza certyfikat SSL w zmiennej $SSLCert 01 wraz z dwiema nazwami hostów.</span><span class="sxs-lookup"><span data-stu-id="d470d-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="d470d-119">Polecenie zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="d470d-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="d470d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d470d-120">PARAMETERS</span></span>

### <span data-ttu-id="d470d-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="d470d-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="d470d-122">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d470d-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="d470d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d470d-123">-DefaultProfile</span></span>
<span data-ttu-id="d470d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d470d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d470d-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d470d-125">-FirewallPolicy</span></span>
<span data-ttu-id="d470d-126">Określa odwołanie obiektu do zasad zapory najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="d470d-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="d470d-127">Odwołanie do obiektu można utworzyć przy użyciu New-AzApplicationGatewayWebApplicationFirewallPolicy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d470d-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="d470d-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-resourceName "rgName" zasada zapory utworzona przy użyciu powyższego unifiedgroup może być określona na poziomie reguły ścieżki.</span><span class="sxs-lookup"><span data-stu-id="d470d-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="d470d-129">Powyższe polecenie utworzy domyślne ustawienia zasad i reguły zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d470d-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="d470d-130">Zamiast wartości domyślnych użytkownicy mogą określać PolicySettings, ManagedRules, odpowiednio, za pomocą New-AzApplicationGatewayFirewallPolicySettings i New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="d470d-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="d470d-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d470d-131">-FirewallPolicyId</span></span>
<span data-ttu-id="d470d-132">Określa identyfikator istniejącego zasobu zapory aplikacji sieci Web najwyższego poziomu.</span><span class="sxs-lookup"><span data-stu-id="d470d-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="d470d-133">Identyfikatory zasad zapory można zwracać przy użyciu polecenia cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="d470d-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="d470d-134">Gdy mamy identyfikator, możesz użyć parametru *FirewallPolicyId* zamiast parametru *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="d470d-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="d470d-135">Na przykład:-FirewallPolicyId/subscriptions/<abonament-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="d470d-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="d470d-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d470d-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d470d-137">Określa obiekt konfiguracji IP frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d470d-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d470d-139">Określa identyfikator zewnętrznej konfiguracji IP dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d470d-140">-FrontendPort</span></span>
<span data-ttu-id="d470d-141">Określa port frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d470d-142">-FrontendPortId</span></span>
<span data-ttu-id="d470d-143">Określa identyfikator obiektu typu front-end dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="d470d-144">-HostName</span></span>
<span data-ttu-id="d470d-145">Określa nazwę hosta odbiornika HTTP bramy Application.</span><span class="sxs-lookup"><span data-stu-id="d470d-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-146">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="d470d-146">-HostNames</span></span>
<span data-ttu-id="d470d-147">Nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="d470d-147">Host names</span></span>

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

### <span data-ttu-id="d470d-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d470d-148">-Name</span></span>
<span data-ttu-id="d470d-149">Określa nazwę odbiornika HTTP, który tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d470d-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d470d-150">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d470d-150">-Protocol</span></span>
<span data-ttu-id="d470d-151">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="d470d-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d470d-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="d470d-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d470d-153">-SslCertificate</span></span>
<span data-ttu-id="d470d-154">Określa obiekt certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d470d-155">-SslCertificateId</span></span>
<span data-ttu-id="d470d-156">Określa identyfikator certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="d470d-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="d470d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d470d-157">CommonParameters</span></span>
<span data-ttu-id="d470d-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d470d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d470d-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d470d-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d470d-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d470d-160">INPUTS</span></span>

### <span data-ttu-id="d470d-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d470d-161">None</span></span>

## <span data-ttu-id="d470d-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d470d-162">OUTPUTS</span></span>

### <span data-ttu-id="d470d-163">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d470d-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d470d-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d470d-164">NOTES</span></span>

## <span data-ttu-id="d470d-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d470d-165">RELATED LINKS</span></span>

[<span data-ttu-id="d470d-166">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d470d-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d470d-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d470d-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d470d-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d470d-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d470d-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d470d-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


