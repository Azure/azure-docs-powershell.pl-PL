---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231682"
---
# <span data-ttu-id="9bcd6-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9bcd6-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="9bcd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bcd6-102">SYNOPSIS</span></span>

<span data-ttu-id="9bcd6-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="9bcd6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bcd6-104">SYNTAX</span></span>

### <span data-ttu-id="9bcd6-105">AzureVMParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bcd6-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd6-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bcd6-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd6-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="9bcd6-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd6-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bcd6-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd6-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bcd6-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd6-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bcd6-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bcd6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="9bcd6-111">DESCRIPTION</span></span>

<span data-ttu-id="9bcd6-112">Polecenie cmdlet **Restore-AzRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="9bcd6-113">To polecenie cmdlet rozpoczyna przywracanie z magazynu usług Recovery Services na konto magazynu klienta.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="9bcd6-114">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="9bcd6-115">Po zakończeniu operacji przywracania przywracana jest przygotowana ilość dysków zarządzanych do grupy zasobów docelowych i informacji o konfiguracji na koncie magazynu klientów, należy utworzyć maszynę wirtualną i uruchomić ją.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="9bcd6-116">Aby uzyskać więcej informacji, refter do innych możliwych zestawów parametrów i tekstu parametrów.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="9bcd6-117">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="9bcd6-118">Uwaga: Aby pomyślnie wykonać to polecenie cmdlet (oprócz parametru-VaultId), należy również użyć parametru VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="9bcd6-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bcd6-119">EXAMPLES</span></span>

### <span data-ttu-id="9bcd6-120">Przykład 1: Przywracanie elementu do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="9bcd6-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="9bcd6-121">Pierwsze polecenie pobiera magazyn RecoveryServices i zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="9bcd6-122">Drugie polecenie pobiera elementy kopii zapasowej, a następnie zapisuje je w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9bcd6-123">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="9bcd6-124">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="9bcd6-125">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="9bcd6-126">Polecenie szóste określa dyski do przywrócenia z punktu odzyskiwania i zapisuje je w zmiennej $restoreDiskLUNs.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="9bcd6-127">Ostatnie polecenie przywraca dyski do docelowego konta magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="9bcd6-128">Przykład 2: Przywracanie wielu plików elementu AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="9bcd6-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="9bcd6-129">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9bcd6-130">Drugie polecenie pobiera element kopii zapasowej o nazwie fileshareitem, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9bcd6-131">W trzecim poleceniu jest pobierana lista punktów odzyskiwania dla określonego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="9bcd6-132">Czwarte polecenie spceifies, które pliki należy przywrócić i przechowywać w zmiennej $files.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="9bcd6-133">Ostatnie polecenie przywraca określone pliki do pierwotnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="9bcd6-134">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9bcd6-134">Example 3</span></span>

<span data-ttu-id="9bcd6-135">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="9bcd6-136">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="9bcd6-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="9bcd6-137">Przykład 4: Przywracanie zarządzanej maszyny wirtualnej jako dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="9bcd6-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="9bcd6-138">Pierwsze polecenie pobiera magazyn RecoveryServices i zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="9bcd6-139">Drugie polecenie pobiera element kopii zapasowej, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9bcd6-140">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="9bcd6-141">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="9bcd6-142">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="9bcd6-143">Polecenie szóste powoduje przywrócenie dysków jako zarządzanych dysków z określoną grupą zasobów docelowych.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="9bcd6-144">Przykład 5: Przywracanie zarządzanej maszyny wirtualnej jako dysków niezarządzanych</span><span class="sxs-lookup"><span data-stu-id="9bcd6-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="9bcd6-145">Pierwsze polecenie pobiera magazyn RecoveryServices i zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="9bcd6-146">Drugie polecenie pobiera element kopii zapasowej, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9bcd6-147">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="9bcd6-148">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="9bcd6-149">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="9bcd6-150">Polecenie szóste powoduje przywrócenie dysków jako dysków niezarządzanych.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="9bcd6-151">Przykład 6: Przywracanie niezarządzanej maszyny wirtualnej jako dysków niezarządzanych przy użyciu oryginalnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="9bcd6-152">Pierwsze polecenie pobiera magazyn RecoveryServices i zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="9bcd6-153">Drugie polecenie pobiera element kopii zapasowej, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9bcd6-154">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="9bcd6-155">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="9bcd6-156">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="9bcd6-157">Szóste polecenie przywraca dyski jako niezarządzane dyski przy użyciu oryginalnego konta magazynu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="9bcd6-158">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bcd6-158">PARAMETERS</span></span>

### <span data-ttu-id="9bcd6-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcd6-159">-DefaultProfile</span></span>

<span data-ttu-id="9bcd6-160">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bcd6-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="9bcd6-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="9bcd6-162">Służy do przywracania wielu plików z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="9bcd6-163">Ścieżki elementów, które mają zostać przywrócone w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="9bcd6-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9bcd6-164">-RecoveryPoint</span></span>

