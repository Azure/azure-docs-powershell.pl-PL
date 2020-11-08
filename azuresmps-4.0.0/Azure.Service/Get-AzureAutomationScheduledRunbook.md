---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055323"
---
# Get-AzureAutomationScheduledRunbook

## STRESZCZENIe

Pobiera elementy Runbook usługi Azure Automation i skojarzone harmonogramy.

## POLECENIA

### ByAll (domyślny)
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Funkcja **Get-AzureAutomationScheduledRunbook** pobiera jeden lub więcej elementów Runbook usługi Azure Automation oraz skojarzonych z nimi harmonogramów.
Domyślnie zostaną zwrócone wszystkie zaplanowane elementy Runbook.

Aby uzyskać określony zaplanowany element Runbook, określ nazwę elementu Runbook i nazwę harmonogramu.
Aby uzyskać wszystkie harmonogramy skojarzone z elementem Runbook, określ tylko nazwę elementu Runbook.
Aby uzyskać wszystkie elementy Runbook skojarzone z harmonogramem, określ tylko nazwę harmonogramu.

## Przykłady

### Przykład 1: pobieranie wszystkich zaplanowanych elementów Runbook
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

To polecenie pobiera wszystkie zaplanowane elementy Runbook z konta usługi Automation o nazwie Contoso17.

### Przykład 2: pobieranie wszystkich harmonogramów skojarzonych z elementem Runbook
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

To polecenie pobiera wszystkie zaplanowane elementy Runbook dla elementu Runbook Runbk01 na koncie usługi Automation o nazwie Contoso17.

### Przykład 3: pobieranie wszystkich elementów Runbook skojarzonych z harmonogramem
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

To polecenie pobiera wszystkie zaplanowane elementy Runbook dla Schedule01 harmonogram na koncie automatyzacji o nazwie Contoso17.

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

### -JobScheduleId
Określa identyfikator zaplanowanego zadania.

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
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

### -Element runbookname
Określa nazwę elementu Runbook.

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Określa nazwę harmonogramu.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. JobSchedule

## INFORMACYJN

## LINKI POKREWNE

[Rejestr — AzureAutomationScheduledRunbook](./Register-AzureAutomationScheduledRunbook.md)

[Wyrejestrowanie — AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


