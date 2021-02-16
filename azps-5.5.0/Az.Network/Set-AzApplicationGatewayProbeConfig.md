---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 4ab021e36502c14e5cec66ae83c5612961500271
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191650"
---
# Set-AzApplicationGatewayProbeConfig

## SYNOPSIS
Ustawia konfigurację kondycji istniejącej bramy aplikacji.

## SKŁADNIA

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie Set-AzApplicationGatewayProbeConfig ustawia konfigurację kondycji istniejącej bramy aplikacji.

## PRZYKŁADY

### Przykład 1. Ustawianie konfiguracji kondycji bramy aplikacji
```powershell
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

To polecenie ustawia konfigurację dla pliku o nazwie Kondycja 05 dla bramy aplikacji o nazwie Brama.
To polecenie ustawia również próg złej kondycji na 8 ponownych prób i przekroczenie czasu po 120 sekundach.

### Przykład 2

Ustawia konfigurację kondycji istniejącej bramy aplikacji. (wygenerowane automatycznie)

<!-- Aladdin Generated Example -->
```powershell
Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Interval 30 -Match <PSApplicationGatewayProbeHealthResponseMatch> -Name 'Probe05' -Path '/path/custompath.htm' -PickHostNameFromBackendHttpSettings -Protocol https -Timeout 120 -UnhealthyThreshold 8
```

## PARAMETERS

### - ApplicationGateway
Określa bramę aplikacji, do której to polecenie cmdlet wysyła wiadomość.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -HostName
Określa nazwę hosta, do których to polecenie cmdlet wysyła dane.

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

### - Interval
Określa interwał interwału interwału w sekundach.
Jest to interwał między dwoma kolejnymi przerwami.
Ta wartość należy do 1 sekundy do 86 400 sekund.

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

### — Dopasowanie
Treść, która musi znajdować się w odpowiedzi na stan zdrowia.
Wartość domyślna jest pusta

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

### - MinServers
Minimalna liczba serwerów, które są zawsze oznaczone jako dobrej kondycji.
Wartość domyślna to 0

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

### — Nazwa
Określa nazwę pliku.

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

### — Ścieżka
Określa względną ścieżkę ścieżki.
Prawidłowe ścieżki zaczynają się od znaku ukośnika (/).
Wiadomość jest wysyłana \<Protocol\> do: \<host\> \<port\> \<path\> .

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

### -PickHostNameFromBackendHttpSettings
Czy nagłówek hosta powinien być wybierany z ustawień http zaplecza.
Wartość domyślna ma wartość fałszywą

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

### — Protokół
Określa protokół używany do wysyłania wiadomości.

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

### — Limit czasu
Określa limit czasu pracy w sekundach.
To polecenie cmdlet oznacza ten adres jako nieudany, jeśli z tym limitem czasu nie odebrano prawidłowej odpowiedzi.
Prawidłowe wartości to między 1 s a 86 400 sekund.

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

### -UnhealthyThreshold
Określa liczbę ponownych prób.
Serwer zaplecza jest oznaczany w dół po osiągnięciu progu awarii systemu o złej kondycji.
Prawidłowe wartości to między 1 sekundą a 20 sekundami.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTATKI

## LINKI POKREWNE

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[New-AzApplicationGatewayProbeConfig](./New-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

