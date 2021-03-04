---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: 542a207e60e451d97ba5edcbdccc45b84b14f760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958433"
---
# <span data-ttu-id="4cb4d-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4cb4d-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="4cb4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb4d-103">Utwórz konfigurację testu monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="4cb4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cb4d-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cb4d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cb4d-105">DESCRIPTION</span></span>
<span data-ttu-id="4cb4d-106">Polecenie New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet tworzy konfigurację testu monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="4cb4d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cb4d-107">EXAMPLES</span></span>

### <span data-ttu-id="4cb4d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4cb4d-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="4cb4d-109">Nazwa: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: { "Port": 443, "Metoda": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold: { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="4cb4d-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="4cb4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cb4d-110">PARAMETERS</span></span>

### <span data-ttu-id="4cb4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb4d-111">-DefaultProfile</span></span>
<span data-ttu-id="4cb4d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cb4d-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cb4d-113">-Name</span></span>
<span data-ttu-id="4cb4d-114">Nazwa konfiguracji testowej monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="4cb4d-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="4cb4d-115">-PreferredIPVersion</span></span>
<span data-ttu-id="4cb4d-116">Preferowana wersja protokołu IP do używania podczas oceny testowej.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="4cb4d-117">Monitor połączenia może zdecydować się na użycie innej wersji w zależności od innych parametrów.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="4cb4d-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cb4d-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="4cb4d-119">Parametry używane do przeprowadzania oceny testowej w pewnym protokole.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb4d-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="4cb4d-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="4cb4d-121">Maksymalna wartość procentowa testów, które zakończyły się niepowodzeniem, może zostać oceniona jako pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb4d-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="4cb4d-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="4cb4d-123">Maksymalny czas rundy (w milisekundach) dozwolony w celu oceny testu jako pomyślnego.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb4d-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="4cb4d-124">-TestFrequencySec</span></span>
<span data-ttu-id="4cb4d-125">Częstotliwość testowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb4d-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cb4d-126">-Confirm</span></span>
<span data-ttu-id="4cb4d-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb4d-128">-WhatIf</span></span>
<span data-ttu-id="4cb4d-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cb4d-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb4d-131">CommonParameters</span></span>
<span data-ttu-id="4cb4d-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb4d-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cb4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb4d-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cb4d-134">INPUTS</span></span>

### <span data-ttu-id="4cb4d-135">Brak</span><span class="sxs-lookup"><span data-stu-id="4cb4d-135">None</span></span>

## <span data-ttu-id="4cb4d-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cb4d-136">OUTPUTS</span></span>

### <span data-ttu-id="4cb4d-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4cb4d-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="4cb4d-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cb4d-138">NOTES</span></span>

## <span data-ttu-id="4cb4d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cb4d-139">RELATED LINKS</span></span>
