---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541952"
---
# Set-AzureRmBackupProtectionPolicy

## STRESZCZENIe
Modyfikuje istniejące zasady ochrony.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### NoScheduleParamSet (domyślny)
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmBackupProtectionPolicy** modyfikuje istniejące zasady ochrony w usłudze Kopia zapasowa Azure.
Można zmodyfikować następujące składniki zasad ochrony: 
- Nazwę
- Harmonogram kopii zapasowych
- Zasady przechowywania wszelkie zmiany mogą mieć wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z zasadami.

## Przykłady

## PARAMETRÓW

### -Bez przestojów
Określa nową godzinę utworzenia kopii zapasowej, na przykład obiekt **DateTime** , dla zasady.
Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.
Aby uzyskać informacje o obiektach **DateTime** , wpisz `Get-Help Get-Date` .

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Codziennie
Wskazuje, że operacja tworzenia kopii zapasowej jest uruchamiana w harmonogramie dziennym.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
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

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -NewName
Określa nową nazwę zasady.
Ta nazwa musi być unikatowa w magazynie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionPolicy
Określa zasady ochrony, które modyfikuje to polecenie cmdlet.
Aby uzyskać obiekt **AzureRmBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmBackupProtectionPolicy.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Określa tablicę zasad przechowywania zasad tworzenia kopii zapasowych.
Aby uzyskać obiekty **AzureRmBackupRetentionPolicy** , użyj polecenia cmdlet New-AzureRmBackupRetentionPolicyObject.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Co tydzień
Wskazuje, że operacja tworzenia kopii zapasowej jest wykonywana w harmonogramie tygodniowym.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupProtectionPolicy
Parametry: ProtectionPolicy (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


