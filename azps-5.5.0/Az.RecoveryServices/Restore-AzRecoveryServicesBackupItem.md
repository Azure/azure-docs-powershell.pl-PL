---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191346"
---
# Restore-AzRecoveryServicesBackupItem

## SYNOPSIS

Przywraca dane i konfigurację elementu kopii zapasowej do określonego punktu odzyskiwania. Wymagane parametry różnią się w zależności od typu elementu kopii zapasowej.
To samo polecenie jest używane do przywracania maszyn wirtualnych platformy Azure, baz danych działających w ramach maszyn wirtualnych platformy Azure oraz udziałów plików platformy Azure.

## SKŁADNIA

### AzureVMParameterSet (domyślne)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedMeterParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedMeterParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS

Polecenie cmdlet **Restore-AzRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.

**Kopia zapasowa maszyn wirtualnych platformy Azure**

Używając tego polecenia, możesz utworzyć kopię zapasową maszyn wirtualnych platformy Azure i przywrócić dyskietki (zarówno zarządzane, jak i nieza zarządzane). Operacja przywracania nie powoduje przywrócenia pełnej maszyny wirtualnej.
Jeśli jest to zarządzana dyskowa maszyny wirtualnej, należy określić grupę zasobów docelowych, w której przechowywane są przywrócone dyskietki. Jeśli określono grupę zasobów docelowych, jeśli migawki znajdują się w grupie zasobów określonej w zasadach kopii zapasowej, operacja przywracania będzie natychmiastowa, a dyskrówna zostanie utworzona na podstawie lokalnych migawek i będzie przechowywana w grupie zasobów docelowych. Istnieje również możliwość ich przywrócenia jako dyskietek nieza zarządzanych, ale spowoduje to wykorzystanie danych obecnych w magazynie usług odzyskiwania platformy Azure, przez co będzie znacznie wolniejsze. Konfiguracja maszyny wirtualnej i szablonu wdrożenia, którego można użyć do utworzenia maszyny wirtualnej z przywróconego dyskietki, zostaną pobrane na określone konto magazynu.
Jeśli jest to nie zarządzana dyskowa maszyny wirtualnej, migawki są obecne w oryginalnym koncie magazynu dysku i/lub w magazynie usług odzyskiwania. Jeśli użytkownik udostępnia opcję przywracania przy użyciu oryginalnego konta magazynu, można błyskawicznie przywrócić dane. W przeciwnym razie dane są pobierane z magazynu usług Azure Recovery, a dysk dyskowe są tworzone w określonym koncie magazynu wraz z konfiguracją maszyny wirtualnej i szablonu wdrożenia.

> [!IMPORTANT]
> Domyślnie kopia zapasowa maszyn wirtualnych platformy Azure jest kopią zapasową wszystkich dysków. Podczas włączania kopii zapasowej można selektywnie utworzyć kopię zapasową odpowiednich dysków, używając parametrów Lista wykluczeń lub Lista Dołączeń. Opcja selektywnego przywracania dysków jest dostępna tylko wtedy, gdy jedna z nich selektywnie przywróciła ich kopię zapasową.

Aby uzyskać więcej informacji, zapoznaj się z różnymi możliwymi zestawami parametrów i tekstem parametrów.

> [!NOTE]
> Jeśli jest używany parametr -VaultId, wówczas powinien być również używany parametr -VaultLocation.

**Kopia zapasowa udostępniania plików platformy Azure**

Możesz przywrócić cały udział plików lub określone/wiele plików/folderów w danym udostępniniu. Możesz przywrócić pierwotną lokalizację lub do lokalizacji alternatywnej.

**W przypadku obciążeń pracą na platformie Azure**

Możesz przywrócić bazy danych SQL DB w ramach maszyn wirtualnych platformy Azure


## PRZYKŁADY

### Przykład 1. Przywracanie dysków z kopią zapasową zarządzanej maszyny wirtualnej Azure z danego punktu odzyskiwania

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Pierwsze polecenie pobiera magazyn usług odzyskiwania i przechowuje go w $vault zmienną.
Drugie polecenie pobiera element Kopii zapasowej typu AzureVM o nazwie "V2VM" i przechowuje go w $BackupItem danych.
Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.
Czwarte polecenie pobiera bieżącą datę, a następnie przechowuje je w $EndDate zmienną.
Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.
Ostatnie polecenie przywraca wszystkie dyskietki w docelowej grupie zasobów Target_RG, a następnie udostępnia informacje o konfiguracji maszyny wirtualnej i szablon wdrożenia w koncie magazynu DestAccount w grupie zasobów DestRG.

### Przykład 2. Przywracanie określonego dysku zapasowego zarządzanej maszyny wirtualnej Azure z danego punktu odzyskiwania

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Pierwsze polecenie pobiera magazyn usług odzyskiwania i przechowuje go w $vault zmienną.
Drugie polecenie pobiera element kopii zapasowej typu AzureVM o nazwie "V2VM" i przechowuje go w $BackupItem danych.
Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.
Czwarte polecenie pobiera bieżącą datę, a następnie przechowuje je w $EndDate zmienną.
Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.
Szóste polecenie przechowuje listę dysków, które mają zostać przywrócone, w zmiennej restore InformacjeOkichi.
Ostatnie polecenie przywraca wskazane dyskietki z określonych luns, do grupy zasobów docelowych Target_RG, a następnie udostępnia informacje o konfiguracji maszyny wirtualnej i szablon wdrożenia w koncie magazynu DestAccount w grupie zasobów DestRG.

