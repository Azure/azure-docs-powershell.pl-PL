---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550668"
---
# New-AzureRmBackupProtectionPolicy

## STRESZCZENIe
Tworzy zasady tworzenia kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### NoScheduleParamSet (domyślny)
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmBackupProtectionPolicy** tworzy zasady kopii zapasowej platformy Azure jako obiektu programu Azure PowerShell.

Zasady tworzenia kopii zapasowych określają, kiedy i jak często kopia zapasowa wykonuje kopię zapasową elementu.
Polecenie cmdlet Enable-AzureRmBackupProtection używa zasad tworzenia kopii zapasowych.

## Przykłady

### Przykład 1: tworzenie codziennych zasad tworzenia kopii zapasowych przy użyciu codziennego i comiesięcznego przechowywania
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.
Polecenie zapisuje ten obiekt w zmiennej $Vault.

Drugie polecenie tworzy zasady przechowywania przez 30 dni codziennego przechowywania, a następnie zapisuje je w zmiennej $Daily.

Trzecie polecenie tworzy zasady przechowywania, które przechowują kopię zapasową w dziesiątym i dwudziestym dniu każdego miesiąca przez dwanaście miesięcy.
Polecenie przechowuje zasady przechowywania w zmiennej $Monthly.

Ostatnie polecenie tworzy zasady tworzenia kopii zapasowych dla magazynu w $Vault o godzinie codziennej kopii zapasowej 3:00 PM.
Polecenie przypisuje zasady przechowywania przechowywane w $Daily i $Monthly.
Polecenie zapisuje wyniki w zmiennej $ProtectionPolicy.

## PARAMETRÓW

### -Bez przestojów
Określa godzinę w postaci obiektu **DateTime** , dla operacji tworzenia kopii zapasowej.
Aby uzyskać **wartość DateTime** , użyj polecenia cmdlet Get-Date.
Aby uzyskać informacje o obiektach **DateTime** , wpisz `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Codziennie
Wskazuje, że operacja tworzenia kopii zapasowej jest uruchamiana w harmonogramie dziennym.

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Określa tablicę dni tygodnia.
Te zasady uruchamiają kopie zapasowe w dniach określonych przez ten parametr.
Dopuszczalne wartości tego parametru to:

- Poniedziałek 
- Wtorku 
- Środa 
- Czwartek 
- Poniedziałek 
- Sobota 
- Niedziele

Jeśli określisz parametr *Weekly* , określ ten parametr.

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę zasad tworzenia kopii zapasowych.
Wybierz nazwę, która jest unikatowa w magazynie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
Określa tablicę zasad przechowywania zasad tworzenia kopii zapasowych.
Aby uzyskać **AzureRmBackupRetentionPolicy** , użyj polecenia cmdlet New-AzureRmBackupRetentionPolicyObject.

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
Określa typ elementu kopii zapasowej, którego dotyczą zasady.
Obecnie jedyną obsługiwaną wartością jest AzureVM.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazyn
Określa magazyn kopii zapasowych Azure, do którego należą zasady tworzenia kopii zapasowych.
Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Co tydzień
Wskazuje, że zasady tworzenia kopii zapasowych są wyzwalane co tydzień w co najmniej jednym dniu tygodnia.

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### AzureRmBackupProtectionPolicy

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Nowe — AzureRmBackupRetentionPolicyObject](./New-AzureRmBackupRetentionPolicyObject.md)

[Remove-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)

[Set-AzureRmBackupProtectionPolicy](./Set-AzureRmBackupProtectionPolicy.md)


