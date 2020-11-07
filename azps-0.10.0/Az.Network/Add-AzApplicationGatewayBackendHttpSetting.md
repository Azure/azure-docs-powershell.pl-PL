---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 4361d025026e3ff9c9a72a092a99a72b8b63c850
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891038"
---
# <span data-ttu-id="3cec9-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3cec9-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="3cec9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cec9-102">SYNOPSIS</span></span>
<span data-ttu-id="3cec9-103">Dodaje Wstecz-End ustawienia HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3cec9-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="3cec9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cec9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cec9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cec9-105">DESCRIPTION</span></span>
<span data-ttu-id="3cec9-106">Polecenie cmdlet Add-AzApplicationGatewayBackendHttpSetting powoduje dodanie wewnętrznych ustawień HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3cec9-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="3cec9-107">Ustawienia HTTP zaplecza są stosowane do wszystkich serwerów wewnętrznych w puli.</span><span class="sxs-lookup"><span data-stu-id="3cec9-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="3cec9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cec9-108">EXAMPLES</span></span>

### <span data-ttu-id="3cec9-109">Przykład 1: Dodawanie ustawień protokołu HTTP zaplecza do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3cec9-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="3cec9-110">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje wstecz-End ustawienia HTTP do bramy Application Gateway, ustawiając port na 88 i protokół na HTTP, a następnie nadaje nazwę Setting02.</span><span class="sxs-lookup"><span data-stu-id="3cec9-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="3cec9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cec9-111">PARAMETERS</span></span>

### <span data-ttu-id="3cec9-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="3cec9-112">-AffinityCookieName</span></span>
<span data-ttu-id="3cec9-113">Nazwa pliku cookie do użycia w pliku cookie koligacji</span><span class="sxs-lookup"><span data-stu-id="3cec9-113">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3cec9-114">-ApplicationGateway</span></span>
<span data-ttu-id="3cec9-115">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje ustawienia.</span><span class="sxs-lookup"><span data-stu-id="3cec9-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="3cec9-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="3cec9-117">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3cec9-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="3cec9-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="3cec9-118">-ConnectionDraining</span></span>
<span data-ttu-id="3cec9-119">Połączenie opróżniania zasobu Ustawienia http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3cec9-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="3cec9-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="3cec9-121">Określa, czy koligacja oparta na plikach cookie powinna być włączona lub wyłączona dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3cec9-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="3cec9-122">Dopuszczalne wartości tego parametru to: wyłączone, włączone.</span><span class="sxs-lookup"><span data-stu-id="3cec9-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cec9-123">-DefaultProfile</span></span>
<span data-ttu-id="3cec9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cec9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cec9-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="3cec9-125">-HostName</span></span>
<span data-ttu-id="3cec9-126">Ustawia nagłówek hosta, który ma być wysyłany na serwery wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3cec9-126">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cec9-127">-Name</span></span>
<span data-ttu-id="3cec9-128">Określa nazwę ustawienia HTTP zaplecza, które ma zostać dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cec9-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="3cec9-129">-Path</span><span class="sxs-lookup"><span data-stu-id="3cec9-129">-Path</span></span>
<span data-ttu-id="3cec9-130">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="3cec9-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="3cec9-131">Jeśli dla tego parametru nie podano żadnej wartości, ścieżka nie zostanie naprawiona.</span><span class="sxs-lookup"><span data-stu-id="3cec9-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="3cec9-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="3cec9-133">Flaga Jeśli nagłówek hosta powinien być wybrany z nazwy hosta serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3cec9-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-134">-Port</span><span class="sxs-lookup"><span data-stu-id="3cec9-134">-Port</span></span>
<span data-ttu-id="3cec9-135">Określa port puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3cec9-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-136">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="3cec9-136">-Probe</span></span>
<span data-ttu-id="3cec9-137">Określa sondę do skojarzenia z serwerem zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3cec9-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="3cec9-138">-ProbeEnabled</span></span>
<span data-ttu-id="3cec9-139">Flaga, czy sonda powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="3cec9-139">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-140">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="3cec9-140">-ProbeId</span></span>
<span data-ttu-id="3cec9-141">Określa identyfikator sondy, która ma być skojarzona z serwerem zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3cec9-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-142">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="3cec9-142">-Protocol</span></span>
<span data-ttu-id="3cec9-143">Określa protokół komunikacji między bramą aplikacji a serwerami zaplecza.</span><span class="sxs-lookup"><span data-stu-id="3cec9-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="3cec9-144">Dopuszczalne wartości tego parametru to: http i https.</span><span class="sxs-lookup"><span data-stu-id="3cec9-144">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="3cec9-145">-RequestTimeout</span></span>
<span data-ttu-id="3cec9-146">Określa wartość limitu czasu żądania.</span><span class="sxs-lookup"><span data-stu-id="3cec9-146">Specifies the request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cec9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cec9-147">CommonParameters</span></span>
<span data-ttu-id="3cec9-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cec9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cec9-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cec9-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cec9-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cec9-150">INPUTS</span></span>

### <span data-ttu-id="3cec9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3cec9-151">System.String</span></span>

## <span data-ttu-id="3cec9-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cec9-152">OUTPUTS</span></span>

### <span data-ttu-id="3cec9-153">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3cec9-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3cec9-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cec9-154">NOTES</span></span>

## <span data-ttu-id="3cec9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cec9-155">RELATED LINKS</span></span>

[<span data-ttu-id="3cec9-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3cec9-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="3cec9-157">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3cec9-157">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="3cec9-158">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3cec9-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="3cec9-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3cec9-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

