---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: e6caf36980fc6b103b77640a174b001c6067bf61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491018"
---
# New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject

## STRESZCZENIe
Tworzenie konfiguracji protokołu używanej do przeprowadzania oceny testowej przez protokoły TCP, HTTP lub ICMP.

## POLECENIA

### PROTOKOŁ
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <UInt16>
 [-DisableTraceRoute] [-DestinationPortBehavior <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### URL
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <UInt16>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Internetem
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject umożliwia utworzenie konfiguracji protokołu służącej do przeprowadzania oceny testowej przez protokoły TCP, HTTP lub ICMP.

## Przykłady

### Przykład 1
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

Port: 80 DisableTraceRoute: FAŁSZ

### Przykład 2

Tworzenie konfiguracji protokołu używanej do przeprowadzania oceny testowej przez protokoły TCP, HTTP lub ICMP. (autogenerowana)

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -IcmpProtocol
```

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

### -DestinationPortBehavior
Zachowanie portów docelowych.
Obsługiwane wartości to None, ListenIfAvailable.

```yaml
Type: System.String
Parameter Sets: TCP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableTraceRoute
Wartość wskazująca, czy ocena ścieżki z marszrutą śledzenia powinna być wyłączona.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpProtocol
Przełącznik protokołu HTTP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IcmpProtocol
Przełącznik protokołu ICMP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
Metoda HTTP, która ma zostać użyta.

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Składnik ścieżki identyfikatora URI.
Na przykład "/dir1/dir2".

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
Port, z którym ma zostać nawiązane połączenie.

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferHTTPS
Wartość wskazująca, czy protokół HTTPS jest preferowany za pośrednictwem protokołu HTTP w przypadkach, gdy wybór jest niejawny.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestHeader
Nagłówki HTTP do przesłania z żądaniem.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TcpProtocol
Przełącznik protokołu TCP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidStatusCodeRange
Kody stanu HTTP, które powinny zostać rozpatrzone powodzeniem.
Na przykład "2xx, 301-304418".

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

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

### Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorTcpConfiguration

### Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorHttpConfiguration

### Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorIcmpConfiguration

## INFORMACYJN

## LINKI POKREWNE
