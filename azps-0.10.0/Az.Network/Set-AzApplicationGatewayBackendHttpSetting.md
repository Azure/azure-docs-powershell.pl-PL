---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 3696b33b18314d58e950fa9786e1febac5c3d22c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892854"
---
# <span data-ttu-id="f8b6b-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f8b6b-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="f8b6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b6b-103">Aktualizuje ustawienia HTTP zaplecza bramy Application.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="f8b6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8b6b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b6b-106">Polecenie cmdlet Set-AzApplicationGatewayBackendHttpSetting aktualizuje ustawienia protokołu HTTP (Hypertext Transfer Protocol) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="f8b6b-107">Ustawienia HTTP zaplecza są stosowane do wszystkich serwerów wewnętrznych w puli.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="f8b6b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8b6b-108">EXAMPLES</span></span>

### <span data-ttu-id="f8b6b-109">Przykład 1: aktualizowanie wewnętrznych ustawień HTTP dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f8b6b-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="f8b6b-110">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f8b6b-111">Drugie polecenie aktualizuje ustawienia HTTP bramy Application Gateway w zmiennej $AppGw, aby używać portów 88, protokołu HTTP i włączania koligacji opartych na plikach cookie.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="f8b6b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8b6b-112">PARAMETERS</span></span>

### <span data-ttu-id="f8b6b-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="f8b6b-113">-AffinityCookieName</span></span>
<span data-ttu-id="f8b6b-114">Nazwa pliku cookie do użycia w pliku cookie koligacji</span><span class="sxs-lookup"><span data-stu-id="f8b6b-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="f8b6b-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8b6b-115">-ApplicationGateway</span></span>
<span data-ttu-id="f8b6b-116">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f8b6b-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="f8b6b-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="f8b6b-118">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="f8b6b-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f8b6b-119">-ConnectionDraining</span></span>
<span data-ttu-id="f8b6b-120">Połączenie opróżniania zasobu Ustawienia http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="f8b6b-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="f8b6b-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="f8b6b-122">Określa, czy koligacja oparta na plikach cookie powinna być włączona lub wyłączona dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="f8b6b-123">Dopuszczalne wartości tego parametru są następujące: wyłączone lub włączone.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="f8b6b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b6b-124">-DefaultProfile</span></span>
<span data-ttu-id="f8b6b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b6b-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="f8b6b-126">-HostName</span></span>
<span data-ttu-id="f8b6b-127">Ustawia nagłówek hosta, który ma być wysyłany na serwery wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="f8b6b-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8b6b-128">-Name</span></span>
<span data-ttu-id="f8b6b-129">Określa nazwę obiektu zaplecza "Ustawienia HTTP".</span><span class="sxs-lookup"><span data-stu-id="f8b6b-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="f8b6b-130">-Path</span><span class="sxs-lookup"><span data-stu-id="f8b6b-130">-Path</span></span>
<span data-ttu-id="f8b6b-131">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="f8b6b-132">Jeśli dla tego parametru nie podano żadnej wartości, ścieżka nie zostanie naprawiona.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="f8b6b-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="f8b6b-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="f8b6b-134">Flaga Jeśli nagłówek hosta powinien być wybrany z nazwy hosta serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="f8b6b-135">-Port</span><span class="sxs-lookup"><span data-stu-id="f8b6b-135">-Port</span></span>
<span data-ttu-id="f8b6b-136">Określa port, który ma być używany dla każdego serwera w puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="f8b6b-137">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="f8b6b-137">-Probe</span></span>
<span data-ttu-id="f8b6b-138">Określa sondę do skojarzenia z ustawieniami HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f8b6b-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="f8b6b-139">-ProbeEnabled</span></span>
<span data-ttu-id="f8b6b-140">Flaga, czy sonda powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="f8b6b-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="f8b6b-141">-ProbeId</span></span>
<span data-ttu-id="f8b6b-142">Określa identyfikator sondy, która ma być skojarzona z ustawieniami protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f8b6b-143">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="f8b6b-143">-Protocol</span></span>
<span data-ttu-id="f8b6b-144">Określa protokół, który ma być używany do komunikacji między bramą aplikacji a serwerami zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="f8b6b-145">Dopuszczalne wartości tego parametru to: http i https.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="f8b6b-146">W tym parametrze jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="f8b6b-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="f8b6b-147">-RequestTimeout</span></span>
<span data-ttu-id="f8b6b-148">Określa wartość limitu czasu żądania.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="f8b6b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b6b-149">CommonParameters</span></span>
<span data-ttu-id="f8b6b-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b6b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b6b-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b6b-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b6b-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8b6b-152">INPUTS</span></span>

### <span data-ttu-id="f8b6b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f8b6b-153">System.String</span></span>

## <span data-ttu-id="f8b6b-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8b6b-154">OUTPUTS</span></span>

### <span data-ttu-id="f8b6b-155">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8b6b-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f8b6b-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8b6b-156">NOTES</span></span>

## <span data-ttu-id="f8b6b-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8b6b-157">RELATED LINKS</span></span>

[<span data-ttu-id="f8b6b-158">Dodaj-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f8b6b-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="f8b6b-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f8b6b-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="f8b6b-160">Nowe — AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f8b6b-160">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="f8b6b-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f8b6b-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

