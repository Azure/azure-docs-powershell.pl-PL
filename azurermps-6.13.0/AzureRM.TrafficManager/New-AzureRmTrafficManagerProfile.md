---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718566"
---
# New-AzureRmTrafficManagerProfile

## STRESZCZENIe
Tworzy profil w usłudze Traffic Manager.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmTrafficManagerProfile** tworzy profil usługi Azure Traffic Manager.
Określ parametr *name* oraz wymagane ustawienia.
To polecenie cmdlet zwraca obiekt lokalny reprezentujący nowy profil.

To polecenie cmdlet nie powoduje skonfigurowania punktów końcowych w usłudze Traffic Manager.
Obiekt profilu lokalnego można zaktualizować przy użyciu polecenia cmdlet Add-AzureRmTrafficManagerEndpointConfig.
Następnie Przekaż zmiany w usłudze Traffic Manager przy użyciu Set-AzureRmTrafficManagerProfile polecenia cmdlet.
Możesz też dodać punkty końcowe przy użyciu New-AzureRmTrafficManagerEndpoint polecenia cmdlet.

## Przykłady

### Przykład 1. Tworzenie profilu
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

To polecenie tworzy profil usługi Azure Traffic Manager o nazwie ContosoProfile w grupie zasób ResourceGroup11.
Nazwa FQDN DNS to contosoapp.trafficmanager.net.

## PARAMETRÓW

### -CustomHeader
Lista niestandardowych par nazw nagłówków i wartości dla żądań sondujące.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedStatusCodeRange
Lista oczekiwanych zakresów kodów stanu HTTP dla żądań sondujące.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxReturn
Maksymalna liczba odpowiedzi zwracanych w przypadku profilów przy użyciu metody routingu z wieloma wartościami.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorIntervalInSeconds
Interwał (w sekundach) sprawdzania kondycji poszczególnych punktów końcowych w tym profilu przez Menedżera ruchu. Wartość domyślna to 30.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPath
Określa ścieżkę używaną do monitorowania kondycji punktu końcowego.
Określ wartość odnoszącą się do nazwy domeny punktu końcowego.
Ta wartość musi zaczynać się od ukośnika (/).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPort
Określa port TCP, który jest wykorzystywany do monitorowania kondycji punktu końcowego.
Prawidłowe wartości to liczby całkowite z zakresu od 1 do 65535.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorProtocol
Określa protokół, który ma być używany do monitorowania kondycji punktu końcowego.
Prawidłowe wartości:

- URL
- HTTPS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorTimeoutInSeconds
Czas (w sekundach), w którym Menedżer ruchu umożliwia reagowanie punktów końcowych w tym profilu na kontrolę kondycji. Wartość domyślna to 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorToleratedNumberOfFailures
Liczba kolejnych nieprawidłowych testów kondycji, które czekają przed zadeklarowaniem punktu końcowego w tym profilu po następnym kolejnym sprawdzeniu kondycji. Wartość domyślna to 3.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę profilu usługi Traffic Managera, który tworzy polecenie cmdlet.

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

### -ProfileStatus
Określa stan profilu.
Prawidłowe wartości to: włączone i wyłączone.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RelativeDnsName
Określa względną nazwę DNS, jaką zapewnia dany profil usługi Traffic Manager.
Usługa Traffic Manager łączy tę wartość i nazwę domeny DNS używaną przez usługę Azure Traffic Manager do utworzenia w pełni kwalifikowanej nazwy domeny (FQDN) profilu.

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

### -ResourceGroupName
Określa nazwę grupy zasobów.
To polecenie cmdlet tworzy profil usługi Traffic Manager w grupie, którą ten parametr określa.

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

### -Tag
Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficRoutingMethod
Określa metodę routingu ruchu.
Ta metoda określa, który Menedżer ruchu punktu końcowego zwraca odpowiedź na przychodzące kwerendy DNS.
Prawidłowe wartości:

- Pracy
- Ważona
- Priorytet
- Geograficznego

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Określa wartość TTL (czas wygaśnięcia).

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
To polecenie cmdlet zwraca nowy obiekt TrafficManagerProfile.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Disable-AzureRmTrafficManagerProfile](./Disable-AzureRmTrafficManagerProfile.md)

[Enable-AzureRmTrafficManagerProfile](./Enable-AzureRmTrafficManagerProfile.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


