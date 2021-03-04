---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3d3cbb196a287e24837c0e7b0e61b16eaa06ce95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997508"
---
# <span data-ttu-id="e3b93-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e3b93-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e3b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b93-102">SYNOPSIS</span></span>

<span data-ttu-id="e3b93-103">Przywraca dane i konfigurację elementu kopii zapasowej do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3b93-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="e3b93-104">Wymagane parametry różnią się w zależności od typu elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e3b93-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="e3b93-105">To samo polecenie jest używane do przywracania maszyn wirtualnych platformy Azure, baz danych działających w ramach maszyn wirtualnych platformy Azure oraz udziałów plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b93-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="e3b93-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3b93-106">SYNTAX</span></span>

### <span data-ttu-id="e3b93-107">AzureVMParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e3b93-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b93-108">AzureVMManagedMeterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b93-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b93-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="e3b93-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b93-110">AzureVMUnManagedMeterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b93-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b93-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b93-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b93-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b93-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b93-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3b93-113">DESCRIPTION</span></span>

<span data-ttu-id="e3b93-114">Polecenie cmdlet **Restore-AzRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3b93-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="e3b93-115">**Kopia zapasowa maszyn wirtualnych platformy Azure**</span><span class="sxs-lookup"><span data-stu-id="e3b93-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="e3b93-116">Za pomocą tego polecenia możesz utworzyć kopię zapasową maszyn wirtualnych platformy Azure i przywrócić dyskietki (zarówno zarządzane, jak i nieza zarządzane).</span><span class="sxs-lookup"><span data-stu-id="e3b93-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="e3b93-117">Operacja przywracania nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3b93-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="e3b93-118">Jeśli jest to zarządzana dyskowa maszyny wirtualnej, należy określić grupę zasobów docelowych, w której przechowywane są przywrócone dyskietki.</span><span class="sxs-lookup"><span data-stu-id="e3b93-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="e3b93-119">Jeśli określono grupę zasobów docelowych, jeśli migawki znajdują się w grupie zasobów wskazanej w zasadach kopii zapasowej, operacja przywracania będzie natychmiastowa, a dyskrówna zostanie utworzona na podstawie lokalnych migawek i będzie przechowywana w grupie zasobów docelowych.</span><span class="sxs-lookup"><span data-stu-id="e3b93-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="e3b93-120">Można również przywrócić je jako dyskietki nieza zarządzanie, ale spowoduje to wykorzystanie danych obecnych w magazynie usług odzyskiwania platformy Azure, przez co będzie znacznie wolniejsze.</span><span class="sxs-lookup"><span data-stu-id="e3b93-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="e3b93-121">Konfiguracja maszyny wirtualnej i szablonu wdrożenia, którego można użyć do utworzenia maszyny wirtualnej z przywróconego dyskietki, zostaną pobrane na określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3b93-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="e3b93-122">Jeśli jest to nie zarządzana dyskowa maszyny wirtualnej, migawki są obecne w oryginalnym koncie magazynu dysku i/lub w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3b93-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="e3b93-123">Jeśli użytkownik udostępnia opcję przywracania przy użyciu oryginalnego konta magazynu, można błyskawicznie przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="e3b93-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="e3b93-124">W przeciwnym razie dane są pobierane z magazynu usług Azure Recovery, a dysk dyskowe są tworzone w określonym koncie magazynu wraz z konfiguracją maszyny wirtualnej i szablonu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e3b93-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3b93-125">Domyślnie kopia zapasowa maszyn wirtualnych platformy Azure jest kopią zapasową wszystkich dysków.</span><span class="sxs-lookup"><span data-stu-id="e3b93-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="e3b93-126">Podczas włączania kopii zapasowej można selektywnie utworzyć kopię zapasową odpowiednich dysków, używając parametrów Lista wykluczeń lub Lista Dołączeń.</span><span class="sxs-lookup"><span data-stu-id="e3b93-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="e3b93-127">Opcja selektywnego przywracania dysków jest dostępna tylko wtedy, gdy jedna z nich selektywnie zbęduje kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="e3b93-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="e3b93-128">Aby uzyskać więcej informacji, zapoznaj się z różnymi możliwymi zestawami parametrów i tekstem parametrów.</span><span class="sxs-lookup"><span data-stu-id="e3b93-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="e3b93-129">Jeśli jest używany parametr -VaultId, wówczas powinien być również używany parametr -VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="e3b93-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="e3b93-130">**Kopia zapasowa udostępniania plików platformy Azure**</span><span class="sxs-lookup"><span data-stu-id="e3b93-130">**For Azure File share backup**</span></span>

