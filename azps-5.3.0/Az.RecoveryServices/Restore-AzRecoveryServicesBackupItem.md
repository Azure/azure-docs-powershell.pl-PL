---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 32ecad0d89725d4fa01d76ebfe9a319dfece6b80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490789"
---
# <span data-ttu-id="eec11-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="eec11-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="eec11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eec11-102">SYNOPSIS</span></span>

<span data-ttu-id="eec11-103">Przywraca dane i konfigurację elementu kopii zapasowej do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eec11-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="eec11-104">Wymagane parametry są różne w zależności od typu elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="eec11-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="eec11-105">To samo polecenie służy do przywracania maszyn wirtualnych platformy Azure, baz danych uruchomionych na maszynach wirtualnych platformy Azure i udziałów plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eec11-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="eec11-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eec11-106">SYNTAX</span></span>

### <span data-ttu-id="eec11-107">AzureVMParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eec11-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec11-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec11-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec11-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="eec11-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec11-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec11-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec11-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec11-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec11-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec11-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec11-113">Opis</span><span class="sxs-lookup"><span data-stu-id="eec11-113">DESCRIPTION</span></span>

<span data-ttu-id="eec11-114">Polecenie cmdlet **Restore-AzRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eec11-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="eec11-115">**Kopia zapasowa Azure VM**</span><span class="sxs-lookup"><span data-stu-id="eec11-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="eec11-116">Za pomocą tego polecenia możesz wykonywać kopie zapasowe maszyn wirtualnych platformy Azure oraz przywracać dyski (zarządzane i niezarządzane).</span><span class="sxs-lookup"><span data-stu-id="eec11-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="eec11-117">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eec11-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="eec11-118">Jeśli jest to zarządzana maszyna wirtualna dysku, należy określić grupę zasobów docelowych, w której są przechowywane przywrócone dyski.</span><span class="sxs-lookup"><span data-stu-id="eec11-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="eec11-119">Gdy grupa zasobów docelowych jest określona, jeśli migawki znajdują się w grupie zasobów określonej w zasadach kopii zapasowej, operacja przywracania będzie dostępna, a dyski zostaną utworzone z migawek lokalnych i zachowane w grupie zasób docelowy.</span><span class="sxs-lookup"><span data-stu-id="eec11-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="eec11-120">Dostępna jest również opcja przywrócenia jako dyski niezarządzane, ale będzie ona korzystać z danych w magazynie usług Azure Recovery Services, a zatem będzie dużo wolniejsze.</span><span class="sxs-lookup"><span data-stu-id="eec11-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="eec11-121">Konfiguracja maszyny wirtualnej i szablonu wdrażania, której można użyć do utworzenia maszyny wirtualnej z przywróconych dysków, zostanie pobrana do określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="eec11-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="eec11-122">Jeśli jest to niezarządzana maszyna wirtualna dysków, migawki są obecne na oryginalnym koncie magazynu dysku i/lub w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="eec11-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="eec11-123">Jeśli użytkownik podaje możliwość przywrócenia oryginalnego konta magazynu, można użyć funkcji przywracania błyskawicznego.</span><span class="sxs-lookup"><span data-stu-id="eec11-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="eec11-124">W przeciwnym razie dane są pobierane z magazynu usługi Azure Recovery Services i dyski są tworzone w określonym koncie magazynu wraz z konfiguracją maszyny wirtualnej i szablonu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="eec11-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eec11-125">Domyślnie kopia zapasowa w usłudze Azure VM wykonuje kopię zapasową wszystkich dysków.</span><span class="sxs-lookup"><span data-stu-id="eec11-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="eec11-126">Możesz wybiórczo wykonywać kopie zapasowe odpowiednich dysków przy użyciu parametrów exclusionList lub InclusionList podczas włączania i wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="eec11-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="eec11-127">Opcja selektywnego przywracania dysków jest dostępna tylko wtedy, gdy jedna z nich selektywnie poprosiła o wykonanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="eec11-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="eec11-128">Aby uzyskać więcej informacji, zapoznaj się z innymi możliwymi zestawami parametrów i tekstem parametrów.</span><span class="sxs-lookup"><span data-stu-id="eec11-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="eec11-129">Należy użyć parametru if-VaultId, a także parametru-VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="eec11-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="eec11-130">**Kopia zapasowa udziału plików platformy Azure**</span><span class="sxs-lookup"><span data-stu-id="eec11-130">**For Azure File share backup**</span></span>

<span data-ttu-id="eec11-131">W udziale możesz przywrócić cały udział plików lub konkretne/wiele plików/folderów.</span><span class="sxs-lookup"><span data-stu-id="eec11-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="eec11-132">Możesz przywrócić pierwotną lokalizację lub alternatywną lokalizację.</span><span class="sxs-lookup"><span data-stu-id="eec11-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="eec11-133">**W przypadku obciążeń Azure**</span><span class="sxs-lookup"><span data-stu-id="eec11-133">**For Azure Workloads**</span></span>

