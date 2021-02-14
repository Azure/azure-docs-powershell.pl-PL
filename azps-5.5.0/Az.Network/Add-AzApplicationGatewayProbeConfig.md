---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189978"
---
# <span data-ttu-id="f0e06-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f0e06-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f0e06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0e06-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e06-103">Dodaje kondycję do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f0e06-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="f0e06-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0e06-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0e06-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0e06-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e06-106">Polecenie Add-AzApplicationGatewayProbeConfig cmdlet dodaje kondycję do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f0e06-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="f0e06-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0e06-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e06-108">Przykład 1. Dodawanie kondycji do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f0e06-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="f0e06-109">To polecenie dodaje kondycję bramy aplikacji o nazwie Brama o nazwie Miszchaj1.</span><span class="sxs-lookup"><span data-stu-id="f0e06-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="f0e06-110">To polecenie ustawia również próg złej kondycji na 8 ponownych prób i przekroczenie czasu po 120 sekundach.</span><span class="sxs-lookup"><span data-stu-id="f0e06-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="f0e06-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0e06-111">PARAMETERS</span></span>

### <span data-ttu-id="f0e06-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0e06-112">-ApplicationGateway</span></span>
<span data-ttu-id="f0e06-113">Określa bramę aplikacji, do której to polecenie cmdlet dodaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="f0e06-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="f0e06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e06-114">-DefaultProfile</span></span>
<span data-ttu-id="f0e06-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0e06-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="f0e06-116">-HostName</span></span>
<span data-ttu-id="f0e06-117">Określa nazwę hosta, do których to polecenie cmdlet wysyła dane.</span><span class="sxs-lookup"><span data-stu-id="f0e06-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="f0e06-118">- Interval</span><span class="sxs-lookup"><span data-stu-id="f0e06-118">-Interval</span></span>
<span data-ttu-id="f0e06-119">Określa interwał interwału w sekundach.</span><span class="sxs-lookup"><span data-stu-id="f0e06-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="f0e06-120">Jest to interwał między dwoma kolejnymi przerwami.</span><span class="sxs-lookup"><span data-stu-id="f0e06-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="f0e06-121">Ta wartość należy do 1 sekundy do 86 400 sekund.</span><span class="sxs-lookup"><span data-stu-id="f0e06-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f0e06-122">— Dopasowanie</span><span class="sxs-lookup"><span data-stu-id="f0e06-122">-Match</span></span>
<span data-ttu-id="f0e06-123">Treść, która musi znajdować się w odpowiedzi na stan zdrowia.</span><span class="sxs-lookup"><span data-stu-id="f0e06-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f0e06-124">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="f0e06-124">Default value is empty</span></span>

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

### <span data-ttu-id="f0e06-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="f0e06-125">-MinServers</span></span>
<span data-ttu-id="f0e06-126">Minimalna liczba serwerów, które są zawsze oznaczone jako dobrej kondycji.</span><span class="sxs-lookup"><span data-stu-id="f0e06-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="f0e06-127">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="f0e06-127">Default value is 0</span></span>

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

### <span data-ttu-id="f0e06-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f0e06-128">-Name</span></span>
<span data-ttu-id="f0e06-129">Określa nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="f0e06-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="f0e06-130">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="f0e06-130">-Path</span></span>
<span data-ttu-id="f0e06-131">Określa względną ścieżkę ścieżki.</span><span class="sxs-lookup"><span data-stu-id="f0e06-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="f0e06-132">Prawidłowa ścieżka rozpoczyna się znakiem ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="f0e06-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="f0e06-133">Wiadomość jest wysyłana \<Protocol\> do: \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="f0e06-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="f0e06-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f0e06-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="f0e06-135">Czy nagłówek hosta powinien być wybierany z ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f0e06-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="f0e06-136">Wartość domyślna ma wartość fałszywą</span><span class="sxs-lookup"><span data-stu-id="f0e06-136">Default value is false</span></span>

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

### <span data-ttu-id="f0e06-137">— Protokół</span><span class="sxs-lookup"><span data-stu-id="f0e06-137">-Protocol</span></span>
<span data-ttu-id="f0e06-138">Określa protokół używany do wysyłania wiadomości.</span><span class="sxs-lookup"><span data-stu-id="f0e06-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="f0e06-139">To polecenie cmdlet obsługuje tylko protokół HTTP.</span><span class="sxs-lookup"><span data-stu-id="f0e06-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="f0e06-140">— Limit czasu</span><span class="sxs-lookup"><span data-stu-id="f0e06-140">-Timeout</span></span>
<span data-ttu-id="f0e06-141">Określa limit czasu pracy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="f0e06-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="f0e06-142">To polecenie cmdlet oznacza ten czas jako nieudany, jeśli z tym limitem czasu nie odebrano prawidłowej odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="f0e06-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="f0e06-143">Prawidłowe wartości to między 1 s a 86 400 sekund.</span><span class="sxs-lookup"><span data-stu-id="f0e06-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f0e06-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="f0e06-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="f0e06-145">Określa liczbę ponownych prób.</span><span class="sxs-lookup"><span data-stu-id="f0e06-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="f0e06-146">Serwer zaplecza jest oznaczany w dół po osiągnięciu progu awarii systemu o złej kondycji.</span><span class="sxs-lookup"><span data-stu-id="f0e06-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="f0e06-147">Prawidłowe wartości to między 1 sekundą a 20 sekundami.</span><span class="sxs-lookup"><span data-stu-id="f0e06-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="f0e06-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e06-148">CommonParameters</span></span>
<span data-ttu-id="f0e06-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e06-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e06-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e06-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e06-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0e06-151">INPUTS</span></span>

### <span data-ttu-id="f0e06-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0e06-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0e06-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0e06-153">OUTPUTS</span></span>

### <span data-ttu-id="f0e06-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0e06-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0e06-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0e06-155">NOTES</span></span>

## <span data-ttu-id="f0e06-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0e06-156">RELATED LINKS</span></span>

[<span data-ttu-id="f0e06-157">Dodawanie pliku do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f0e06-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="f0e06-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f0e06-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f0e06-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f0e06-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f0e06-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f0e06-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f0e06-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f0e06-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

