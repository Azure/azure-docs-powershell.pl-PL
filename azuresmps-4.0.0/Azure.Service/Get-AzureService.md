---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055275"
---
# Get-AzureService

## STRESZCZENIe
Zwraca obiekt z informacją o usługach w chmurze dla bieżącej subskrypcji.

## POLECENIA

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureService** zwraca obiekt listy ze wszystkimi usługami usługi Azure Cloud skojarzonymi z bieżącą subskrypcją.
Jeśli określisz parametr *ServiceName* , funkcja **Get-AzureService** zwraca informacje dotyczące tylko usługi zgodnej.

## Przykłady

### Przykład 1: uzyskiwanie informacji o wszystkich usługach
```
PS C:\> Get-AzureService
```

To polecenie zwraca obiekt zawierający informacje dotyczące wszystkich usług platformy Azure skojarzonych z bieżącą subskrypcją.

### Przykład 2: uzyskiwanie informacji o określonej usłudze
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

To polecenie zwraca informacje o usłudze $MySvc.

### Przykład 3: wyświetlanie dostępnych metod i właściwości
```
PS C:\> Get-AzureService | Get-Member
```

To polecenie wyświetla właściwości i metody dostępne w polecenia cmdlet **Get-AzureService** .

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
Określa nazwę usługi, na której należy zwrócić informacje.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### HostedServiceContext

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


