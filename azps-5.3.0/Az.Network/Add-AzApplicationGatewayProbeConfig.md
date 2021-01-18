---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499625"
---
# <span data-ttu-id="8528c-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8528c-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="8528c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8528c-102">SYNOPSIS</span></span>
<span data-ttu-id="8528c-103">Dodaje badanie kondycji do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8528c-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="8528c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8528c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8528c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8528c-105">DESCRIPTION</span></span>
<span data-ttu-id="8528c-106">Polecenie cmdlet Add-AzApplicationGatewayProbeConfig umożliwia dodanie sondy kondycji do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8528c-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="8528c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8528c-107">EXAMPLES</span></span>

### <span data-ttu-id="8528c-108">Przykład 1: Dodawanie sondy kondycji do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8528c-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="8528c-109">To polecenie dodaje sondę Health o nazwie Probe01 dla bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="8528c-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="8528c-110">Polecenie ustawia również wartość progu niezdrowego na 8 ponownych prób i czas po 120 sekund.</span><span class="sxs-lookup"><span data-stu-id="8528c-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="8528c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8528c-111">PARAMETERS</span></span>

### <span data-ttu-id="8528c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8528c-112">-ApplicationGateway</span></span>
<span data-ttu-id="8528c-113">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje sondę.</span><span class="sxs-lookup"><span data-stu-id="8528c-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="8528c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8528c-114">-DefaultProfile</span></span>
<span data-ttu-id="8528c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8528c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8528c-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="8528c-116">-HostName</span></span>
<span data-ttu-id="8528c-117">Określa nazwę hosta, do którego to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="8528c-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="8528c-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="8528c-118">-Interval</span></span>
<span data-ttu-id="8528c-119">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="8528c-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="8528c-120">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="8528c-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="8528c-121">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="8528c-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="8528c-122">-Match</span><span class="sxs-lookup"><span data-stu-id="8528c-122">-Match</span></span>
<span data-ttu-id="8528c-123">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="8528c-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="8528c-124">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="8528c-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8528c-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="8528c-125">-MinServers</span></span>
<span data-ttu-id="8528c-126">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="8528c-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="8528c-127">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="8528c-127">Default value is 0</span></span>

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

### <span data-ttu-id="8528c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8528c-128">-Name</span></span>
<span data-ttu-id="8528c-129">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="8528c-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="8528c-130">-Path</span><span class="sxs-lookup"><span data-stu-id="8528c-130">-Path</span></span>
<span data-ttu-id="8528c-131">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="8528c-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="8528c-132">Prawidłowa ścieżka zaczyna się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="8528c-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="8528c-133">Sonda jest wysyłana do \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="8528c-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="8528c-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8528c-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="8528c-135">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="8528c-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="8528c-136">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="8528c-136">Default value is false</span></span>

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

### <span data-ttu-id="8528c-137">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="8528c-137">-Protocol</span></span>
<span data-ttu-id="8528c-138">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="8528c-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="8528c-139">To polecenie cmdlet obsługuje tylko protokół HTTP.</span><span class="sxs-lookup"><span data-stu-id="8528c-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="8528c-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="8528c-140">-Timeout</span></span>
<span data-ttu-id="8528c-141">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="8528c-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="8528c-142">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="8528c-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="8528c-143">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="8528c-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="8528c-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="8528c-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="8528c-145">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="8528c-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="8528c-146">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="8528c-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="8528c-147">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="8528c-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="8528c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8528c-148">CommonParameters</span></span>
<span data-ttu-id="8528c-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8528c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8528c-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8528c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8528c-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8528c-151">INPUTS</span></span>

### <span data-ttu-id="8528c-152">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8528c-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8528c-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8528c-153">OUTPUTS</span></span>

### <span data-ttu-id="8528c-154">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8528c-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8528c-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8528c-155">NOTES</span></span>

## <span data-ttu-id="8528c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8528c-156">RELATED LINKS</span></span>

[<span data-ttu-id="8528c-157">Dodawanie sondy do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8528c-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="8528c-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8528c-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="8528c-159">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8528c-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="8528c-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8528c-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="8528c-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8528c-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

