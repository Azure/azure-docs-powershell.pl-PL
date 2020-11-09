---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309193"
---
# New-AzNetworkWatcherConnectionMonitorObject

## STRESZCZENIe
Utwórz obiekt monitora połączenia w wersji 2.

## POLECENIA

### SetByResource
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByLocation
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorObject powoduje utworzenie obiektu monitorowanie połączenia w wersji 2.

## Przykłady

### Przykład 1
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }
        
   

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### — Lokalizacja
Lokalizacja obserwatora sieci.

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa monitora połączeń.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWatcher
Zasób obserwatora sieci.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWatcherName
Nazwa obserwatora sieci.

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uwaga
Notatki związane z monitorem połączeń.

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

### — Dane wyjściowe
Zawiera opis docelowych lokalizacji wyjściowych monitora połączeń.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów obserwatora sieci.

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Obiekt Hashtable reprezentujący znaczniki zasobów.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tester
Lista grup testowych.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorObject

## INFORMACYJN

## LINKI POKREWNE