<span data-ttu-id="eec11-134">Możesz przywrócić usługę SQL DBs na platformie Azure VMs</span><span class="sxs-lookup"><span data-stu-id="eec11-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="eec11-135">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eec11-135">EXAMPLES</span></span>

### <span data-ttu-id="eec11-136">Przykład 1: Przywracanie dysków z kopii zapasowej zarządzanej maszyny wirtualnej platformy Azure z określonego punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="eec11-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="eec11-137">Pierwsze polecenie pobiera magazyn usług Recovery Services i przechowuje go w $vault zmiennej.</span><span class="sxs-lookup"><span data-stu-id="eec11-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="eec11-138">Drugie polecenie pobiera element kopii zapasowej typu AzureVM o nazwie "V2VM" i zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="eec11-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="eec11-139">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="eec11-140">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="eec11-141">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="eec11-142">Ostatnie polecenie przywraca wszystkie dyski do grupy zasobów docelowych Target_RG, a następnie udostępnia informacje o konfiguracji maszyny wirtualnej i szablonie wdrożenia na koncie magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="eec11-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="eec11-143">Przykład 2: Przywracanie określonych dysków z kopii zapasowej zarządzanej maszyny wirtualnej na platformie Azure z określonego punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="eec11-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="eec11-144">Pierwsze polecenie pobiera magazyn usług Recovery Services i przechowuje go w $vault zmiennej.</span><span class="sxs-lookup"><span data-stu-id="eec11-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="eec11-145">Drugie polecenie pobiera element kopii zapasowej typu AzureVM o nazwie "V2VM" i zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="eec11-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="eec11-146">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="eec11-147">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="eec11-148">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="eec11-149">Szóste polecenie zapisuje listę dysków do przywrócenia w zmiennej restoreDiskLUN.</span><span class="sxs-lookup"><span data-stu-id="eec11-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="eec11-150">Ostatnie polecenie przywraca dane na podstawie określonych dysków LUN do grupy zasobów docelowych Target_RG, a następnie udostępnia informacje o konfiguracji maszyny wirtualnej i szablonie wdrożenia na koncie magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="eec11-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="eec11-151">Przykład 3: Przywracanie dysków zarządzanej maszyny wirtualnej jako dysków niezarządzanych</span><span class="sxs-lookup"><span data-stu-id="eec11-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="eec11-152">Pierwsze polecenie pobiera magazyn RecoveryServices i zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="eec11-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="eec11-153">Drugie polecenie pobiera element kopii zapasowej, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="eec11-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="eec11-154">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="eec11-155">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="eec11-156">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="eec11-157">Polecenie szóste powoduje przywrócenie dysków jako dysków niezarządzanych.</span><span class="sxs-lookup"><span data-stu-id="eec11-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="eec11-158">Przykład 4: Przywracanie niezarządzanej maszyny wirtualnej jako dysków niezarządzanych przy użyciu oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="eec11-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="eec11-159">Pierwsze polecenie pobiera magazyn RecoveryServices i zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="eec11-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="eec11-160">Drugie polecenie pobiera element kopii zapasowej, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="eec11-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="eec11-161">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="eec11-162">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="eec11-163">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="eec11-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="eec11-164">Polecenie szóste powoduje przywrócenie dysków jako niezarządzanych do oryginalnych kont magazynu</span><span class="sxs-lookup"><span data-stu-id="eec11-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="eec11-165">Przykład 5: Przywracanie wielu plików elementu AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="eec11-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="eec11-166">Pierwsze polecenie pobiera magazyn usług Recovery Services i przechowuje go w $vault zmiennej.</span><span class="sxs-lookup"><span data-stu-id="eec11-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="eec11-167">Drugie polecenie pobiera element kopii zapasowej o nazwie fileshareitem, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="eec11-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="eec11-168">W trzecim poleceniu jest pobierana lista punktów odzyskiwania dla określonego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="eec11-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="eec11-169">W czwartym poleceniu są określone pliki do przywrócenia i przechowywane w zmiennej $files.</span><span class="sxs-lookup"><span data-stu-id="eec11-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="eec11-170">Ostatnie polecenie przywraca określone pliki do pierwotnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="eec11-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="eec11-171">Przykład 6: Przywracanie bazy danych SQL w ramach maszyny wirtualnej platformy Azure do innej docelowej maszyny wirtualnej dla unikatowego pełnego punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="eec11-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="eec11-172">Przykład 7: Przywracanie bazy danych SQL w ramach maszyny wirtualnej platformy Azure do innej docelowej maszyny wirtualnej dla punktu odzyskiwania dziennika</span><span class="sxs-lookup"><span data-stu-id="eec11-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="eec11-173">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eec11-173">PARAMETERS</span></span>

### <span data-ttu-id="eec11-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec11-174">-DefaultProfile</span></span>

<span data-ttu-id="eec11-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eec11-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec11-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="eec11-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="eec11-177">Służy do przywracania wielu plików z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="eec11-178">Ścieżki elementów, które mają zostać przywrócone w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="eec11-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="eec11-179">-RecoveryPoint</span></span>