<span data-ttu-id="e3b93-131">Możesz przywrócić cały udział plików lub określone/wiele plików/folderów w danym udostępniniu.</span><span class="sxs-lookup"><span data-stu-id="e3b93-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="e3b93-132">Możesz przywrócić pierwotną lokalizację lub lokalizację alternatywną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="e3b93-133">**W przypadku obciążeń pracą na platformie Azure**</span><span class="sxs-lookup"><span data-stu-id="e3b93-133">**For Azure Workloads**</span></span>

<span data-ttu-id="e3b93-134">Możesz przywrócić bazy danych SQL DB w ramach maszyn wirtualnych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e3b93-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="e3b93-135">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3b93-135">EXAMPLES</span></span>

### <span data-ttu-id="e3b93-136">Przykład 1. Przywracanie dysków z kopią zapasową zarządzanej maszyny wirtualnej Azure z danego punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="e3b93-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="e3b93-137">Pierwsze polecenie pobiera magazyn usług odzyskiwania i przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="e3b93-138">Drugie polecenie pobiera element kopii zapasowej typu AzureVM o nazwie "V2VM" i przechowuje go w $BackupItem danych.</span><span class="sxs-lookup"><span data-stu-id="e3b93-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e3b93-139">Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e3b93-140">Czwarte polecenie pobiera bieżącą datę, a następnie zapisuje je w $EndDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e3b93-141">Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="e3b93-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="e3b93-142">Ostatnie polecenie przywraca wszystkie dyskietki w docelowej grupie zasobów Target_RG, a następnie udostępnia informacje o konfiguracji maszyny wirtualnej i szablon wdrożenia w koncie magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="e3b93-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="e3b93-143">Przykład 2. Przywracanie określonego dysku zapasowego zarządzanej maszyny wirtualnej Azure z danego punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="e3b93-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="e3b93-144">Pierwsze polecenie pobiera magazyn usług odzyskiwania i przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="e3b93-145">Drugie polecenie pobiera element kopii zapasowej typu AzureVM o nazwie "V2VM" i przechowuje go w $BackupItem danych.</span><span class="sxs-lookup"><span data-stu-id="e3b93-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e3b93-146">Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e3b93-147">Czwarte polecenie pobiera bieżącą datę, a następnie zapisuje je w $EndDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e3b93-148">Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="e3b93-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="e3b93-149">Szóste polecenie przechowuje listę dysków, które mają zostać przywrócone, w zmiennej restore InformacjeOkichi.</span><span class="sxs-lookup"><span data-stu-id="e3b93-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="e3b93-150">Ostatnie polecenie przywraca wskazane dyskietki z określonych luns, do grupy zasobów docelowych Target_RG, a następnie udostępnia informacje o konfiguracji maszyny wirtualnej i szablon wdrożenia w koncie magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="e3b93-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="e3b93-151">Przykład 3. Przywracanie dysków zarządzanej maszyny wirtualnej jako niezamanektowana dyskietki</span><span class="sxs-lookup"><span data-stu-id="e3b93-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="e3b93-152">Pierwsze polecenie pobiera magazyn RecoveryServices i przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="e3b93-153">Drugie polecenie pobiera element kopii zapasowej, a następnie przechowuje go w $BackupItem danych.</span><span class="sxs-lookup"><span data-stu-id="e3b93-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e3b93-154">Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e3b93-155">Czwarte polecenie pobiera bieżącą datę, a następnie zapisuje je w $EndDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e3b93-156">Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="e3b93-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="e3b93-157">Szóste polecenie przywraca dyskietki jako niezamanektowane dyskietki.</span><span class="sxs-lookup"><span data-stu-id="e3b93-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="e3b93-158">Przykład 4. Przywracanie niezamanektowej maszyny wirtualnej jako niezamanektowana dyskietki przy użyciu oryginalnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e3b93-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="e3b93-159">Pierwsze polecenie pobiera magazyn RecoveryServices i przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="e3b93-160">Drugie polecenie pobiera element kopii zapasowej, a następnie przechowuje go w $BackupItem danych.</span><span class="sxs-lookup"><span data-stu-id="e3b93-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e3b93-161">Trzecie polecenie pobiera datę z siedmiu dni wcześniej, a następnie przechowuje ją w $StartDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e3b93-162">Czwarte polecenie pobiera bieżącą datę, a następnie zapisuje je w $EndDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e3b93-163">Piąte polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej filtrowanych według $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="e3b93-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="e3b93-164">Szóste polecenie przywraca dyskietki jako niezamanektowane dyskietki do ich oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3b93-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="e3b93-165">Przykład 5. Przywracanie wielu plików elementu AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e3b93-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="e3b93-166">Pierwsze polecenie pobiera magazyn usług odzyskiwania i przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="e3b93-167">Drugie polecenie pobiera element kopii zapasowej o nazwie fileshareitem i zapisuje go w $BackupItem pliku.</span><span class="sxs-lookup"><span data-stu-id="e3b93-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e3b93-168">Trzecie polecenie otrzymuje listę punktów odzyskiwania dla określonego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e3b93-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="e3b93-169">Czwarte polecenie określa, które pliki mają zostać przywrócone i przechowywane w $files zmienną.</span><span class="sxs-lookup"><span data-stu-id="e3b93-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="e3b93-170">Ostatnie polecenie przywraca wskazane pliki do pierwotnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e3b93-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="e3b93-171">Przykład 6. Przywracanie bazy danych SQL w usłudze Azure VM do innej docelowej maszyny wirtualnej w celu pełnego punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="e3b93-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="e3b93-172">Przykład 7. Przywracanie bazy danych SQL w usłudze Azure VM do innej docelowej maszyny wirtualnej dla punktu odzyskiwania dziennika</span><span class="sxs-lookup"><span data-stu-id="e3b93-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="e3b93-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3b93-173">PARAMETERS</span></span>

