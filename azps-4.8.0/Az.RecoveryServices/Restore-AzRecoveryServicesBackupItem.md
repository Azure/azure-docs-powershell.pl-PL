---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063842"
---
# <span data-ttu-id="89497-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89497-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="89497-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89497-102">SYNOPSIS</span></span>

<span data-ttu-id="89497-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="89497-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="89497-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89497-104">SYNTAX</span></span>

### <span data-ttu-id="89497-105">AzureVMParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89497-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89497-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="89497-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89497-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="89497-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89497-108">Opis</span><span class="sxs-lookup"><span data-stu-id="89497-108">DESCRIPTION</span></span>

<span data-ttu-id="89497-109">Polecenie cmdlet **Restore-AzRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="89497-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="89497-110">To polecenie cmdlet rozpoczyna przywracanie z magazynu usług Recovery Services na konto magazynu klienta.</span><span class="sxs-lookup"><span data-stu-id="89497-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="89497-111">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89497-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="89497-112">Po zakończeniu operacji przywracania przywracana jest przygotowana ilość dysków zarządzanych do grupy zasobów docelowych i informacji o konfiguracji na koncie magazynu klientów, należy utworzyć maszynę wirtualną i uruchomić ją.</span><span class="sxs-lookup"><span data-stu-id="89497-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="89497-113">Aby uzyskać więcej informacji, refter do innych możliwych zestawów parametrów i tekstu parametrów.</span><span class="sxs-lookup"><span data-stu-id="89497-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="89497-114">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="89497-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="89497-115">Uwaga: Aby pomyślnie wykonać to polecenie cmdlet (oprócz parametru-VaultId), należy również użyć parametru VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="89497-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="89497-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89497-116">EXAMPLES</span></span>

### <span data-ttu-id="89497-117">Przykład 1: Przywracanie elementu do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="89497-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="89497-118">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="89497-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="89497-119">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM z $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="89497-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="89497-120">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="89497-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="89497-121">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="89497-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="89497-122">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="89497-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="89497-123">Określony zakres dat to ostatnie 7 dni.</span><span class="sxs-lookup"><span data-stu-id="89497-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="89497-124">Polecenie siódme określa dyski, które mają zostać przywrócone z punktu odzyskiwania, i zapisuje je w zmiennej $restoreDiskLUNs.</span><span class="sxs-lookup"><span data-stu-id="89497-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="89497-125">Ostatnie polecenie przywraca dyski do docelowego konta magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="89497-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="89497-126">Przykład 2: Przywracanie wielu plików elementu AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="89497-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="89497-127">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="89497-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="89497-128">Drugie polecenie pobiera element kopii zapasowej o nazwie fileshareitem, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="89497-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="89497-129">W trzecim poleceniu jest pobierana lista punktów odzyskiwania dla określonego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="89497-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="89497-130">Czwarte polecenie spceifies, które pliki należy przywrócić i przechowywać w zmiennej $files.</span><span class="sxs-lookup"><span data-stu-id="89497-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="89497-131">Ostatnie polecenie przywraca określone pliki do pierwotnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="89497-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="89497-132">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="89497-132">Example 3</span></span>

<span data-ttu-id="89497-133">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="89497-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="89497-134">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="89497-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="89497-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89497-135">PARAMETERS</span></span>

### <span data-ttu-id="89497-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89497-136">-DefaultProfile</span></span>

<span data-ttu-id="89497-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89497-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89497-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="89497-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="89497-139">Służy do przywracania wielu plików z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="89497-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="89497-140">Ścieżki elementów, które mają zostać przywrócone w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="89497-140">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="89497-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="89497-141">-RecoveryPoint</span></span>

<span data-ttu-id="89497-142">Określa punkt odzyskiwania, do którego ma zostać przywrócony element kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="89497-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="89497-143">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="89497-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89497-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="89497-144">-ResolveConflict</span></span>

