---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708658"
---
# Get-AzRecoveryServicesBackupRecoveryPoint

## STRESZCZENIe
Pobiera punkty odzyskiwania dla elementu z kopii zapasowej.

## POLECENIA

### NoFilterParameterSet (domyślny)
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RecoveryPointId
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** pobiera punkty odzyskiwania dla kopii zapasowej elementu kopii zapasowej platformy Azure.
Po wykonaniu kopii zapasowej elementu obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** ma co najmniej jeden punkt odzyskiwania.
Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.

## Przykłady

### Przykład 1: uzyskiwanie punktów odzyskiwania z ostatniego tygodnia dla elementu
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

Pierwsze polecenie pobiera datę z siedmiu dni temu, a następnie zapisuje ją w zmiennej $StartDate.
Drugie polecenie pobiera dzisiejszą datę, a następnie zapisuje je w zmiennej $EndDate.
Trzecie polecenie pobiera kontenery kopii zapasowych AzureVM i przechowuje je w zmiennej $Containers.
Czwarte polecenie uzyskuje element kopii zapasowej o nazwie V2VM, a następnie zapisuje go w zmiennej $BackupItem.
Ostatnie polecenie pobiera tablicę punktów odzyskiwania dla elementu w $BackupItem, a następnie zapisuje je w zmiennej $RP.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
Określa koniec zakresu dat.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item
Określa element, dla którego to polecenie cmdlet umożliwia pobieranie punktów odzyskiwania.
Aby uzyskać obiekt **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFileDownloadLocation
Określa lokalizację, w której ma zostać pobrany plik wejściowy, w celu przywrócenia klucza magazynu kluczy dla zaszyfrowanej maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPointId
Określa identyfikator punktu odzyskiwania.

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataRozpoczęcia
Określa początek zakresu dat.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
Identyfikator ARM magazynu usług Recovery Services.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase

## INFORMACYJN

## LINKI POKREWNE

[Get-AzRecoveryServicesBackupContainer](./Get-AzRecoveryServicesBackupContainer.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)