### <span data-ttu-id="e3b93-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b93-174">-DefaultProfile</span></span>

<span data-ttu-id="e3b93-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b93-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b93-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="e3b93-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="e3b93-177">Służy do przywracania wielu plików z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="e3b93-178">Ścieżki elementów, które mają zostać przywrócone w ramach udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="e3b93-179">- RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e3b93-179">-RecoveryPoint</span></span>

<span data-ttu-id="e3b93-180">Określa punkt odzyskiwania, do którego ma zostać przywrócony element kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e3b93-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="e3b93-181">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint.**</span><span class="sxs-lookup"><span data-stu-id="e3b93-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="e3b93-182">- ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="e3b93-182">-ResolveConflict</span></span>

<span data-ttu-id="e3b93-183">Jeśli przywrócony element także istnieje w lokalizacji docelowej, skorzystaj z tej informacji, aby wskazać, czy chcesz zastąpić element, czy nie.</span><span class="sxs-lookup"><span data-stu-id="e3b93-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="e3b93-184">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e3b93-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3b93-185">Zastąp</span><span class="sxs-lookup"><span data-stu-id="e3b93-185">Overwrite</span></span>
- <span data-ttu-id="e3b93-186">Pomiń</span><span class="sxs-lookup"><span data-stu-id="e3b93-186">Skip</span></span>

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

### <span data-ttu-id="e3b93-187">-RestoreAsUnmanaged Jednakowe</span><span class="sxs-lookup"><span data-stu-id="e3b93-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="e3b93-188">Użyj tego przełącznika, aby określić, że przywracana jest dyskietki niezamanektowane</span><span class="sxs-lookup"><span data-stu-id="e3b93-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="e3b93-189">-Restore WymusznaLista</span><span class="sxs-lookup"><span data-stu-id="e3b93-189">-RestoreDiskList</span></span>
<span data-ttu-id="e3b93-190">Określanie dyskietki do odzyskania kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3b93-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="e3b93-191">-RestoreOnlyOS Jednakowa</span><span class="sxs-lookup"><span data-stu-id="e3b93-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="e3b93-192">Użyj tego przełącznika, aby przywrócić tylko dyski systemu operacyjnego kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3b93-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="e3b93-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="e3b93-193">-SourceFilePath</span></span>

<span data-ttu-id="e3b93-194">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="e3b93-195">Ścieżka elementu, który ma zostać przywrócony w ramach udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="e3b93-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="e3b93-196">-SourceFileType</span></span>

