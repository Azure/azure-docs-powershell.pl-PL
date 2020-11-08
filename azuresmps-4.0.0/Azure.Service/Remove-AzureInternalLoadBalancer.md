---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055441"
---
# Remove-AzureInternalLoadBalancer

## STRESZCZENIe
Umożliwia usunięcie konfiguracji wewnętrznego modułu równoważenia obciążenia.

## POLECENIA

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureInternalLoadBalancer** umożliwia usunięcie konfiguracji wewnętrznego modułu równoważenia obciążenia z usługi platformy Azure.
Jeśli jakiś punkt końcowy odwołuje się obecnie do wewnętrznego modułu równoważenia obciążenia, to polecenie cmdlet nie może usunąć konfiguracji.

## Przykłady

### Przykład 1: Usuwanie konfiguracji wewnętrznego modułu równoważenia obciążenia
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

To polecenie powoduje usunięcie konfiguracji wewnętrznego modułu równoważenia obciążenia dla usługi o nazwie ContosoService.

## PARAMETRÓW

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -ServiceName
Określa nazwę usługi, z poziomu której to polecenie cmdlet powoduje usunięcie wewnętrznego modułu równoważenia obciążenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureInternalLoadBalancer](./Add-AzureInternalLoadBalancer.md)

[Get-AzureInternalLoadBalancer](./Get-AzureInternalLoadBalancer.md)

[Nowe — AzureInternalLoadBalancerConfig](./New-AzureInternalLoadBalancerConfig.md)

[Set-AzureInternalLoadBalancer](./Set-AzureInternalLoadBalancer.md)


