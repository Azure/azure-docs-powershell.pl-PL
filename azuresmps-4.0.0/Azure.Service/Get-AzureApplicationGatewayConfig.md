---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054631"
---
# Get-AzureApplicationGatewayConfig

## STRESZCZENIe
Pobiera kontekst konfiguracji bramy aplikacji.

## POLECENIA

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureApplicationGatewayConfig umożliwia pobranie** kontekstu konfiguracji bramy aplikacji platformy Azure.
Kontekst obejmuje zarówno obiekt konfiguracji, jak i konfigurację XML.
Możesz zapisać konfigurację XML w pliku.

## Przykłady

### Przykład 1: pobranie konfiguracji bramy aplikacji i zapisanie jej w pliku
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

To polecenie pobiera konfigurację bramy Application Gateway o nazwie ApplicationGateway06.
Polecenie zapisuje je w pliku w określonej ścieżce.

## PARAMETRÓW

### -ExportToFile
Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje konfigurację w formacie XML.

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

### -Name (nazwa)
Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera informacje o konfiguracji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## WYSYŁA

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


