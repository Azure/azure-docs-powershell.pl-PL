---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 30a717d24145364f2850a381382e8d7d35303172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718792"
---
# <span data-ttu-id="620c9-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="620c9-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="620c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="620c9-102">SYNOPSIS</span></span>
<span data-ttu-id="620c9-103">Ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="620c9-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="620c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="620c9-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="620c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="620c9-105">DESCRIPTION</span></span>
<span data-ttu-id="620c9-106">Polecenie cmdlet Set-AzureRmApplicationGatewayProbeConfig ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="620c9-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="620c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="620c9-107">EXAMPLES</span></span>

### <span data-ttu-id="620c9-108">Przykład 1: Ustawianie konfiguracji dla badania kondycji w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="620c9-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="620c9-109">To polecenie ustawia konfigurację dla badania kondycji o nazwie Probe05 dla bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="620c9-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="620c9-110">Polecenie ustawia również wartość progu niezdrowego na 8 ponownych prób i czas po 120 sekund.</span><span class="sxs-lookup"><span data-stu-id="620c9-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="620c9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="620c9-111">PARAMETERS</span></span>

### <span data-ttu-id="620c9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="620c9-112">-ApplicationGateway</span></span>
<span data-ttu-id="620c9-113">Określa bramę aplikacji, z którą to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="620c9-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="620c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620c9-114">-DefaultProfile</span></span>
<span data-ttu-id="620c9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="620c9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="620c9-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="620c9-116">-HostName</span></span>
<span data-ttu-id="620c9-117">Określa nazwę hosta, do którego to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="620c9-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="620c9-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="620c9-118">-Interval</span></span>
<span data-ttu-id="620c9-119">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="620c9-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="620c9-120">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="620c9-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="620c9-121">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="620c9-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="620c9-122">-Match</span><span class="sxs-lookup"><span data-stu-id="620c9-122">-Match</span></span>
<span data-ttu-id="620c9-123">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="620c9-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="620c9-124">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="620c9-124">Default value is empty</span></span>

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

### <span data-ttu-id="620c9-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="620c9-125">-MinServers</span></span>
<span data-ttu-id="620c9-126">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="620c9-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="620c9-127">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="620c9-127">Default value is 0</span></span>

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

### <span data-ttu-id="620c9-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="620c9-128">-Name</span></span>
<span data-ttu-id="620c9-129">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="620c9-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="620c9-130">-Path</span><span class="sxs-lookup"><span data-stu-id="620c9-130">-Path</span></span>
<span data-ttu-id="620c9-131">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="620c9-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="620c9-132">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="620c9-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="620c9-133">Sonda jest wysyłana do \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="620c9-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="620c9-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="620c9-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="620c9-135">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="620c9-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="620c9-136">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="620c9-136">Default value is false</span></span>

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

### <span data-ttu-id="620c9-137">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="620c9-137">-Protocol</span></span>
<span data-ttu-id="620c9-138">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="620c9-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="620c9-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="620c9-139">-Timeout</span></span>
<span data-ttu-id="620c9-140">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="620c9-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="620c9-141">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="620c9-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="620c9-142">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="620c9-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="620c9-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="620c9-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="620c9-144">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="620c9-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="620c9-145">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="620c9-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="620c9-146">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="620c9-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="620c9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620c9-147">CommonParameters</span></span>
<span data-ttu-id="620c9-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620c9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620c9-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620c9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620c9-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="620c9-150">INPUTS</span></span>

### <span data-ttu-id="620c9-151">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="620c9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="620c9-152">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="620c9-152">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="620c9-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="620c9-153">OUTPUTS</span></span>

### <span data-ttu-id="620c9-154">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="620c9-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="620c9-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="620c9-155">NOTES</span></span>

## <span data-ttu-id="620c9-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="620c9-156">RELATED LINKS</span></span>

[<span data-ttu-id="620c9-157">Dodaj-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="620c9-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="620c9-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="620c9-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="620c9-159">Nowe — AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="620c9-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="620c9-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="620c9-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()
