---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 75688743c03db16c9683b84698ad41ddcb7fa52e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709363"
---
# <span data-ttu-id="71c11-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c11-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="71c11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71c11-102">SYNOPSIS</span></span>
<span data-ttu-id="71c11-103">Umożliwia utworzenie badania dotyczącego kondycji.</span><span class="sxs-lookup"><span data-stu-id="71c11-103">Creates a health probe.</span></span>

## <span data-ttu-id="71c11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71c11-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71c11-105">DESCRIPTION</span></span>
<span data-ttu-id="71c11-106">Polecenie cmdlet New-AzApplicationGatewayProbeConfig powoduje utworzenie badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="71c11-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="71c11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71c11-107">EXAMPLES</span></span>

### <span data-ttu-id="71c11-108">Example1: Tworzenie badania dotyczącego kondycji</span><span class="sxs-lookup"><span data-stu-id="71c11-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="71c11-109">To polecenie powoduje utworzenie badania kondycji o nazwie Probe03, protokołu HTTP, interwału 30 sekund, limitu czasu 120 sekund oraz progu niezdrowego 8 prób.</span><span class="sxs-lookup"><span data-stu-id="71c11-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="71c11-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71c11-110">PARAMETERS</span></span>

### <span data-ttu-id="71c11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c11-111">-DefaultProfile</span></span>
<span data-ttu-id="71c11-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71c11-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c11-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="71c11-113">-HostName</span></span>
<span data-ttu-id="71c11-114">Określa nazwę hosta, w którym to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="71c11-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="71c11-115">-Interval</span><span class="sxs-lookup"><span data-stu-id="71c11-115">-Interval</span></span>
<span data-ttu-id="71c11-116">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="71c11-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="71c11-117">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="71c11-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="71c11-118">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="71c11-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="71c11-119">-Match</span><span class="sxs-lookup"><span data-stu-id="71c11-119">-Match</span></span>
<span data-ttu-id="71c11-120">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="71c11-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="71c11-121">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="71c11-121">Default value is empty</span></span>

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

### <span data-ttu-id="71c11-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="71c11-122">-MinServers</span></span>
<span data-ttu-id="71c11-123">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="71c11-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="71c11-124">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="71c11-124">Default value is 0</span></span>

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

### <span data-ttu-id="71c11-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71c11-125">-Name</span></span>
<span data-ttu-id="71c11-126">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="71c11-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="71c11-127">-Path</span><span class="sxs-lookup"><span data-stu-id="71c11-127">-Path</span></span>
<span data-ttu-id="71c11-128">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="71c11-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="71c11-129">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="71c11-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="71c11-130">Sonda jest wysyłana do \< protokołu \> :// \< hosta \> : \< ścieżka portu \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="71c11-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="71c11-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="71c11-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="71c11-132">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="71c11-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="71c11-133">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="71c11-133">Default value is false</span></span>

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

### <span data-ttu-id="71c11-134">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="71c11-134">-Protocol</span></span>
<span data-ttu-id="71c11-135">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="71c11-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="71c11-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="71c11-136">-Timeout</span></span>
<span data-ttu-id="71c11-137">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="71c11-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="71c11-138">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="71c11-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="71c11-139">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="71c11-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="71c11-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="71c11-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="71c11-141">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="71c11-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="71c11-142">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="71c11-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="71c11-143">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="71c11-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="71c11-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c11-144">CommonParameters</span></span>
<span data-ttu-id="71c11-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c11-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c11-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c11-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c11-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71c11-147">INPUTS</span></span>

### <span data-ttu-id="71c11-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71c11-148">None</span></span>

## <span data-ttu-id="71c11-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71c11-149">OUTPUTS</span></span>

### <span data-ttu-id="71c11-150">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="71c11-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="71c11-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71c11-151">NOTES</span></span>

## <span data-ttu-id="71c11-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71c11-152">RELATED LINKS</span></span>

[<span data-ttu-id="71c11-153">Tworzenie niestandardowej funkcji sondowania bramy Application Manager za pomocą programu PowerShell dla Menedżera zasobów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="71c11-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="71c11-154">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c11-154">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="71c11-155">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c11-155">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="71c11-156">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c11-156">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="71c11-157">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c11-157">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

