---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528282"
---
# New-AzureRmBackupRetentionPolicyObject

## STRESZCZENIe
Tworzy zasady przechowywania kopii zapasowej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmBackupRetentionPolicyObject** tworzy zasady przechowywania kopii zapasowej platformy Azure.
Zasady przechowywania określają, jak długo kopia zapasowa zachowuje punkt odzyskiwania.
Typy przechowywania są następujące: 

- Dobow 
- Weekly 
- Podstaw 
- Roczny 

Tworzenie jednej zasady przechowywania dla każdego typu retencji, który ma zostać użyty.

Zasady tworzenia kopii zapasowych są skojarzone z co najmniej jednym zasadami przechowywania.
Aby utworzyć zasady tworzenia kopii zapasowych, użyj polecenia cmdlet New-AzureRmBackupProtectionPolicy.
Możesz zamiast tego podać zasady przechowywania dla Enable-AzureRmBackupProtection polecenia cmdlet.

## Przykłady

### Przykład 1: Tworzenie zasad przechowywania do codziennego przechowywania
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

Pierwsze polecenie tworzy zasady przechowywania przez 30 dni codziennego przechowywania, a następnie zapisuje je w zmiennej $Daily.

Drugie polecenie wyświetla zawartość $Daily.

### Przykład 2: Tworzenie miesięcznych zasad przechowywania
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

Pierwsze polecenie tworzy zasady przechowywania, które przechowują kopię zapasową w dziesiątym i dwudziestym dniu każdego miesiąca przez dwanaście miesięcy.
Polecenie przechowuje zasady przechowywania w zmiennej $Monthly.

Drugie polecenie wyświetla zawartość $Monthly.

## PARAMETRÓW

### -DailyRetention
Wskazuje, że to polecenie cmdlet tworzy codzienne zasady przechowywania.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
Określa dni miesiąca, w których należy określić, że kopie zapasowe punktów odzyskiwania są zachowywane i przez czas.
Dozwolone wartości dla tego parametru to: liczby całkowite z zakresu od 1 do 28 i ostatnie.
Określ ten parametr, jeśli określisz parametry *DailyRetention* , *MonthlyRetentionInDailyFormat* i *YearlyRetentionInDailyFormat* .

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Określa tablicę dni tygodnia.
Dni, w których to polecenie cmdlet określa, jakie punkty odzyskiwania są zachowywane i jak długo.
Dopuszczalne wartości tego parametru to:

- Poniedziałek 
- Wtorku 
- Środa 
- Czwartek 
- Poniedziałek 
- Sobota 
- Niedziele

Określ ten parametr, jeśli określisz parametry *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* i *YearlyRetentionInWeeklyFormat* .

Należy się upewnić, że dni tygodnia, które zostały wybrane dla kopii zapasowej i do przechowywania, są wyrównane.
Jeśli na przykład dla kopii zapasowej jest ustawiona wartość soboty, zasady przechowywania muszą także korzystać z soboty.

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInDailyFormat
Wskazuje, że to polecenie cmdlet tworzy zasady miesięczne w codziennym formacie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
Wskazuje, że to polecenie cmdlet tworzy zasady miesięczne w formacie tygodnia.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
Określa, które miesiące roku mają punkty odzyskiwania, których kopie zapasowe są zachowywane w skali rocznej.
Dopuszczalne wartości tego parametru to: nazwy miesięcy, na przykład styczeń lub luty.

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Retencja
Określa okres przechowywania, w dniach, miesiącach lub latach, dla którego kopia zapasowa zawiera punkt kopii zapasowej.
Jednostka zależy od tego, czy to polecenie cmdlet umożliwia wybranie opcji przechowywania codziennie, comiesięcznego czy rocznego.
Jeśli na przykład określono parametr *DailyRetention* , polecenie cmdlet interpretuje bieżący parametr jako liczbę dni.

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

### -WeeklyRetention
Wskazuje, że to polecenie cmdlet tworzy cotygodniowe zasady przechowywania.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekNumber
Określa tygodnie miesiąca, które identyfikują, które kopie zapasowe punktów odzyskiwania są zachowywane i jak długo.
Dopuszczalne wartości tego parametru to:

- Pierwszy 
- Drugiego 
- 1/3 
- Czwarty 
- Końcu

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
Wskazuje, że to polecenie cmdlet tworzy zasady przechowywania roczne w codziennej formie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
Wskazuje, że to polecenie cmdlet tworzy roczne zasady przechowywania w formacie tygodnia.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### AzureRmBackupRetentionPolicy

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Nowe — AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


