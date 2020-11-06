---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541943"
---
# Stop-AzureRmBackupJob

## STRESZCZENIe
Anuluje istniejące zadanie kopii zapasowej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### IdFiltersSet
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobFiltersSet
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **stop-AzureRmBackupJob** anuluje istniejące zadanie kopii zapasowej Azure.
Za pomocą tego parametru można zatrzymać zadanie, które trwa zbyt długo i blokuje inne działania.
Możesz anulować tylko następujące typy zadań: 
- Wykonania
- Przywrócenie

## Przykłady

### Przykład 1: zatrzymanie zadania kopii zapasowej przy użyciu identyfikatora zadania
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .
Polecenie zapisuje ten obiekt w zmiennej $Vault.
Drugie polecenie pobiera zadanie kopii zapasowej z magazynu w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupJob** .
Polecenie zapisuje zadanie w zmiennej $Job.
W tym przykładzie istnieje tylko jedna operacja wykonywania kopii zapasowej w określonym magazynie.
Polecenie ostatnie zatrzymuje zadanie o określonym IDENTYFIKATORze.

### Przykład 2: zatrzymanie wszystkich operacji przywracania
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

To polecenie pobiera wszystkie operacje przywracania w magazynie w $Vault, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet zatrzymuje każde zadanie.

## PARAMETRÓW

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

### — Zadanie
Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.
Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobID
Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.
Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Magazyn
Określa magazyn kopii zapasowych, w którym to polecenie cmdlet anuluje zadanie.
Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
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

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob
Parametry: zadanie (ByValue)

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


