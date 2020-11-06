---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: add18f52e46f39c639c87526d948c750bb22fa93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553228"
---
# <span data-ttu-id="e26e5-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e26e5-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e26e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e26e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e26e5-103">Dodaje Wstecz-End ustawienia HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e26e5-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e26e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e26e5-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e26e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e26e5-106">Polecenie cmdlet Add-AzureRmApplicationGatewayBackendHttpSettings powoduje dodanie wewnętrznych ustawień HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e26e5-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="e26e5-107">Ustawienia HTTP zaplecza są stosowane do wszystkich serwerów wewnętrznych w puli.</span><span class="sxs-lookup"><span data-stu-id="e26e5-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="e26e5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e26e5-108">EXAMPLES</span></span>

### <span data-ttu-id="e26e5-109">Przykład 1: Dodawanie ustawień protokołu HTTP zaplecza do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e26e5-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="e26e5-110">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje wstecz-End ustawienia HTTP do bramy Application Gateway, ustawiając port na 88 i protokół na HTTP, a następnie nadaje nazwę Setting02.</span><span class="sxs-lookup"><span data-stu-id="e26e5-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="e26e5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e26e5-111">PARAMETERS</span></span>

### <span data-ttu-id="e26e5-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e26e5-112">-AffinityCookieName</span></span>
<span data-ttu-id="e26e5-113">Nazwa pliku cookie do użycia w pliku cookie koligacji</span><span class="sxs-lookup"><span data-stu-id="e26e5-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e26e5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e26e5-114">-ApplicationGateway</span></span>
<span data-ttu-id="e26e5-115">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e26e5-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="e26e5-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e26e5-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="e26e5-117">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e26e5-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26e5-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e26e5-118">-ConnectionDraining</span></span>
<span data-ttu-id="e26e5-119">Połączenie opróżniania zasobu Ustawienia http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e26e5-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="e26e5-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e26e5-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="e26e5-121">Określa, czy koligacja oparta na plikach cookie powinna być włączona lub wyłączona dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e26e5-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="e26e5-122">Dopuszczalne wartości tego parametru to: wyłączone, włączone.</span><span class="sxs-lookup"><span data-stu-id="e26e5-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="e26e5-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="e26e5-123">-HostName</span></span>
<span data-ttu-id="e26e5-124">Ustawia nagłówek hosta, który ma być wysyłany na serwery wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e26e5-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e26e5-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e26e5-125">-Name</span></span>
<span data-ttu-id="e26e5-126">Określa nazwę ustawienia HTTP zaplecza, które ma zostać dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e26e5-126">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="e26e5-127">-Path</span><span class="sxs-lookup"><span data-stu-id="e26e5-127">-Path</span></span>
<span data-ttu-id="e26e5-128">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="e26e5-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e26e5-129">Jeśli dla tego parametru nie podano żadnej wartości, ścieżka nie zostanie naprawiona.</span><span class="sxs-lookup"><span data-stu-id="e26e5-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e26e5-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e26e5-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e26e5-131">Flaga Jeśli nagłówek hosta powinien być wybrany z nazwy hosta serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e26e5-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="e26e5-132">-Port</span><span class="sxs-lookup"><span data-stu-id="e26e5-132">-Port</span></span>
<span data-ttu-id="e26e5-133">Określa port puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e26e5-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="e26e5-134">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="e26e5-134">-Probe</span></span>
<span data-ttu-id="e26e5-135">Określa sondę do skojarzenia z serwerem zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e26e5-135">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="e26e5-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="e26e5-136">-ProbeEnabled</span></span>
<span data-ttu-id="e26e5-137">Flaga, czy sonda powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="e26e5-137">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="e26e5-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e26e5-138">-ProbeId</span></span>
<span data-ttu-id="e26e5-139">Określa identyfikator sondy, która ma być skojarzona z serwerem zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e26e5-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="e26e5-140">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e26e5-140">-Protocol</span></span>
<span data-ttu-id="e26e5-141">Określa protokół komunikacji między bramą aplikacji a serwerami zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e26e5-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="e26e5-142">Dopuszczalne wartości tego parametru to: http i https.</span><span class="sxs-lookup"><span data-stu-id="e26e5-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="e26e5-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e26e5-143">-RequestTimeout</span></span>
<span data-ttu-id="e26e5-144">Określa wartość limitu czasu żądania.</span><span class="sxs-lookup"><span data-stu-id="e26e5-144">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="e26e5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26e5-145">-DefaultProfile</span></span>
<span data-ttu-id="e26e5-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e26e5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e26e5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26e5-147">CommonParameters</span></span>
<span data-ttu-id="e26e5-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26e5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26e5-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26e5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26e5-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e26e5-150">INPUTS</span></span>

### <span data-ttu-id="e26e5-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e26e5-151">System.String</span></span>

## <span data-ttu-id="e26e5-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e26e5-152">OUTPUTS</span></span>

### <span data-ttu-id="e26e5-153">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e26e5-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e26e5-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e26e5-154">NOTES</span></span>

## <span data-ttu-id="e26e5-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e26e5-155">RELATED LINKS</span></span>

[<span data-ttu-id="e26e5-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e26e5-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e26e5-157">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e26e5-157">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e26e5-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e26e5-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e26e5-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e26e5-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

