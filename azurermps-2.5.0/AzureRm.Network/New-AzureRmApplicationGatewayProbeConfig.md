---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 0e3c0c9a3f1c47163a28dc1732ef488f87014c63
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897309"
---
# <span data-ttu-id="fe219-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fe219-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fe219-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe219-102">SYNOPSIS</span></span>
<span data-ttu-id="fe219-103">Umożliwia utworzenie badania dotyczącego kondycji.</span><span class="sxs-lookup"><span data-stu-id="fe219-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe219-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe219-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe219-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe219-105">DESCRIPTION</span></span>
<span data-ttu-id="fe219-106">Polecenie cmdlet New-AzureRmApplicationGatewayProbeConfig powoduje utworzenie badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="fe219-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="fe219-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe219-107">EXAMPLES</span></span>

### <span data-ttu-id="fe219-108">Example1: Tworzenie badania dotyczącego kondycji</span><span class="sxs-lookup"><span data-stu-id="fe219-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="fe219-109">To polecenie powoduje utworzenie badania kondycji o nazwie Probe03, protokołu HTTP, interwału 30 sekund, limitu czasu 120 sekund oraz progu niezdrowego 8 prób.</span><span class="sxs-lookup"><span data-stu-id="fe219-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="fe219-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe219-110">PARAMETERS</span></span>

### <span data-ttu-id="fe219-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe219-111">-DefaultProfile</span></span>
<span data-ttu-id="fe219-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe219-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe219-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="fe219-113">-HostName</span></span>
<span data-ttu-id="fe219-114">Określa nazwę hosta, w którym to polecenie cmdlet wysyła sondę.</span><span class="sxs-lookup"><span data-stu-id="fe219-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="fe219-115">-Interval</span><span class="sxs-lookup"><span data-stu-id="fe219-115">-Interval</span></span>
<span data-ttu-id="fe219-116">Określa interwał sondy w sekundach.</span><span class="sxs-lookup"><span data-stu-id="fe219-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="fe219-117">Jest to odstęp czasu między dwiema kolejnymi sondami.</span><span class="sxs-lookup"><span data-stu-id="fe219-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="fe219-118">Ta wartość należy do zakresu od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="fe219-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fe219-119">-Match</span><span class="sxs-lookup"><span data-stu-id="fe219-119">-Match</span></span>
<span data-ttu-id="fe219-120">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="fe219-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="fe219-121">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="fe219-121">Default value is empty</span></span>

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

### <span data-ttu-id="fe219-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="fe219-122">-MinServers</span></span>
<span data-ttu-id="fe219-123">Minimalna liczba serwerów, które są zawsze oznaczone jako zdrowe.</span><span class="sxs-lookup"><span data-stu-id="fe219-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="fe219-124">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="fe219-124">Default value is 0</span></span>

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

### <span data-ttu-id="fe219-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe219-125">-Name</span></span>
<span data-ttu-id="fe219-126">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="fe219-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="fe219-127">-Path</span><span class="sxs-lookup"><span data-stu-id="fe219-127">-Path</span></span>
<span data-ttu-id="fe219-128">Określa względną ścieżkę sondy.</span><span class="sxs-lookup"><span data-stu-id="fe219-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="fe219-129">Prawidłowe ścieżki rozpoczynają się od znaku ukośnika (/).</span><span class="sxs-lookup"><span data-stu-id="fe219-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="fe219-130">Sonda jest wysyłana do \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="fe219-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="fe219-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fe219-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="fe219-132">Czy nagłówek hosta powinien być wybrany na podstawie ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="fe219-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="fe219-133">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="fe219-133">Default value is false</span></span>

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

### <span data-ttu-id="fe219-134">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="fe219-134">-Protocol</span></span>
<span data-ttu-id="fe219-135">Określa protokół używany do wysyłania sondy.</span><span class="sxs-lookup"><span data-stu-id="fe219-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="fe219-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="fe219-136">-Timeout</span></span>
<span data-ttu-id="fe219-137">Określa limit czasu badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="fe219-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="fe219-138">To polecenie cmdlet oznacza, że sonda nie powiodła się, jeśli nie otrzymano prawidłowej odpowiedzi z tym limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="fe219-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="fe219-139">Prawidłowe wartości należą do przedziału od 1 sekundy do 86400 sekund.</span><span class="sxs-lookup"><span data-stu-id="fe219-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fe219-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="fe219-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="fe219-141">Określa liczbę ponownych prób sondowania.</span><span class="sxs-lookup"><span data-stu-id="fe219-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="fe219-142">Serwer wewnętrznej bazy danych jest oznaczony jako wyłączony po upływie progu liczby błędów sondy w niezdrowym stanie.</span><span class="sxs-lookup"><span data-stu-id="fe219-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="fe219-143">Prawidłowe wartości należą do przedziału od 1 sekundy do 20 sekund.</span><span class="sxs-lookup"><span data-stu-id="fe219-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="fe219-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe219-144">CommonParameters</span></span>
<span data-ttu-id="fe219-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe219-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe219-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe219-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe219-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe219-147">INPUTS</span></span>

## <span data-ttu-id="fe219-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe219-148">OUTPUTS</span></span>

### <span data-ttu-id="fe219-149">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="fe219-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="fe219-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe219-150">NOTES</span></span>

## <span data-ttu-id="fe219-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe219-151">RELATED LINKS</span></span>

[<span data-ttu-id="fe219-152">Tworzenie niestandardowej funkcji sondowania bramy Application Manager za pomocą programu PowerShell dla Menedżera zasobów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe219-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="fe219-153">Dodaj-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fe219-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fe219-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fe219-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fe219-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fe219-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fe219-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fe219-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

