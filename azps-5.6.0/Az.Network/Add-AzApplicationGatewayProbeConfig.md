---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 385a77c2b7b11d20b3ffb8d3728720b46c431d4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982529"
---
# <span data-ttu-id="4ef0a-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4ef0a-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="4ef0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef0a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef0a-103">Dodaje kondycję do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="4ef0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ef0a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef0a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ef0a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef0a-106">Polecenie Add-AzApplicationGatewayProbeConfig cmdlet dodaje kondycję do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="4ef0a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ef0a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef0a-108">Przykład 1. Dodawanie kondycji do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4ef0a-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="4ef0a-109">To polecenie dodaje kondycję bramy aplikacji o nazwie Brama o nazwie Miszchaj1.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="4ef0a-110">To polecenie ustawia również próg złej kondycji na 8 ponownych prób i przekroczenie czasu po 120 sekundach.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="4ef0a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ef0a-111">PARAMETERS</span></span>

### <span data-ttu-id="4ef0a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef0a-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ef0a-113">Określa bramę aplikacji, do której to polecenie cmdlet dodaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="4ef0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef0a-114">-DefaultProfile</span></span>
<span data-ttu-id="4ef0a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef0a-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="4ef0a-116">-HostName</span></span>
<span data-ttu-id="4ef0a-117">Określa nazwę hosta, do których to polecenie cmdlet wysyła dane.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="4ef0a-118">- Interval</span><span class="sxs-lookup"><span data-stu-id="4ef0a-118">-Interval</span></span>
<span data-ttu-id="4ef0a-119">Określa interwał interwału w sekundach.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="4ef0a-120">Jest to interwał między dwoma kolejnymi przerwami.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="4ef0a-121">Ta wartość należy do 1 sekundy do 86 400 sekund.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4ef0a-122">— Dopasowanie</span><span class="sxs-lookup"><span data-stu-id="4ef0a-122">-Match</span></span>
<span data-ttu-id="4ef0a-123">Treść, która musi być zawarta w odpowiedzi na stan zdrowia.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="4ef0a-124">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="4ef0a-124">Default value is empty</span></span>

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

### <span data-ttu-id="4ef0a-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="4ef0a-125">-MinServers</span></span>
<span data-ttu-id="4ef0a-126">Minimalna liczba serwerów, które są zawsze oznaczone jako dobrej kondycji.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="4ef0a-127">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="4ef0a-127">Default value is 0</span></span>

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

### <span data-ttu-id="4ef0a-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ef0a-128">-Name</span></span>
<span data-ttu-id="4ef0a-129">Określa nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="4ef0a-130">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="4ef0a-130">-Path</span></span>
<span data-ttu-id="4ef0a-131">Określa ścieżkę względną.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="4ef0a-132">Prawidłowa ścieżka rozpoczyna się znakiem ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="4ef0a-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="4ef0a-133">Wiadomość jest wysyłana \<Protocol\> do: \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="4ef0a-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="4ef0a-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4ef0a-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="4ef0a-135">Czy nagłówek hosta powinien być wybierany z ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="4ef0a-136">Wartość domyślna ma wartość fałszywą</span><span class="sxs-lookup"><span data-stu-id="4ef0a-136">Default value is false</span></span>

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

### <span data-ttu-id="4ef0a-137">— Protokół</span><span class="sxs-lookup"><span data-stu-id="4ef0a-137">-Protocol</span></span>
<span data-ttu-id="4ef0a-138">Określa protokół używany do wysyłania wiadomości.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="4ef0a-139">To polecenie cmdlet obsługuje tylko protokół HTTP.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="4ef0a-140">— Limit czasu</span><span class="sxs-lookup"><span data-stu-id="4ef0a-140">-Timeout</span></span>
<span data-ttu-id="4ef0a-141">Określa limit czasu pobierania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="4ef0a-142">To polecenie cmdlet oznacza ten adres jako nieudany, jeśli z tym limitem czasu nie odebrano prawidłowej odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="4ef0a-143">Prawidłowe wartości to między 1 sekundą a 86 400 sekund.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4ef0a-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="4ef0a-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="4ef0a-145">Określa liczbę ponownych prób.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="4ef0a-146">Serwer zaplecza jest oznaczany w dół po osiągnięciu progu awarii systemu o złej kondycji.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="4ef0a-147">Prawidłowe wartości to między 1 sekundą a 20 sekundami.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="4ef0a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef0a-148">CommonParameters</span></span>
<span data-ttu-id="4ef0a-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef0a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef0a-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef0a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef0a-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ef0a-151">INPUTS</span></span>

### <span data-ttu-id="4ef0a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef0a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ef0a-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ef0a-153">OUTPUTS</span></span>

### <span data-ttu-id="4ef0a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef0a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ef0a-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ef0a-155">NOTES</span></span>

## <span data-ttu-id="4ef0a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ef0a-156">RELATED LINKS</span></span>

[<span data-ttu-id="4ef0a-157">Dodawanie pliku do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4ef0a-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="4ef0a-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4ef0a-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="4ef0a-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4ef0a-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="4ef0a-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4ef0a-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="4ef0a-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4ef0a-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

