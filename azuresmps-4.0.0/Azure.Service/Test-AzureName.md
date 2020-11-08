---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054903"
---
# Test-AzureName

## STRESZCZENIe
Sprawdza, czy istnieje nazwa obszaru nazw usługi w chmurze platformy Microsoft Azure, nazwa usługi Storage lub Magistrala usług.

## POLECENIA

### Służby
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Chowan
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Firmy
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Jeśli nazwa istnieje, polecenie cmdlet zwraca $True.
Jeśli ta nazwa nie istnieje, zwracana jest $False.

## Przykłady

### Przykład 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

To polecenie umożliwia sprawdzenie, czy nazwa "MyNameService1" jest istniejącą nazwą usługi w chmurze platformy Microsoft Azure.

### Przykład 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

To polecenie sprawdza, czy nazwa "mystorename1" jest istniejącą nazwą usługi magazynu platformy Microsoft Azure.

### Przykład 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

To polecenie sprawdza, czy "Moja przestrzeń nazw" jest istniejącą nazwą przestrzeni nazw usługi Microsoft Azure Service Bus.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę konta usługi lub magazynu do przetestowania.

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

### -Service
Określa, że należy przetestować istniejące konto usługi.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Określa, że należy przetestować istniejący obszar nazw usługi Service Bus.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storage
Określa, że należy przetestować istniejące konto magazynu.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Witryna sieci Web
Określa, że należy testować istniejącą witrynę sieci Web.

```yaml
Type: SwitchParameter
Parameter Sets: Website
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

## WYSYŁA

## INFORMACYJN
* węzły — dev, php — dev, Python — dev

## LINKI POKREWNE

