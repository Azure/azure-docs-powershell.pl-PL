---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 16499dfb72f973169769c35cd1ba427eba52fd0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053763"
---
# <span data-ttu-id="e9b07-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9b07-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e9b07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9b07-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b07-103">Umożliwia utworzenie badania dotyczącego kondycji.</span><span class="sxs-lookup"><span data-stu-id="e9b07-103">Creates a health probe.</span></span>

## <span data-ttu-id="e9b07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9b07-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-Port <Int32>]
```

## <span data-ttu-id="e9b07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9b07-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b07-106">Polecenie cmdlet New-AzApplicationGatewayProbeConfig powoduje utworzenie badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="e9b07-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="e9b07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9b07-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b07-108">Example1: Tworzenie badania dotyczącego kondycji</span><span class="sxs-lookup"><span data-stu-id="e9b07-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e9b07-109">To polecenie powoduje utworzenie badania kondycji o nazwie Probe03, protokołu HTTP, interwału 30 sekund, limitu czasu 120 sekund oraz progu niezdrowego 8 prób.</span><span class="sxs-lookup"><span data-stu-id="e9b07-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="e9b07-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9b07-110">PARAMETERS</span></span>

### <span data-ttu-id="e9b07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b07-111">-DefaultProfile</span></span>
<span data-ttu-id="e9b07-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b07-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="e9b07-113">-HostName</span></span>
<span data-ttu-id="e9b07-114">Określa nazwę hosta, w którym to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="e9b07-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="e9b07-115">-Interval</span><span class="sxs-lookup"><span data-stu-id="e9b07-115">-Interval</span></span>
<span data-ttu-id="e9b07-116">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="e9b07-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e9b07-117">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="e9b07-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e9b07-118">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="e9b07-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e9b07-119">-Match</span><span class="sxs-lookup"><span data-stu-id="e9b07-119">-Match</span></span>
<span data-ttu-id="e9b07-120">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="e9b07-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e9b07-121">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="e9b07-121">Default value is empty</span></span>

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

### <span data-ttu-id="e9b07-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e9b07-122">-MinServers</span></span>
<span data-ttu-id="e9b07-123">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="e9b07-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e9b07-124">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="e9b07-124">Default value is 0</span></span>

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

### <span data-ttu-id="e9b07-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9b07-125">-Name</span></span>
<span data-ttu-id="e9b07-126">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="e9b07-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e9b07-127">-Path</span><span class="sxs-lookup"><span data-stu-id="e9b07-127">-Path</span></span>
<span data-ttu-id="e9b07-128">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="e9b07-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e9b07-129">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="e9b07-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="e9b07-130">Sonda jest wysyłana do \< protokołu \> :// \< hosta \> : \< ścieżka portu \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="e9b07-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e9b07-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e9b07-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e9b07-132">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e9b07-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e9b07-133">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="e9b07-133">Default value is false</span></span>

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

### <span data-ttu-id="e9b07-134">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e9b07-134">-Protocol</span></span>
<span data-ttu-id="e9b07-135">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="e9b07-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="e9b07-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e9b07-136">-Timeout</span></span>
<span data-ttu-id="e9b07-137">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="e9b07-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e9b07-138">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="e9b07-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e9b07-139">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="e9b07-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e9b07-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e9b07-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="e9b07-141">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="e9b07-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="e9b07-142">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="e9b07-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e9b07-143">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="e9b07-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e9b07-144">-Port</span><span class="sxs-lookup"><span data-stu-id="e9b07-144">-Port</span></span>
<span data-ttu-id="e9b07-145">Określa port służący do obsługi serwerów zaplecza sondowania.</span><span class="sxs-lookup"><span data-stu-id="e9b07-145">Specifies the port used for probing backend servers.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe

## NOTES

## RELATED LINKS

[Create custom probe for Application Gateway using PowerShell for Azure Resource Manager](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

