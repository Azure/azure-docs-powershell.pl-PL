---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054901"
---
# Test-AzureTrafficManagerDomainName

## STRESZCZENIe
Sprawdza, czy nazwa domeny jest dostępna jako profil w usłudze Traffic Manager.

## POLECENIA

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **test-AzureTrafficManagerDomainName** sprawdza, czy nazwa domeny jest dostępna jako profil usługi Microsoft Azure Traffic Manager.
Jeśli nazwa domeny jest dostępna, to polecenie cmdlet zwraca wartość $True.

## Przykłady

### Przykład 1. Sprawdź, czy nazwa domeny jest dostępna
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

To polecenie sprawdza, czy nazwa domeny ContosoApp.trafficmanager.net jest dostępna jako profil usługi Traffic Manager.

## PARAMETRÓW

### -NazwaDomeny
Określa nazwę domeny do sprawdzenia.
Musisz podać następujący ciąg: 

. trafficmanager.net

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

## WYSYŁA

### System. Boolean
To polecenie cmdlet generuje $True lub $False.
Jeśli nazwa domeny jest dostępna, to polecenie cmdlet zwraca wartość $True.

## INFORMACYJN

## LINKI POKREWNE

