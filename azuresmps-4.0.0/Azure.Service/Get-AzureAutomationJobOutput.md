---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054624"
---
# Get-AzureAutomationJobOutput

## STRESZCZENIe

Pobiera dane wyjściowe zadania usługi Azure Automation.

## POLECENIA

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Polecenie cmdlet **Get-AzureAutomationJobOutput** pobiera dane wyjściowe zadania automatyzacji platformy Microsoft Azure.

## Przykłady

### Przykład 1. Pobieranie danych wyjściowych zadania usługi Azure Automation
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

To polecenie pobiera wszystkie dane wyjściowe zadania o określonym IDENTYFIKATORze.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta usługi Azure Automation.

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

### -ID
Określa identyfikator zadania.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

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

### -StartTime
Określa godzinę rozpoczęcia.

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stream
Określa typ danych wyjściowych.
Prawidłowe wartości: 

- Jakieś
- Wykrywanie
- Błędów
- Prowadzone
- Okres
- Pełne
- Ostrzeżenie

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureAutomationJob](./Get-AzureAutomationJob.md)

[Życiorys — AzureAutomationJob](./Resume-AzureAutomationJob.md)

[Zatrzymaj — AzureAutomationJob](./Stop-AzureAutomationJob.md)

[Suspend — AzureAutomationJob](./Suspend-AzureAutomationJob.md)


