---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240603"
---
# <span data-ttu-id="e9716-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e9716-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="e9716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9716-102">SYNOPSIS</span></span>
<span data-ttu-id="e9716-103">Umożliwia aktualizacje ustawień protokołu HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e9716-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="e9716-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9716-104">SYNTAX</span></span>

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

## <span data-ttu-id="e9716-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9716-105">DESCRIPTION</span></span>
<span data-ttu-id="e9716-106">Polecenie Set-AzApplicationGatewayBackendHttpSetting aktualizuje ustawienia protokołu HTTP (Hypertext Transfer Protocol) dla bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="e9716-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="e9716-107">Ustawienia protokołu HTTP typu Back-end są stosowane do wszystkich serwerów back-end w puli.</span><span class="sxs-lookup"><span data-stu-id="e9716-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="e9716-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9716-108">EXAMPLES</span></span>

### <span data-ttu-id="e9716-109">Przykład 1. Aktualizowanie ustawień protokołu HTTP dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e9716-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="e9716-110">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9716-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e9716-111">Drugie polecenie aktualizuje ustawienia HTTP bramy aplikacji w zmiennej $AppGw, aby używać portu 88, protokołu HTTP i umożliwia ffinity oparte na plikach cookie.</span><span class="sxs-lookup"><span data-stu-id="e9716-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="e9716-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9716-112">PARAMETERS</span></span>

### <span data-ttu-id="e9716-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e9716-113">-AffinityCookieName</span></span>
<span data-ttu-id="e9716-114">Nazwa pliku cookie do użycia dla pliku cookie affinity</span><span class="sxs-lookup"><span data-stu-id="e9716-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e9716-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9716-115">-ApplicationGateway</span></span>
<span data-ttu-id="e9716-116">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet skojarzy ustawienia protokołu HTTP na zawęzie.</span><span class="sxs-lookup"><span data-stu-id="e9716-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e9716-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e9716-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="e9716-118">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e9716-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="e9716-119">- ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e9716-119">-ConnectionDraining</span></span>
<span data-ttu-id="e9716-120">Wyczerpanie połączenia zasobu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e9716-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="e9716-121">- CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e9716-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="e9716-122">Określa, czy ffinity oparte na plikach cookie powinny być włączone, czy wyłączone dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e9716-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="e9716-123">Dopuszczalne wartości dla tego parametru to: Wyłączone lub Włączone.</span><span class="sxs-lookup"><span data-stu-id="e9716-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="e9716-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9716-124">-DefaultProfile</span></span>
<span data-ttu-id="e9716-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9716-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9716-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="e9716-126">-HostName</span></span>
<span data-ttu-id="e9716-127">Ustawia nagłówek hosta do wysłania na serwery zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e9716-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e9716-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e9716-128">-Name</span></span>
<span data-ttu-id="e9716-129">Określa nazwę obiektu ustawień protokołu HTTP w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e9716-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="e9716-130">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="e9716-130">-Path</span></span>
<span data-ttu-id="e9716-131">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9716-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e9716-132">Jeśli dla tego parametru nie podano żadnej wartości, oznacza to, że ścieżka nie będzie prefiksowana.</span><span class="sxs-lookup"><span data-stu-id="e9716-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e9716-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e9716-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e9716-134">Flaga oznacza, jeśli nagłówek hosta powinien być wybierany z nazwy hosta serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e9716-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="e9716-135">— Port</span><span class="sxs-lookup"><span data-stu-id="e9716-135">-Port</span></span>
<span data-ttu-id="e9716-136">Określa port do użycia dla każdego serwera w puli serwerów back-end.</span><span class="sxs-lookup"><span data-stu-id="e9716-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="e9716-137">— Dor.</span><span class="sxs-lookup"><span data-stu-id="e9716-137">-Probe</span></span>
<span data-ttu-id="e9716-138">Określa wartość do skojarzenia z ustawieniami protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9716-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e9716-139">- NaiwnyId</span><span class="sxs-lookup"><span data-stu-id="e9716-139">-ProbeId</span></span>
<span data-ttu-id="e9716-140">Określa identyfikator współpracownika, który ma skojarzyć z ustawieniami protokołu HTTP na zawęzie.</span><span class="sxs-lookup"><span data-stu-id="e9716-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e9716-141">— Protokół</span><span class="sxs-lookup"><span data-stu-id="e9716-141">-Protocol</span></span>
<span data-ttu-id="e9716-142">Określa protokół używany do komunikacji między bramą aplikacji a serwerami back-end.</span><span class="sxs-lookup"><span data-stu-id="e9716-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="e9716-143">Dopuszczalne wartości dla tego parametru to: Http i Https.</span><span class="sxs-lookup"><span data-stu-id="e9716-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="e9716-144">W tym parametrze jest zróżnicowa wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e9716-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="e9716-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e9716-145">-RequestTimeout</span></span>
<span data-ttu-id="e9716-146">Określa wartość prze wychodzącą z żądania.</span><span class="sxs-lookup"><span data-stu-id="e9716-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="e9716-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e9716-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="e9716-148">Zaufane certyfikaty główne bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e9716-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="e9716-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9716-149">CommonParameters</span></span>
<span data-ttu-id="e9716-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9716-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9716-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9716-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9716-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9716-152">INPUTS</span></span>

### <span data-ttu-id="e9716-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9716-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9716-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9716-154">OUTPUTS</span></span>

### <span data-ttu-id="e9716-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9716-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9716-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9716-156">NOTES</span></span>

## <span data-ttu-id="e9716-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9716-157">RELATED LINKS</span></span>

[<span data-ttu-id="e9716-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e9716-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e9716-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e9716-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e9716-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e9716-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e9716-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e9716-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

