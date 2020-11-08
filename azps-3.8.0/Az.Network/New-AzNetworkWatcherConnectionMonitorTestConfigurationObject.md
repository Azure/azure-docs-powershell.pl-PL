---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: f394d5aadb743f4439f3bda4cd5522f26f719516
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050757"
---
# <span data-ttu-id="2096e-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2096e-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="2096e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2096e-102">SYNOPSIS</span></span>
<span data-ttu-id="2096e-103">Tworzenie konfiguracji testu monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="2096e-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="2096e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2096e-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Int32>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2096e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2096e-105">DESCRIPTION</span></span>
<span data-ttu-id="2096e-106">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorTestConfigurationObject powoduje utworzenie konfiguracji testu monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="2096e-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="2096e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2096e-107">EXAMPLES</span></span>

### <span data-ttu-id="2096e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2096e-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="2096e-109">Nazwa: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443, "Metoda": "GET", "RequestHeaders": [{"nazwa": "dozwolone", "wartość": "GET"}], "ValidStatusCodeRanges": ["2xx", "300-308", "</span><span class="sxs-lookup"><span data-stu-id="2096e-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="2096e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2096e-110">PARAMETERS</span></span>

### <span data-ttu-id="2096e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2096e-111">-DefaultProfile</span></span>
<span data-ttu-id="2096e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2096e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2096e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2096e-113">-Name</span></span>
<span data-ttu-id="2096e-114">Nazwa konfiguracji testu monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="2096e-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="2096e-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="2096e-115">-PreferredIPVersion</span></span>
<span data-ttu-id="2096e-116">Preferowana wersja protokołu IP używana w ocenie testu.</span><span class="sxs-lookup"><span data-stu-id="2096e-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="2096e-117">Monitor połączenia może wybrać opcję używania innej wersji w zależności od innych parametrów.</span><span class="sxs-lookup"><span data-stu-id="2096e-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="2096e-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2096e-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="2096e-119">Parametry używane do przeprowadzania oceny testowej w ramach jakiegoś protokołu.</span><span class="sxs-lookup"><span data-stu-id="2096e-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="2096e-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="2096e-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="2096e-121">Maksymalny procent nieudanych kontroli dozwolonych dla testu, który może zostać oceniony jako pomyślny.</span><span class="sxs-lookup"><span data-stu-id="2096e-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="2096e-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="2096e-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="2096e-123">Maksymalny czas błądzenia w milisekundach, w którym test może zostać oceniony jako pomyślny.</span><span class="sxs-lookup"><span data-stu-id="2096e-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="2096e-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="2096e-124">-TestFrequencySec</span></span>
<span data-ttu-id="2096e-125">Częstotliwość oceny badania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="2096e-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="2096e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2096e-126">-Confirm</span></span>
<span data-ttu-id="2096e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2096e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2096e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2096e-128">-WhatIf</span></span>
<span data-ttu-id="2096e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2096e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2096e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2096e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2096e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2096e-131">CommonParameters</span></span>
<span data-ttu-id="2096e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2096e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2096e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2096e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2096e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2096e-134">INPUTS</span></span>

### <span data-ttu-id="2096e-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2096e-135">None</span></span>

## <span data-ttu-id="2096e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2096e-136">OUTPUTS</span></span>

### <span data-ttu-id="2096e-137">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2096e-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="2096e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2096e-138">NOTES</span></span>

## <span data-ttu-id="2096e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2096e-139">RELATED LINKS</span></span>