<span data-ttu-id="89497-145">W przypadku gdy przywrócony element istnieje również w miejscu docelowym, Użyj tej pozycji, aby wskazać, czy zastąpić go.</span><span class="sxs-lookup"><span data-stu-id="89497-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="89497-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89497-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89497-147">Zastąpić</span><span class="sxs-lookup"><span data-stu-id="89497-147">Overwrite</span></span>
- <span data-ttu-id="89497-148">Przeskok</span><span class="sxs-lookup"><span data-stu-id="89497-148">Skip</span></span>

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

### <span data-ttu-id="89497-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="89497-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="89497-150">Użyj tego przełącznika, aby określić przywracanie jako niezarządzanych dysków</span><span class="sxs-lookup"><span data-stu-id="89497-150">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="89497-151">-RestoreDiskList</span></span>
<span data-ttu-id="89497-152">Określanie dysków do odzyskania kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="89497-152">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="89497-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="89497-154">Użyj tego przełącznika, aby przywrócić tylko dyski systemu operacyjnego kopii zapasowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="89497-154">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="89497-155">-SourceFilePath</span></span>

<span data-ttu-id="89497-156">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="89497-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="89497-157">Ścieżka elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="89497-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="89497-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="89497-158">-SourceFileType</span></span>

<span data-ttu-id="89497-159">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="89497-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="89497-160">Typ elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="89497-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="89497-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89497-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89497-162">Plik</span><span class="sxs-lookup"><span data-stu-id="89497-162">File</span></span>
- <span data-ttu-id="89497-163">Directory</span><span class="sxs-lookup"><span data-stu-id="89497-163">Directory</span></span>

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

### <span data-ttu-id="89497-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89497-164">-StorageAccountName</span></span>

<span data-ttu-id="89497-165">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="89497-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="89497-166">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="89497-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89497-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="89497-168">Określa nazwę grupy zasobów zawierającej docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="89497-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="89497-169">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="89497-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="89497-170">-TargetFileShareName</span></span>

<span data-ttu-id="89497-171">Udział pliku, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="89497-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="89497-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="89497-172">-TargetFolder</span></span>

<span data-ttu-id="89497-173">Folder, w którym ma zostać przywrócony udział plików w TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="89497-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="89497-174">Jeśli kopia zapasowa zawartości ma zostać przywrócona do folderu głównego, wprowadź wartości w folderze docelowym jako ciąg pusty.</span><span class="sxs-lookup"><span data-stu-id="89497-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="89497-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89497-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="89497-176">Grupa zasobów, do której są przywracane zarządzane dyski.</span><span class="sxs-lookup"><span data-stu-id="89497-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="89497-177">Dotyczy kopii zapasowych maszyny wirtualnej z zarządzanymi dyskami</span><span class="sxs-lookup"><span data-stu-id="89497-177">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89497-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="89497-179">Konto magazynu, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="89497-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="89497-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89497-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="89497-181">Użyj tego przełącznika, jeśli dyski z punktu odzyskiwania zostaną przywrócone do oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="89497-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89497-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="89497-182">-VaultId</span></span>

<span data-ttu-id="89497-183">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="89497-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="89497-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="89497-184">-VaultLocation</span></span>

<span data-ttu-id="89497-185">Lokalizacja magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="89497-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="89497-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="89497-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="89497-187">Konfiguracja odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="89497-187">Recovery config</span></span>

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

### <span data-ttu-id="89497-188">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89497-188">-Confirm</span></span>

<span data-ttu-id="89497-189">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89497-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89497-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89497-190">-WhatIf</span></span>

<span data-ttu-id="89497-191">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89497-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="89497-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89497-192">CommonParameters</span></span>
<span data-ttu-id="89497-193">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89497-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89497-194">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89497-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89497-195">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89497-195">INPUTS</span></span>

### <span data-ttu-id="89497-196">System. String</span><span class="sxs-lookup"><span data-stu-id="89497-196">System.String</span></span>

### <span data-ttu-id="89497-197">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="89497-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="89497-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89497-198">OUTPUTS</span></span>

### <span data-ttu-id="89497-199">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="89497-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="89497-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89497-200">NOTES</span></span>

## <span data-ttu-id="89497-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89497-201">RELATED LINKS</span></span>

[<span data-ttu-id="89497-202">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89497-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="89497-203">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89497-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="89497-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="89497-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