<span data-ttu-id="9bcd6-165">Określa punkt odzyskiwania, do którego ma zostać przywrócony element kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="9bcd6-166">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="9bcd6-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="9bcd6-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="9bcd6-167">-ResolveConflict</span></span>

<span data-ttu-id="9bcd6-168">W przypadku gdy przywrócony element istnieje również w miejscu docelowym, Użyj tej pozycji, aby wskazać, czy zastąpić go.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="9bcd6-169">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9bcd6-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9bcd6-170">Zastąpić</span><span class="sxs-lookup"><span data-stu-id="9bcd6-170">Overwrite</span></span>
- <span data-ttu-id="9bcd6-171">Przeskok</span><span class="sxs-lookup"><span data-stu-id="9bcd6-171">Skip</span></span>

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

### <span data-ttu-id="9bcd6-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="9bcd6-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="9bcd6-173">Użyj tego przełącznika, aby określić przywracanie jako niezarządzanych dysków</span><span class="sxs-lookup"><span data-stu-id="9bcd6-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="9bcd6-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="9bcd6-174">-RestoreDiskList</span></span>
<span data-ttu-id="9bcd6-175">Określanie dysków do odzyskania kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9bcd6-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="9bcd6-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="9bcd6-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="9bcd6-177">Użyj tego przełącznika, aby przywrócić tylko dyski systemu operacyjnego kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9bcd6-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="9bcd6-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="9bcd6-178">-SourceFilePath</span></span>

<span data-ttu-id="9bcd6-179">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="9bcd6-180">Ścieżka elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="9bcd6-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="9bcd6-181">-SourceFileType</span></span>

<span data-ttu-id="9bcd6-182">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="9bcd6-183">Typ elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="9bcd6-184">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9bcd6-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9bcd6-185">Plik</span><span class="sxs-lookup"><span data-stu-id="9bcd6-185">File</span></span>
- <span data-ttu-id="9bcd6-186">Directory</span><span class="sxs-lookup"><span data-stu-id="9bcd6-186">Directory</span></span>

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

### <span data-ttu-id="9bcd6-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9bcd6-187">-StorageAccountName</span></span>

<span data-ttu-id="9bcd6-188">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="9bcd6-189">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="9bcd6-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bcd6-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="9bcd6-191">Określa nazwę grupy zasobów zawierającej docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="9bcd6-192">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="9bcd6-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="9bcd6-193">-TargetFileShareName</span></span>

<span data-ttu-id="9bcd6-194">Udział pliku, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="9bcd6-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="9bcd6-195">-TargetFolder</span></span>

<span data-ttu-id="9bcd6-196">Folder, w którym ma zostać przywrócony udział plików w TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="9bcd6-197">Jeśli kopia zapasowa zawartości ma zostać przywrócona do folderu głównego, wprowadź wartości w folderze docelowym jako ciąg pusty.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="9bcd6-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bcd6-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="9bcd6-199">Grupa zasobów, do której są przywracane zarządzane dyski.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="9bcd6-200">Dotyczy kopii zapasowych maszyny wirtualnej z zarządzanymi dyskami</span><span class="sxs-lookup"><span data-stu-id="9bcd6-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="9bcd6-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9bcd6-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="9bcd6-202">Konto magazynu, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="9bcd6-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9bcd6-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="9bcd6-204">Użyj tego przełącznika, jeśli dyski z punktu odzyskiwania zostaną przywrócone do oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="9bcd6-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9bcd6-205">-VaultId</span></span>

<span data-ttu-id="9bcd6-206">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9bcd6-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="9bcd6-207">-VaultLocation</span></span>

<span data-ttu-id="9bcd6-208">Lokalizacja magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9bcd6-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="9bcd6-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="9bcd6-210">Konfiguracja odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="9bcd6-210">Recovery config</span></span>

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

### <span data-ttu-id="9bcd6-211">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bcd6-211">-Confirm</span></span>

<span data-ttu-id="9bcd6-212">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bcd6-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bcd6-213">-WhatIf</span></span>

<span data-ttu-id="9bcd6-214">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="9bcd6-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcd6-215">CommonParameters</span></span>
<span data-ttu-id="9bcd6-216">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bcd6-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcd6-217">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bcd6-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcd6-218">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bcd6-218">INPUTS</span></span>

### <span data-ttu-id="9bcd6-219">System. String</span><span class="sxs-lookup"><span data-stu-id="9bcd6-219">System.String</span></span>

### <span data-ttu-id="9bcd6-220">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="9bcd6-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="9bcd6-221">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bcd6-221">OUTPUTS</span></span>

### <span data-ttu-id="9bcd6-222">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9bcd6-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9bcd6-223">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bcd6-223">NOTES</span></span>

## <span data-ttu-id="9bcd6-224">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bcd6-224">RELATED LINKS</span></span>

[<span data-ttu-id="9bcd6-225">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9bcd6-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="9bcd6-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9bcd6-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="9bcd6-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9bcd6-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
