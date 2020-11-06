---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 212e418c3fdaf8ba7f67ebdae0565d5d230daa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546199"
---
# <span data-ttu-id="926d6-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="926d6-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="926d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="926d6-102">SYNOPSIS</span></span>
<span data-ttu-id="926d6-103">Ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="926d6-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="926d6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="926d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="926d6-105">DESCRIPTION</span></span>
<span data-ttu-id="926d6-106">Polecenie cmdlet Set-AzureRmApplicationGatewayProbeConfig ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="926d6-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="926d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="926d6-107">EXAMPLES</span></span>

### <span data-ttu-id="926d6-108">Przykład 1: Ustawianie konfiguracji dla badania kondycji w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="926d6-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="926d6-109">To polecenie ustawia konfigurację dla badania kondycji o nazwie Probe05 dla bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="926d6-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="926d6-110">Polecenie ustawia również wartość progu niezdrowego na 8 ponownych prób i czas po 120 sekund.</span><span class="sxs-lookup"><span data-stu-id="926d6-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="926d6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="926d6-111">PARAMETERS</span></span>

### <span data-ttu-id="926d6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="926d6-112">-ApplicationGateway</span></span>
<span data-ttu-id="926d6-113">Określa bramę aplikacji, z którą to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="926d6-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="926d6-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="926d6-114">-HostName</span></span>
<span data-ttu-id="926d6-115">Określa nazwę hosta, do którego to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="926d6-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="926d6-116">-Interval</span><span class="sxs-lookup"><span data-stu-id="926d6-116">-Interval</span></span>
<span data-ttu-id="926d6-117">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="926d6-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="926d6-118">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="926d6-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="926d6-119">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="926d6-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="926d6-120">-Match</span><span class="sxs-lookup"><span data-stu-id="926d6-120">-Match</span></span>
<span data-ttu-id="926d6-121">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="926d6-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="926d6-122">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="926d6-122">Default value is empty</span></span>

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

### <span data-ttu-id="926d6-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="926d6-123">-MinServers</span></span>
<span data-ttu-id="926d6-124">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="926d6-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="926d6-125">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="926d6-125">Default value is 0</span></span>

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

### <span data-ttu-id="926d6-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="926d6-126">-Name</span></span>
<span data-ttu-id="926d6-127">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="926d6-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="926d6-128">-Path</span><span class="sxs-lookup"><span data-stu-id="926d6-128">-Path</span></span>
<span data-ttu-id="926d6-129">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="926d6-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="926d6-130">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="926d6-130">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="926d6-131">Sonda jest wysyłana do \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="926d6-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="926d6-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="926d6-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="926d6-133">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="926d6-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="926d6-134">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="926d6-134">Default value is false</span></span>

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

### <span data-ttu-id="926d6-135">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="926d6-135">-Protocol</span></span>
<span data-ttu-id="926d6-136">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="926d6-136">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="926d6-137">-Timeout</span><span class="sxs-lookup"><span data-stu-id="926d6-137">-Timeout</span></span>
<span data-ttu-id="926d6-138">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="926d6-138">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="926d6-139">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="926d6-139">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="926d6-140">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="926d6-140">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="926d6-141">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="926d6-141">-UnhealthyThreshold</span></span>
<span data-ttu-id="926d6-142">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="926d6-142">Specifies the probe retry count.</span></span>
<span data-ttu-id="926d6-143">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="926d6-143">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="926d6-144">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="926d6-144">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="926d6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926d6-145">-DefaultProfile</span></span>
<span data-ttu-id="926d6-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="926d6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926d6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926d6-147">CommonParameters</span></span>
<span data-ttu-id="926d6-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926d6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926d6-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926d6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926d6-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="926d6-150">INPUTS</span></span>

### <span data-ttu-id="926d6-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="926d6-151">PSApplicationGateway</span></span>
<span data-ttu-id="926d6-152">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="926d6-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="926d6-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="926d6-153">OUTPUTS</span></span>

### <span data-ttu-id="926d6-154">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="926d6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="926d6-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="926d6-155">NOTES</span></span>

## <span data-ttu-id="926d6-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="926d6-156">RELATED LINKS</span></span>

[<span data-ttu-id="926d6-157">Dodaj-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="926d6-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="926d6-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="926d6-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="926d6-159">Nowe — AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="926d6-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="926d6-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="926d6-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

