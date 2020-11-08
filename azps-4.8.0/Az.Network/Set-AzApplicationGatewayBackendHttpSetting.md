---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220489"
---
# <span data-ttu-id="5e69c-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5e69c-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="5e69c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e69c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e69c-103">Aktualizuje ustawienia HTTP zaplecza bramy Application.</span><span class="sxs-lookup"><span data-stu-id="5e69c-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="5e69c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e69c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e69c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e69c-105">DESCRIPTION</span></span>
<span data-ttu-id="5e69c-106">Polecenie cmdlet Set-AzApplicationGatewayBackendHttpSetting aktualizuje ustawienia protokołu HTTP (Hypertext Transfer Protocol) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e69c-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="5e69c-107">Ustawienia HTTP zaplecza są stosowane do wszystkich serwerów wewnętrznych w puli.</span><span class="sxs-lookup"><span data-stu-id="5e69c-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="5e69c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e69c-108">EXAMPLES</span></span>

### <span data-ttu-id="5e69c-109">Przykład 1: aktualizowanie wewnętrznych ustawień HTTP dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5e69c-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="5e69c-110">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5e69c-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5e69c-111">Drugie polecenie aktualizuje ustawienia HTTP bramy Application Gateway w zmiennej $AppGw, aby używać portów 88, protokołu HTTP i włączania koligacji opartych na plikach cookie.</span><span class="sxs-lookup"><span data-stu-id="5e69c-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="5e69c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e69c-112">PARAMETERS</span></span>

### <span data-ttu-id="5e69c-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="5e69c-113">-AffinityCookieName</span></span>
<span data-ttu-id="5e69c-114">Nazwa pliku cookie do użycia w pliku cookie koligacji</span><span class="sxs-lookup"><span data-stu-id="5e69c-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="5e69c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e69c-115">-ApplicationGateway</span></span>
<span data-ttu-id="5e69c-116">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="5e69c-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="5e69c-118">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5e69c-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5e69c-119">-ConnectionDraining</span></span>
<span data-ttu-id="5e69c-120">Połączenie opróżniania zasobu Ustawienia http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-120">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="5e69c-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="5e69c-122">Określa, czy koligacja oparta na plikach cookie powinna być włączona lub wyłączona dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="5e69c-123">Dopuszczalne wartości tego parametru są następujące: wyłączone lub włączone.</span><span class="sxs-lookup"><span data-stu-id="5e69c-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e69c-124">-DefaultProfile</span></span>
<span data-ttu-id="5e69c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e69c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e69c-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="5e69c-126">-HostName</span></span>
<span data-ttu-id="5e69c-127">Ustawia nagłówek hosta, który ma być wysyłany na serwery wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5e69c-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="5e69c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e69c-128">-Name</span></span>
<span data-ttu-id="5e69c-129">Określa nazwę obiektu zaplecza "Ustawienia HTTP".</span><span class="sxs-lookup"><span data-stu-id="5e69c-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="5e69c-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5e69c-130">-Path</span></span>
<span data-ttu-id="5e69c-131">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="5e69c-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="5e69c-132">Jeśli dla tego parametru nie podano żadnej wartości, ścieżka nie zostanie naprawiona.</span><span class="sxs-lookup"><span data-stu-id="5e69c-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="5e69c-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="5e69c-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="5e69c-134">Flaga Jeśli nagłówek hosta powinien być wybrany z nazwy hosta serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5e69c-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="5e69c-135">-Port</span><span class="sxs-lookup"><span data-stu-id="5e69c-135">-Port</span></span>
<span data-ttu-id="5e69c-136">Określa port, który ma być używany dla każdego serwera w puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-136">Specifies the port to use for each server in the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-137">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="5e69c-137">-Probe</span></span>
<span data-ttu-id="5e69c-138">Określa sondę do skojarzenia z ustawieniami HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="5e69c-139">-ProbeId</span></span>
<span data-ttu-id="5e69c-140">Określa identyfikator sondy, która ma być skojarzona z ustawieniami protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="5e69c-141">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="5e69c-141">-Protocol</span></span>
<span data-ttu-id="5e69c-142">Określa protokół, który ma być używany do komunikacji między bramą aplikacji a serwerami zaplecza.</span><span class="sxs-lookup"><span data-stu-id="5e69c-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="5e69c-143">Dopuszczalne wartości tego parametru to: http i https.</span><span class="sxs-lookup"><span data-stu-id="5e69c-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="5e69c-144">W tym parametrze jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="5e69c-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="5e69c-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="5e69c-145">-RequestTimeout</span></span>
<span data-ttu-id="5e69c-146">Określa wartość limitu czasu żądania.</span><span class="sxs-lookup"><span data-stu-id="5e69c-146">Specifies a request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5e69c-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="5e69c-148">Zaufane certyfikaty główne bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5e69c-148">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e69c-149">CommonParameters</span></span>
<span data-ttu-id="5e69c-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e69c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e69c-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e69c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e69c-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e69c-152">INPUTS</span></span>

### <span data-ttu-id="5e69c-153">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e69c-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e69c-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e69c-154">OUTPUTS</span></span>

### <span data-ttu-id="5e69c-155">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e69c-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e69c-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e69c-156">NOTES</span></span>

## <span data-ttu-id="5e69c-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e69c-157">RELATED LINKS</span></span>

[<span data-ttu-id="5e69c-158">Dodaj-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5e69c-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5e69c-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5e69c-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5e69c-160">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5e69c-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5e69c-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5e69c-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

