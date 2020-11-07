---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 50f54d258e6b5575983d8cd35f487783ea922eb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892837"
---
# <span data-ttu-id="4baa6-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4baa6-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="4baa6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4baa6-102">SYNOPSIS</span></span>
<span data-ttu-id="4baa6-103">Ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4baa6-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="4baa6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4baa6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4baa6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4baa6-105">DESCRIPTION</span></span>
<span data-ttu-id="4baa6-106">Polecenie cmdlet Set-AzApplicationGatewayProbeConfig ustawia konfigurację badania kondycji na istniejącej bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4baa6-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="4baa6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4baa6-107">EXAMPLES</span></span>

### <span data-ttu-id="4baa6-108">Przykład 1: Ustawianie konfiguracji dla badania kondycji w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="4baa6-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="4baa6-109">To polecenie ustawia konfigurację dla badania kondycji o nazwie Probe05 dla bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="4baa6-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="4baa6-110">Polecenie ustawia również wartość progu niezdrowego na 8 ponownych prób i czas po 120 sekund.</span><span class="sxs-lookup"><span data-stu-id="4baa6-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="4baa6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4baa6-111">PARAMETERS</span></span>

### <span data-ttu-id="4baa6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4baa6-112">-ApplicationGateway</span></span>
<span data-ttu-id="4baa6-113">Określa bramę aplikacji, z którą to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="4baa6-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="4baa6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4baa6-114">-DefaultProfile</span></span>
<span data-ttu-id="4baa6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4baa6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4baa6-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="4baa6-116">-HostName</span></span>
<span data-ttu-id="4baa6-117">Określa nazwę hosta, do którego to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="4baa6-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="4baa6-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="4baa6-118">-Interval</span></span>
<span data-ttu-id="4baa6-119">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="4baa6-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="4baa6-120">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="4baa6-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="4baa6-121">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="4baa6-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4baa6-122">-Match</span><span class="sxs-lookup"><span data-stu-id="4baa6-122">-Match</span></span>
<span data-ttu-id="4baa6-123">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="4baa6-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="4baa6-124">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="4baa6-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4baa6-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="4baa6-125">-MinServers</span></span>
<span data-ttu-id="4baa6-126">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="4baa6-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="4baa6-127">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="4baa6-127">Default value is 0</span></span>

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

### <span data-ttu-id="4baa6-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4baa6-128">-Name</span></span>
<span data-ttu-id="4baa6-129">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="4baa6-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="4baa6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="4baa6-130">-Path</span></span>
<span data-ttu-id="4baa6-131">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="4baa6-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="4baa6-132">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="4baa6-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="4baa6-133">Sonda jest wysyłana do \< protokołu \> :// \< hosta \> : \< ścieżka portu \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="4baa6-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="4baa6-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4baa6-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="4baa6-135">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4baa6-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="4baa6-136">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="4baa6-136">Default value is false</span></span>

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

### <span data-ttu-id="4baa6-137">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="4baa6-137">-Protocol</span></span>
<span data-ttu-id="4baa6-138">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="4baa6-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="4baa6-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="4baa6-139">-Timeout</span></span>
<span data-ttu-id="4baa6-140">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="4baa6-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="4baa6-141">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="4baa6-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="4baa6-142">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="4baa6-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4baa6-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="4baa6-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="4baa6-144">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="4baa6-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="4baa6-145">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="4baa6-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="4baa6-146">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="4baa6-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="4baa6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4baa6-147">CommonParameters</span></span>
<span data-ttu-id="4baa6-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4baa6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4baa6-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4baa6-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4baa6-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4baa6-150">INPUTS</span></span>

### <span data-ttu-id="4baa6-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4baa6-151">PSApplicationGateway</span></span>
<span data-ttu-id="4baa6-152">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4baa6-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4baa6-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4baa6-153">OUTPUTS</span></span>

### <span data-ttu-id="4baa6-154">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4baa6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4baa6-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4baa6-155">NOTES</span></span>

## <span data-ttu-id="4baa6-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4baa6-156">RELATED LINKS</span></span>

[<span data-ttu-id="4baa6-157">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4baa6-157">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4baa6-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4baa6-158">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4baa6-159">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4baa6-159">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4baa6-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4baa6-160">Remove-AzApplicationGatewayProbeConfig</span></span>]()