<span data-ttu-id="eec11-180">Określa punkt odzyskiwania, do którego ma zostać przywrócony element kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="eec11-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="eec11-181">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="eec11-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="eec11-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="eec11-182">-ResolveConflict</span></span>

<span data-ttu-id="eec11-183">W przypadku gdy przywrócony element istnieje również w miejscu docelowym, Użyj tej pozycji, aby wskazać, czy zastąpić go.</span><span class="sxs-lookup"><span data-stu-id="eec11-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="eec11-184">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eec11-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eec11-185">Zastąpić</span><span class="sxs-lookup"><span data-stu-id="eec11-185">Overwrite</span></span>
- <span data-ttu-id="eec11-186">Przeskok</span><span class="sxs-lookup"><span data-stu-id="eec11-186">Skip</span></span>

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

### <span data-ttu-id="eec11-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="eec11-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="eec11-188">Użyj tego przełącznika, aby określić przywracanie jako niezarządzanych dysków</span><span class="sxs-lookup"><span data-stu-id="eec11-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="eec11-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="eec11-189">-RestoreDiskList</span></span>
<span data-ttu-id="eec11-190">Określanie dysków do odzyskania kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eec11-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="eec11-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="eec11-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="eec11-192">Użyj tego przełącznika, aby przywrócić tylko dyski systemu operacyjnego kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eec11-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="eec11-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="eec11-193">-SourceFilePath</span></span>

<span data-ttu-id="eec11-194">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="eec11-195">Ścieżka elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="eec11-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="eec11-196">-SourceFileType</span></span>

<span data-ttu-id="eec11-197">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="eec11-198">Typ elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="eec11-199">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eec11-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eec11-200">Plik</span><span class="sxs-lookup"><span data-stu-id="eec11-200">File</span></span>
- <span data-ttu-id="eec11-201">Directory</span><span class="sxs-lookup"><span data-stu-id="eec11-201">Directory</span></span>

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

### <span data-ttu-id="eec11-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eec11-202">-StorageAccountName</span></span>

<span data-ttu-id="eec11-203">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="eec11-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="eec11-204">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="eec11-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="eec11-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec11-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="eec11-206">Określa nazwę grupy zasobów zawierającej docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="eec11-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="eec11-207">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="eec11-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="eec11-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="eec11-208">-TargetFileShareName</span></span>

<span data-ttu-id="eec11-209">Udział pliku, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="eec11-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="eec11-210">-TargetFolder</span></span>

<span data-ttu-id="eec11-211">Folder, w którym ma zostać przywrócony udział plików w TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="eec11-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="eec11-212">Jeśli kopia zapasowa zawartości ma zostać przywrócona do folderu głównego, wprowadź wartości w folderze docelowym jako ciąg pusty.</span><span class="sxs-lookup"><span data-stu-id="eec11-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="eec11-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec11-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="eec11-214">Grupa zasobów, do której są przywracane zarządzane dyski.</span><span class="sxs-lookup"><span data-stu-id="eec11-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="eec11-215">Dotyczy kopii zapasowych maszyny wirtualnej z zarządzanymi dyskami</span><span class="sxs-lookup"><span data-stu-id="eec11-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="eec11-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eec11-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="eec11-217">Konto magazynu, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="eec11-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="eec11-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eec11-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="eec11-219">Użyj tego przełącznika, jeśli dyski z punktu odzyskiwania zostaną przywrócone do oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="eec11-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="eec11-220">-VaultId</span><span class="sxs-lookup"><span data-stu-id="eec11-220">-VaultId</span></span>

<span data-ttu-id="eec11-221">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="eec11-221">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="eec11-222">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="eec11-222">-VaultLocation</span></span>

<span data-ttu-id="eec11-223">Lokalizacja magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eec11-223">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="eec11-224">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="eec11-224">-WLRecoveryConfig</span></span>

<span data-ttu-id="eec11-225">Konfiguracja odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="eec11-225">Recovery config</span></span>

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

### <span data-ttu-id="eec11-226">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eec11-226">-Confirm</span></span>

<span data-ttu-id="eec11-227">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eec11-227">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec11-228">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec11-228">-WhatIf</span></span>

<span data-ttu-id="eec11-229">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eec11-229">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="eec11-230">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec11-230">CommonParameters</span></span>
<span data-ttu-id="eec11-231">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec11-231">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec11-232">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eec11-232">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec11-233">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eec11-233">INPUTS</span></span>

### <span data-ttu-id="eec11-234">System. String</span><span class="sxs-lookup"><span data-stu-id="eec11-234">System.String</span></span>

### <span data-ttu-id="eec11-235">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="eec11-235">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="eec11-236">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eec11-236">OUTPUTS</span></span>

### <span data-ttu-id="eec11-237">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="eec11-237">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="eec11-238">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eec11-238">NOTES</span></span>

## <span data-ttu-id="eec11-239">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eec11-239">RELATED LINKS</span></span>

[<span data-ttu-id="eec11-240">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="eec11-240">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="eec11-241">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="eec11-241">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="eec11-242">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="eec11-242">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
