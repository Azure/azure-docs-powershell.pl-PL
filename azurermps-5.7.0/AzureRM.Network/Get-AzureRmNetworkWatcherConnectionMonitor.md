---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528086"
---
# Get-AzureRmNetworkWatcherConnectionMonitor

## STRESZCZENIe
Zwraca monitor połączenia z określoną nazwą lub z listą monitorów połączeń.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SetByName (domyślny)
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByLocation
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzureRmNetworkWatcherConnectionMonitor zwraca monitor połączenia z określoną nazwą/identyfikatorem zasobu lub listą monitorów połączeń odpowiadającą określonemu obserwatorowi/lokalizacji sieci.

## Przykłady

### Przykład 1: uzyskiwanie monitora połączeń według nazwy w określonej lokalizacji
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

W tym przykładzie monitor połączenia jest wyświetlany według nazwy w określonej lokalizacji.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### — Lokalizacja
Lokalizacja obserwatora sieci.

```yaml
Type: String
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
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWatcher
Zasób obserwatora sieci.

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NetworkWatcherName
Nazwa obserwatora sieci.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów obserwatora sieci.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu monitora połączeń.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.
Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSNetworkWatcher
System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia

## LINKI POKREWNE

[Nowe — AzureRmNetworkWatcher]()

[Get-AzureRmNetworkWatcher]()

[Remove-AzureRmNetworkWatcher]()

[Get-AzureRmNetworkWatcherNextHop]()

[Get-AzureRmNetworkWatcherSecurityGroupView]()

[Get-AzureRmNetworkWatcherTopology]()

[Get-AzureRmNetworkWatcherTroubleshootingResult]()

[Nowe — AzureRmNetworkWatcherPacketCapture]()

[Nowe — AzureRmPacketCaptureFilterConfig]()

[Get-AzureRmNetworkWatcherPacketCapture]()

[Remove-AzureRmNetworkWatcherPacketCapture]()

[Zatrzymaj — AzureRmNetworkWatcherPacketCapture]()

[Nowe — AzureRmNetworkWatcherConnectionMonitor]()

[Get-AzureRmNetworkWatcherConnectionMonitorReport]()

[Set-AzureRmNetworkWatcherConnectionMonitor]()

[Start — AzureRmNetworkWatcherConnectionMonitor]()

[Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor]()

[Remove-AzureRmNetworkWatcherConnectionMonitor]()
