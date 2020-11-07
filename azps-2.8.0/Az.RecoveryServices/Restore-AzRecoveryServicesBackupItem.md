---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872599"
---
# <span data-ttu-id="87c29-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="87c29-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="87c29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87c29-102">SYNOPSIS</span></span>

<span data-ttu-id="87c29-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="87c29-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="87c29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87c29-104">SYNTAX</span></span>

### <span data-ttu-id="87c29-105">AzureVMParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87c29-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c29-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="87c29-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87c29-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="87c29-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c29-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87c29-108">DESCRIPTION</span></span>

<span data-ttu-id="87c29-109">Polecenie cmdlet **Restore-AzRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="87c29-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="87c29-110">To polecenie cmdlet rozpoczyna przywracanie z magazynu usług Recovery Services na konto magazynu klienta.</span><span class="sxs-lookup"><span data-stu-id="87c29-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="87c29-111">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87c29-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="87c29-112">Przywraca dane dyskowe i informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="87c29-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="87c29-113">Po zakończeniu operacji przywracania musisz utworzyć maszynę wirtualną i ją uruchomić.</span><span class="sxs-lookup"><span data-stu-id="87c29-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="87c29-114">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="87c29-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="87c29-115">Uwaga: Aby pomyślnie wykonać to polecenie cmdlet (oprócz parametru-VaultId), należy również użyć parametru VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="87c29-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="87c29-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87c29-116">EXAMPLES</span></span>

### <span data-ttu-id="87c29-117">Przykład 1: Przywracanie elementu do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="87c29-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="87c29-118">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="87c29-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="87c29-119">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM z $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="87c29-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="87c29-120">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="87c29-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="87c29-121">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="87c29-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="87c29-122">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="87c29-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="87c29-123">Określony zakres dat to ostatnie 7 dni.</span><span class="sxs-lookup"><span data-stu-id="87c29-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="87c29-124">Ostatnie polecenie przywraca dyski do docelowego konta magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="87c29-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="87c29-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87c29-125">PARAMETERS</span></span>

### <span data-ttu-id="87c29-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c29-126">-DefaultProfile</span></span>

<span data-ttu-id="87c29-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87c29-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c29-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="87c29-128">-RecoveryPoint</span></span>

<span data-ttu-id="87c29-129">Określa punkt odzyskiwania, do którego ma zostać przywrócona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="87c29-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="87c29-130">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="87c29-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="87c29-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="87c29-131">-ResolveConflict</span></span>

<span data-ttu-id="87c29-132">W przypadku gdy przywrócony element istnieje również w miejscu docelowym, Użyj tej pozycji, aby wskazać, czy zastąpić go.</span><span class="sxs-lookup"><span data-stu-id="87c29-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="87c29-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="87c29-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87c29-134">Zastąpić</span><span class="sxs-lookup"><span data-stu-id="87c29-134">Overwrite</span></span>
- <span data-ttu-id="87c29-135">Przeskok</span><span class="sxs-lookup"><span data-stu-id="87c29-135">Skip</span></span>

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

### <span data-ttu-id="87c29-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="87c29-136">-SourceFilePath</span></span>

<span data-ttu-id="87c29-137">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="87c29-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="87c29-138">Ścieżka elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="87c29-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="87c29-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="87c29-139">-SourceFileType</span></span>

<span data-ttu-id="87c29-140">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="87c29-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="87c29-141">Typ elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="87c29-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="87c29-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="87c29-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87c29-143">Plik</span><span class="sxs-lookup"><span data-stu-id="87c29-143">File</span></span>
- <span data-ttu-id="87c29-144">Directory</span><span class="sxs-lookup"><span data-stu-id="87c29-144">Directory</span></span>

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

### <span data-ttu-id="87c29-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87c29-145">-StorageAccountName</span></span>

<span data-ttu-id="87c29-146">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87c29-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="87c29-147">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="87c29-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="87c29-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c29-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="87c29-149">Określa nazwę grupy zasobów zawierającej docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87c29-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="87c29-150">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="87c29-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="87c29-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="87c29-151">-TargetFileShareName</span></span>

<span data-ttu-id="87c29-152">Udział pliku, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="87c29-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="87c29-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="87c29-153">-TargetFolder</span></span>

<span data-ttu-id="87c29-154">Folder, w którym ma zostać przywrócony udział plików w TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="87c29-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="87c29-155">Jeśli kopia zapasowa zawartości ma zostać przywrócona do folderu głównego, wprowadź wartości w folderze docelowym jako ciąg pusty.</span><span class="sxs-lookup"><span data-stu-id="87c29-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="87c29-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c29-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="87c29-157">Grupa zasobów, do której są przywracane zarządzane dyski.</span><span class="sxs-lookup"><span data-stu-id="87c29-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="87c29-158">Dotyczy kopii zapasowych maszyny wirtualnej z zarządzanymi dyskami</span><span class="sxs-lookup"><span data-stu-id="87c29-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="87c29-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87c29-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="87c29-160">Konto magazynu, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="87c29-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="87c29-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87c29-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="87c29-162">Użyj tego przełącznika, jeśli dyski z punktu odzyskiwania zostaną przywrócone do oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="87c29-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="87c29-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="87c29-163">-VaultId</span></span>

<span data-ttu-id="87c29-164">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="87c29-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="87c29-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="87c29-165">-VaultLocation</span></span>

<span data-ttu-id="87c29-166">Lokalizacja magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="87c29-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="87c29-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="87c29-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="87c29-168">Konfiguracja odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="87c29-168">Recovery config</span></span>

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

### <span data-ttu-id="87c29-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87c29-169">-Confirm</span></span>

<span data-ttu-id="87c29-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c29-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c29-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c29-171">-WhatIf</span></span>

<span data-ttu-id="87c29-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c29-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87c29-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87c29-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c29-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c29-174">-CommonParameters</span></span>

<span data-ttu-id="87c29-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c29-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c29-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87c29-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c29-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87c29-177">INPUTS</span></span>

### <span data-ttu-id="87c29-178">System. String</span><span class="sxs-lookup"><span data-stu-id="87c29-178">System.String</span></span>

### <span data-ttu-id="87c29-179">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="87c29-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="87c29-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87c29-180">OUTPUTS</span></span>

### <span data-ttu-id="87c29-181">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="87c29-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="87c29-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87c29-182">NOTES</span></span>

## <span data-ttu-id="87c29-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87c29-183">RELATED LINKS</span></span>

[<span data-ttu-id="87c29-184">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="87c29-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="87c29-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="87c29-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="87c29-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="87c29-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
