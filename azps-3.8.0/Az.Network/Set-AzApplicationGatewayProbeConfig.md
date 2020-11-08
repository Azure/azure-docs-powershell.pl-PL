---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: e7da21709215b4ab185a573e32c8d15de901b33f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053792"
---
# <span data-ttu-id="2fc86-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2fc86-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2fc86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fc86-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc86-103">Ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2fc86-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="2fc86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fc86-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fc86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2fc86-105">DESCRIPTION</span></span>
<span data-ttu-id="2fc86-106">Polecenie cmdlet Set-AzApplicationGatewayProbeConfig ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2fc86-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="2fc86-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fc86-107">EXAMPLES</span></span>

### <span data-ttu-id="2fc86-108">Przykład 1: Ustawianie konfiguracji dla badania kondycji w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="2fc86-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="2fc86-109">To polecenie ustawia konfigurację dla badania kondycji o nazwie Probe05 dla bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="2fc86-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="2fc86-110">Polecenie ustawia również wartość progu niezdrowego na 8 ponownych prób i czas po 120 sekund.</span><span class="sxs-lookup"><span data-stu-id="2fc86-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="2fc86-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fc86-111">PARAMETERS</span></span>

### <span data-ttu-id="2fc86-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fc86-112">-ApplicationGateway</span></span>
<span data-ttu-id="2fc86-113">Określa bramę aplikacji, z którą to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="2fc86-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="2fc86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc86-114">-DefaultProfile</span></span>
<span data-ttu-id="2fc86-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc86-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc86-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="2fc86-116">-HostName</span></span>
<span data-ttu-id="2fc86-117">Określa nazwę hosta, do którego to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="2fc86-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="2fc86-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="2fc86-118">-Interval</span></span>
<span data-ttu-id="2fc86-119">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="2fc86-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="2fc86-120">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="2fc86-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="2fc86-121">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="2fc86-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2fc86-122">-Match</span><span class="sxs-lookup"><span data-stu-id="2fc86-122">-Match</span></span>
<span data-ttu-id="2fc86-123">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="2fc86-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="2fc86-124">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="2fc86-124">Default value is empty</span></span>

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

### <span data-ttu-id="2fc86-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="2fc86-125">-MinServers</span></span>
<span data-ttu-id="2fc86-126">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="2fc86-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="2fc86-127">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="2fc86-127">Default value is 0</span></span>

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

### <span data-ttu-id="2fc86-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fc86-128">-Name</span></span>
<span data-ttu-id="2fc86-129">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="2fc86-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="2fc86-130">-Path</span><span class="sxs-lookup"><span data-stu-id="2fc86-130">-Path</span></span>
<span data-ttu-id="2fc86-131">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="2fc86-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="2fc86-132">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="2fc86-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="2fc86-133">Sonda jest wysyłana do \< protokołu \> :// \< hosta \> : \< ścieżka portu \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="2fc86-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="2fc86-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2fc86-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="2fc86-135">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2fc86-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="2fc86-136">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="2fc86-136">Default value is false</span></span>

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

### <span data-ttu-id="2fc86-137">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="2fc86-137">-Protocol</span></span>
<span data-ttu-id="2fc86-138">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="2fc86-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="2fc86-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="2fc86-139">-Timeout</span></span>
<span data-ttu-id="2fc86-140">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="2fc86-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="2fc86-141">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="2fc86-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="2fc86-142">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="2fc86-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2fc86-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="2fc86-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="2fc86-144">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="2fc86-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="2fc86-145">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="2fc86-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="2fc86-146">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="2fc86-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="2fc86-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc86-147">CommonParameters</span></span>
<span data-ttu-id="2fc86-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc86-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc86-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc86-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc86-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fc86-150">INPUTS</span></span>

### <span data-ttu-id="2fc86-151">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fc86-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fc86-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fc86-152">OUTPUTS</span></span>

### <span data-ttu-id="2fc86-153">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fc86-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fc86-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fc86-154">NOTES</span></span>

## <span data-ttu-id="2fc86-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fc86-155">RELATED LINKS</span></span>

[<span data-ttu-id="2fc86-156">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2fc86-156">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2fc86-157">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2fc86-157">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2fc86-158">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2fc86-158">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2fc86-159">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2fc86-159">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

