---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055395"
---
# Set-AzureApplicationGatewayConfig

## STRESZCZENIe
Konfiguruje bramę aplikacji.

## POLECENIA

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureApplicationGatewayConfig** konfiguruje bramę aplikacji.

## Przykłady

### Przykład 1: Konfigurowanie bramy aplikacji przy użyciu obiektu konfiguracji
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

Pierwsze polecenie pobiera obiekt konfiguracji bramy Application Gateway o nazwie ApplicationGateway02 przy użyciu polecenia cmdlet **Get-AzureApplicationGatewayConfig** .
Polecenie zapisuje je w zmiennej $ConfigReturnObject.

Drugie polecenie ustawia konfigurację dla aplikacji o nazwie ApplicationGateway06 przy użyciu obiektu konfiguracji bramy aplikacji przechowywanego w zmiennej $ConfigReturnObject.

### Przykład 2: Konfigurowanie bramy aplikacji przy użyciu pliku konfiguracji
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

To polecenie ustawia konfigurację dla aplikacji o nazwie ApplicationGateway06 przy użyciu pliku konfiguracji bramy aplikacji w określonej lokalizacji.

### Przykład 3: modyfikowanie konfiguracji przy użyciu obiektu konfiguracji
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

Pierwsze polecenie pobiera obiekt konfiguracji bramy Application Gateway o nazwie ApplicationGateway06 przy użyciu polecenia cmdlet **Get-AzureApplicationGatewayConfig** .
Polecenie zapisuje je w zmiennej $ConfigReturnObject.

Drugie polecenie przypisuje wartość portu do właściwości **port** w obiekcie przechowywanym w $ConfigReturnObject.

Polecenie ostatnie przekazuje zaktualizowaną $ConfigReturnObject do bieżącego polecenia cmdlet.

## PARAMETRÓW

### -Config
Określa obiekt konfiguracji bramy aplikacji.
To polecenie cmdlet umożliwia przypisanie konfiguracji, którą ten parametr określa do bramy aplikacji.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigFile
Określa ścieżkę pliku konfiguracji w formacie XML dla bramy aplikacji.
To polecenie cmdlet umożliwia przypisanie konfiguracji, którą ten parametr określa do bramy aplikacji.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę bramy aplikacji, którą konfiguruje to polecenie cmdlet.

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## WYSYŁA

### Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