### Przykład 3. Przywracanie dysków zarządzanej maszyny wirtualnej jako niezamanektowana dyskietki

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Pierwsze polecenie pobiera magazyn RecoveryServices i przechowuje go w $vault zmienną.
Drugie polecenie pobiera element kopii zapasowej, a następnie przechowuje go w $BackupItem danych.
Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.
Czwarte polecenie pobiera bieżącą datę, a następnie przechowuje je w $EndDate zmienną.
Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.
Szóste polecenie przywraca dyskietki jako niezamanektowane dyskietki.

### Przykład 4. Przywracanie niezamanektowej maszyny wirtualnej jako niezamanektowana dyskietki przy użyciu oryginalnego konta magazynu

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Pierwsze polecenie pobiera magazyn RecoveryServices i przechowuje go w $vault zmienną.
Drugie polecenie pobiera element kopii zapasowej, a następnie przechowuje go w $BackupItem danych.
Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.
Czwarte polecenie pobiera bieżącą datę, a następnie przechowuje je w $EndDate zmienną.
Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.
Szóste polecenie przywraca dyskietki jako niezamanektowane dyskietki do ich oryginalnych kont magazynu

### Przykład 5. Przywracanie wielu plików elementu AzureFileShare

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Pierwsze polecenie pobiera magazyn usług odzyskiwania i przechowuje go w $vault zmienną.
Drugie polecenie pobiera element kopii zapasowej o nazwie fileshareitem i zapisuje go w $BackupItem pliku.
Trzecie polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej.
Czwarte polecenie określa, które pliki mają zostać przywrócone i przechowywane w $files zmienną.
Ostatnie polecenie przywraca wskazane pliki do pierwotnej lokalizacji.

### Przykład 6. Przywracanie bazy danych SQL w usłudze Azure WIRTUALNEj do innej docelowej maszyny wirtualnej w celu pełnego punktu odzyskiwania

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### Przykład 7. Przywracanie bazy danych SQL w usłudze Azure VM do innej docelowej maszyny wirtualnej dla punktu odzyskiwania dziennika

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## PARAMETERS

### -DefaultProfile

Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -MultipleSourceFilePath
Służy do przywracania wielu plików z udziału plików. Ścieżki elementów, które mają zostać przywrócone w ramach udziału plików.

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - RecoveryPoint

Określa punkt odzyskiwania, do którego ma zostać przywrócony element kopii zapasowej.
Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint.**

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### - ResolveConflict

Jeśli przywrócony element także istnieje w lokalizacji docelowej, skorzystaj z tej informacji, aby wskazać, czy chcesz zastąpić element, czy nie.
Dopuszczalne wartości dla tego parametru to:

- Zastąp
- Pomiń

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreAsUnmanaged Jednakowe
Użyj tego przełącznika, aby określić, że przywracana jest dyskietki niezamanektowane

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Restore WymusznaLista
Określanie dyskietki do odzyskania kopii zapasowej maszyny wirtualnej

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOS Jednakowa
Użyj tego przełącznika, aby przywrócić tylko dyski systemu operacyjnego kopii zapasowej maszyny wirtualnej

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

Służy do przywracania określonego elementu z udziału plików. Ścieżka elementu, który ma zostać przywrócony w ramach udziału plików.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType

Służy do przywracania określonego elementu z udziału plików. Typ elementu, który ma zostać przywrócony w ramach udziału plików.
Dopuszczalne wartości dla tego parametru to:

- Plik
- Katalog

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

Określa nazwę docelowego konta magazynu w subskrypcji.
W ramach procesu przywracania to polecenie cmdlet przechowuje informacje o dyskach i konfiguracji na tym koncie magazynu.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

Określa nazwę grupy zasobów, która zawiera docelowe konto magazynu w subskrypcji.
W ramach procesu przywracania to polecenie cmdlet przechowuje informacje o dyskach i konfiguracji na tym koncie magazynu.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

Udział plików, do którego należy przywrócić udział plików.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - TargetFolder

Folder, w którym należy przywrócić udział plików, w obrębie parametru TargetFileShareName. Jeśli zawartość kopii zapasowej ma zostać przywrócona do folderu głównego, nadaj wartości folderu docelowego jako pusty ciąg.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName

Grupa zasobów, do której przywracane są zarządzane dyskietki. Dotyczy kopii zapasowej maszyny wirtualnej z zarządzanymi dyskami

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

Konto magazynu, do którego należy przywrócić udział plików.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount

Użyj tego przełącznika, jeśli dyskietki z punktu odzyskiwania mają zostać przywrócone do ich oryginalnych kont magazynu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId 

Identyfikator DES do szyfrowania przywracanych dysków.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreToSecondaryRegion

Użyj tego przełącznika, aby wyzwolić przywracanie regionu między regionami do regionu pomocniczego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

ARM identyfikatora magazynu usług odzyskiwania.

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

### -VaultLocation

Lokalizacja magazynu usług odzyskiwania.

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

### -WLRecoveryConfig

Konfiguracja odzyskiwania

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Potwierdź

Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryPointBase

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase

## NOTATKI

## LINKI POKREWNE

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
