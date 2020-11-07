---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 87d875881ce6086f033353dd4b37ba8a8098a96c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719613"
---
# <span data-ttu-id="a1a03-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a1a03-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="a1a03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1a03-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a03-103">Aktualizuje ustawienia HTTP zaplecza bramy Application.</span><span class="sxs-lookup"><span data-stu-id="a1a03-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1a03-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a03-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1a03-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a03-106">Polecenie cmdlet Set-AzureRmApplicationGatewayBackendHttpSettings aktualizuje ustawienia protokołu HTTP (Hypertext Transfer Protocol) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a03-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="a1a03-107">Ustawienia HTTP zaplecza są stosowane do wszystkich serwerów wewnętrznych w puli.</span><span class="sxs-lookup"><span data-stu-id="a1a03-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="a1a03-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1a03-108">EXAMPLES</span></span>

### <span data-ttu-id="a1a03-109">Przykład 1: aktualizowanie wewnętrznych ustawień HTTP dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a1a03-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="a1a03-110">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a1a03-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a1a03-111">Drugie polecenie aktualizuje ustawienia HTTP bramy Application Gateway w zmiennej $AppGw, aby używać portów 88, protokołu HTTP i włączania koligacji opartych na plikach cookie.</span><span class="sxs-lookup"><span data-stu-id="a1a03-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="a1a03-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1a03-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a03-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="a1a03-113">-AffinityCookieName</span></span>
<span data-ttu-id="a1a03-114">Nazwa pliku cookie do użycia w pliku cookie koligacji</span><span class="sxs-lookup"><span data-stu-id="a1a03-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="a1a03-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1a03-115">-ApplicationGateway</span></span>
<span data-ttu-id="a1a03-116">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy ustawienia HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a1a03-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="a1a03-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="a1a03-118">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1a03-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="a1a03-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a1a03-119">-ConnectionDraining</span></span>
<span data-ttu-id="a1a03-120">Połączenie opróżniania zasobu Ustawienia http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="a1a03-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="a1a03-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="a1a03-122">Określa, czy koligacja oparta na plikach cookie powinna być włączona lub wyłączona dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="a1a03-123">Dopuszczalne wartości tego parametru są następujące: wyłączone lub włączone.</span><span class="sxs-lookup"><span data-stu-id="a1a03-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="a1a03-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="a1a03-124">-HostName</span></span>
<span data-ttu-id="a1a03-125">Ustawia nagłówek hosta, który ma być wysyłany na serwery wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a1a03-125">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="a1a03-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1a03-126">-Name</span></span>
<span data-ttu-id="a1a03-127">Określa nazwę obiektu zaplecza "Ustawienia HTTP".</span><span class="sxs-lookup"><span data-stu-id="a1a03-127">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="a1a03-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a1a03-128">-Path</span></span>
<span data-ttu-id="a1a03-129">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1a03-129">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="a1a03-130">Jeśli dla tego parametru nie podano żadnej wartości, ścieżka nie zostanie naprawiona.</span><span class="sxs-lookup"><span data-stu-id="a1a03-130">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="a1a03-131">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="a1a03-131">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="a1a03-132">Flaga Jeśli nagłówek hosta powinien być wybrany z nazwy hosta serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a1a03-132">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="a1a03-133">-Port</span><span class="sxs-lookup"><span data-stu-id="a1a03-133">-Port</span></span>
<span data-ttu-id="a1a03-134">Określa port, który ma być używany dla każdego serwera w puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-134">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="a1a03-135">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="a1a03-135">-Probe</span></span>
<span data-ttu-id="a1a03-136">Określa sondę do skojarzenia z ustawieniami HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-136">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a1a03-137">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="a1a03-137">-ProbeEnabled</span></span>
<span data-ttu-id="a1a03-138">Flaga, czy sonda powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="a1a03-138">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="a1a03-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a1a03-139">-ProbeId</span></span>
<span data-ttu-id="a1a03-140">Określa identyfikator sondy, która ma być skojarzona z ustawieniami protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a1a03-141">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="a1a03-141">-Protocol</span></span>
<span data-ttu-id="a1a03-142">Określa protokół, który ma być używany do komunikacji między bramą aplikacji a serwerami zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a1a03-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="a1a03-143">Dopuszczalne wartości tego parametru to: http i https.</span><span class="sxs-lookup"><span data-stu-id="a1a03-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="a1a03-144">W tym parametrze jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a1a03-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="a1a03-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="a1a03-145">-RequestTimeout</span></span>
<span data-ttu-id="a1a03-146">Określa wartość limitu czasu żądania.</span><span class="sxs-lookup"><span data-stu-id="a1a03-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="a1a03-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a03-147">-DefaultProfile</span></span>
<span data-ttu-id="a1a03-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a03-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a03-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a03-149">CommonParameters</span></span>
<span data-ttu-id="a1a03-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a03-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a03-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a03-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a03-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1a03-152">INPUTS</span></span>

### <span data-ttu-id="a1a03-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a1a03-153">System.String</span></span>

## <span data-ttu-id="a1a03-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1a03-154">OUTPUTS</span></span>

### <span data-ttu-id="a1a03-155">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1a03-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a1a03-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1a03-156">NOTES</span></span>

## <span data-ttu-id="a1a03-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1a03-157">RELATED LINKS</span></span>

[<span data-ttu-id="a1a03-158">Dodaj-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a1a03-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="a1a03-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a1a03-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="a1a03-160">Nowe — AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a1a03-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="a1a03-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a1a03-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

