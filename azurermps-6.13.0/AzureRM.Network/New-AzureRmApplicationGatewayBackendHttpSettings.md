---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 3b292b70e96c8da57a87834ecc4c095c9ca3f55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541696"
---
# <span data-ttu-id="70f79-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="70f79-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="70f79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70f79-102">SYNOPSIS</span></span>
<span data-ttu-id="70f79-103">Umożliwia utworzenie wewnętrznych ustawień HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="70f79-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70f79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70f79-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70f79-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70f79-105">DESCRIPTION</span></span>
<span data-ttu-id="70f79-106">Polecenie cmdlet New-AzureRmApplicationGatewayBackendHttpSettings służy do tworzenia wewnętrznych ustawień HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="70f79-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="70f79-107">Ustawienia HTTP zaplecza są stosowane do wszystkich serwerów wewnętrznych w puli.</span><span class="sxs-lookup"><span data-stu-id="70f79-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="70f79-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70f79-108">EXAMPLES</span></span>

### <span data-ttu-id="70f79-109">Przykład 1: Tworzenie wewnętrznych ustawień HTTP</span><span class="sxs-lookup"><span data-stu-id="70f79-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="70f79-110">To polecenie umożliwia tworzenie wewnętrznych ustawień HTTP o nazwie Setting01 na porcie 80 przy użyciu protokołu HTTP z wyłączonymi koligacjami opartymi na plikach cookie.</span><span class="sxs-lookup"><span data-stu-id="70f79-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="70f79-111">Ustawienia są przechowywane w zmiennej $Setting.</span><span class="sxs-lookup"><span data-stu-id="70f79-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="70f79-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70f79-112">PARAMETERS</span></span>

### <span data-ttu-id="70f79-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="70f79-113">-AffinityCookieName</span></span>
<span data-ttu-id="70f79-114">Nazwa pliku cookie do użycia w pliku cookie koligacji</span><span class="sxs-lookup"><span data-stu-id="70f79-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="70f79-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="70f79-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="70f79-116">Określa certyfikaty uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="70f79-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="70f79-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="70f79-117">-ConnectionDraining</span></span>
<span data-ttu-id="70f79-118">Połączenie opróżniania zasobu Ustawienia http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="70f79-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="70f79-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="70f79-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="70f79-120">Określa, czy koligacja oparta na plikach cookie powinna być włączona lub wyłączona dla puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="70f79-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="70f79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f79-121">-DefaultProfile</span></span>
<span data-ttu-id="70f79-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70f79-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f79-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="70f79-123">-HostName</span></span>
<span data-ttu-id="70f79-124">Ustawia nagłówek hosta, który ma być wysyłany na serwery wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70f79-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="70f79-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70f79-125">-Name</span></span>
<span data-ttu-id="70f79-126">Określa nazwę ustawień HTTP zaplecza, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70f79-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="70f79-127">-Path</span><span class="sxs-lookup"><span data-stu-id="70f79-127">-Path</span></span>
<span data-ttu-id="70f79-128">Ścieżka, która powinna być używana jako prefiks dla wszystkich żądań HTTP.</span><span class="sxs-lookup"><span data-stu-id="70f79-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="70f79-129">Jeśli dla tego parametru nie podano żadnej wartości, ścieżka nie zostanie naprawiona.</span><span class="sxs-lookup"><span data-stu-id="70f79-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="70f79-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="70f79-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="70f79-131">Flaga Jeśli nagłówek hosta powinien być wybrany z nazwy hosta serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="70f79-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="70f79-132">-Port</span><span class="sxs-lookup"><span data-stu-id="70f79-132">-Port</span></span>
<span data-ttu-id="70f79-133">Określa port puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="70f79-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="70f79-134">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="70f79-134">-Probe</span></span>
<span data-ttu-id="70f79-135">Określa sondę do skojarzenia z pulą serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="70f79-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="70f79-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="70f79-136">-ProbeId</span></span>
<span data-ttu-id="70f79-137">Określa identyfikator sondy, która ma być skojarzona z pulą serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="70f79-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="70f79-138">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="70f79-138">-Protocol</span></span>
<span data-ttu-id="70f79-139">Określa protokół, który ma być używany do komunikacji między bramą aplikacji a serwerami zaplecza.</span><span class="sxs-lookup"><span data-stu-id="70f79-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="70f79-140">Dopuszczalne wartości tego parametru to: http i https.</span><span class="sxs-lookup"><span data-stu-id="70f79-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="70f79-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="70f79-141">-RequestTimeout</span></span>
<span data-ttu-id="70f79-142">Określa wartość limitu czasu żądania.</span><span class="sxs-lookup"><span data-stu-id="70f79-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="70f79-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="70f79-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="70f79-144">Zaufane certyfikaty główne bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="70f79-144">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f79-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f79-145">CommonParameters</span></span>
<span data-ttu-id="70f79-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f79-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f79-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f79-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f79-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70f79-148">INPUTS</span></span>

### <span data-ttu-id="70f79-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70f79-149">None</span></span>

## <span data-ttu-id="70f79-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70f79-150">OUTPUTS</span></span>

### <span data-ttu-id="70f79-151">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="70f79-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="70f79-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70f79-152">NOTES</span></span>

## <span data-ttu-id="70f79-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70f79-153">RELATED LINKS</span></span>

[<span data-ttu-id="70f79-154">Dodaj-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="70f79-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="70f79-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="70f79-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="70f79-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="70f79-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="70f79-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="70f79-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