<span data-ttu-id="e3b93-197">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="e3b93-198">Typ elementu, który ma zostać przywrócony w ramach udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="e3b93-199">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e3b93-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3b93-200">Plik</span><span class="sxs-lookup"><span data-stu-id="e3b93-200">File</span></span>
- <span data-ttu-id="e3b93-201">Katalog</span><span class="sxs-lookup"><span data-stu-id="e3b93-201">Directory</span></span>

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

### <span data-ttu-id="e3b93-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3b93-202">-StorageAccountName</span></span>

<span data-ttu-id="e3b93-203">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e3b93-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="e3b93-204">W ramach procesu przywracania to polecenie cmdlet przechowuje informacje o dyskach i konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3b93-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="e3b93-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b93-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="e3b93-206">Określa nazwę grupy zasobów, która zawiera docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e3b93-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="e3b93-207">W ramach procesu przywracania to polecenie cmdlet przechowuje informacje o dyskach i konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3b93-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="e3b93-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="e3b93-208">-TargetFileShareName</span></span>

<span data-ttu-id="e3b93-209">Udział plików, do którego należy przywrócić udział plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="e3b93-210">- TargetFolder</span><span class="sxs-lookup"><span data-stu-id="e3b93-210">-TargetFolder</span></span>

<span data-ttu-id="e3b93-211">Folder, w którym należy przywrócić udział plików, w obrębie parametru TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="e3b93-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="e3b93-212">Jeśli zawartość kopii zapasowej ma zostać przywrócona do folderu głównego, nadaj wartości folderu docelowego jako pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="e3b93-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="e3b93-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b93-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="e3b93-214">Grupa zasobów, do której przywracane są zarządzane dyskietki.</span><span class="sxs-lookup"><span data-stu-id="e3b93-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="e3b93-215">Dotyczy kopii zapasowej maszyny wirtualnej z zarządzanymi dyskami</span><span class="sxs-lookup"><span data-stu-id="e3b93-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="e3b93-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3b93-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="e3b93-217">Konto magazynu, do którego należy przywrócić udział plików.</span><span class="sxs-lookup"><span data-stu-id="e3b93-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="e3b93-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3b93-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="e3b93-219">Użyj tego przełącznika, jeśli dyskietki z punktu odzyskiwania mają zostać przywrócone do ich oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3b93-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="e3b93-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e3b93-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="e3b93-221">Identyfikator DES do szyfrowania przywracanych dysków.</span><span class="sxs-lookup"><span data-stu-id="e3b93-221">The DES ID to encrypt the restored disks.</span></span>

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

### <span data-ttu-id="e3b93-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="e3b93-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="e3b93-223">Użyj tego przełącznika, aby wyzwolić przywracanie regionu krzyżowego do regionu pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="e3b93-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

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

### <span data-ttu-id="e3b93-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e3b93-224">-VaultId</span></span>

<span data-ttu-id="e3b93-225">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3b93-225">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e3b93-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="e3b93-226">-VaultLocation</span></span>

<span data-ttu-id="e3b93-227">Lokalizacja magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3b93-227">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e3b93-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="e3b93-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="e3b93-229">Konfiguracja odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="e3b93-229">Recovery config</span></span>

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

### <span data-ttu-id="e3b93-230">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3b93-230">-Confirm</span></span>

<span data-ttu-id="e3b93-231">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3b93-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b93-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b93-232">-WhatIf</span></span>

<span data-ttu-id="e3b93-233">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b93-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="e3b93-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b93-234">CommonParameters</span></span>
<span data-ttu-id="e3b93-235">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b93-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b93-236">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3b93-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b93-237">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3b93-237">INPUTS</span></span>

### <span data-ttu-id="e3b93-238">System.String</span><span class="sxs-lookup"><span data-stu-id="e3b93-238">System.String</span></span>

### <span data-ttu-id="e3b93-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="e3b93-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="e3b93-240">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3b93-240">OUTPUTS</span></span>

### <span data-ttu-id="e3b93-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="e3b93-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e3b93-242">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3b93-242">NOTES</span></span>

## <span data-ttu-id="e3b93-243">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3b93-243">RELATED LINKS</span></span>

[<span data-ttu-id="e3b93-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e3b93-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e3b93-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e3b93-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e3b93-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e3b93-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
