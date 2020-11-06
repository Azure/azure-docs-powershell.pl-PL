---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524329"
---
# <span data-ttu-id="5f836-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5f836-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5f836-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f836-102">SYNOPSIS</span></span>
<span data-ttu-id="5f836-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5f836-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f836-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f836-104">SYNTAX</span></span>

### <span data-ttu-id="5f836-105">AzureVMParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f836-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f836-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f836-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f836-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5f836-107">DESCRIPTION</span></span>
<span data-ttu-id="5f836-108">Polecenie cmdlet **Restore-AzureRmRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5f836-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="5f836-109">To polecenie cmdlet rozpoczyna przywracanie z magazynu usług Recovery Services na konto magazynu klienta.</span><span class="sxs-lookup"><span data-stu-id="5f836-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="5f836-110">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5f836-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="5f836-111">Przywraca dane dyskowe i informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="5f836-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="5f836-112">Po zakończeniu operacji przywracania musisz utworzyć maszynę wirtualną i ją uruchomić.</span><span class="sxs-lookup"><span data-stu-id="5f836-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="5f836-113">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="5f836-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5f836-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f836-114">EXAMPLES</span></span>

### <span data-ttu-id="5f836-115">Przykład 1: Przywracanie elementu do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="5f836-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="5f836-116">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="5f836-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5f836-117">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM z $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5f836-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5f836-118">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="5f836-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5f836-119">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5f836-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5f836-120">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5f836-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5f836-121">Określony zakres dat to ostatnie 7 dni.</span><span class="sxs-lookup"><span data-stu-id="5f836-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="5f836-122">Ostatnie polecenie przywraca dyski do docelowego konta magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="5f836-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="5f836-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f836-123">PARAMETERS</span></span>

### <span data-ttu-id="5f836-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f836-124">-DefaultProfile</span></span>
<span data-ttu-id="5f836-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f836-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f836-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5f836-126">-RecoveryPoint</span></span>
<span data-ttu-id="5f836-127">Określa punkt odzyskiwania, do którego ma zostać przywrócona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="5f836-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="5f836-128">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="5f836-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f836-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="5f836-129">-ResolveConflict</span></span>
<span data-ttu-id="5f836-130">W przypadku gdy przywrócony element istnieje również w miejscu docelowym, Użyj tej pozycji, aby wskazać, czy zastąpić go.</span><span class="sxs-lookup"><span data-stu-id="5f836-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f836-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5f836-131">-SourceFilePath</span></span>
<span data-ttu-id="5f836-132">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="5f836-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5f836-133">Ścieżka elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="5f836-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="5f836-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="5f836-134">-SourceFileType</span></span>
<span data-ttu-id="5f836-135">Służy do przywracania określonego elementu z udziału plików.</span><span class="sxs-lookup"><span data-stu-id="5f836-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5f836-136">Ścieżka elementu, który ma zostać przywrócony w udziale plików.</span><span class="sxs-lookup"><span data-stu-id="5f836-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f836-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5f836-137">-StorageAccountName</span></span>
<span data-ttu-id="5f836-138">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5f836-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="5f836-139">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f836-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f836-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f836-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="5f836-141">Określa nazwę grupy zasobów zawierającej docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5f836-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="5f836-142">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f836-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f836-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="5f836-143">-TargetFileShareName</span></span>
<span data-ttu-id="5f836-144">Udział pliku, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="5f836-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5f836-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="5f836-145">-TargetFolder</span></span>
<span data-ttu-id="5f836-146">Folder, w którym ma zostać przywrócony udział plików w targetFileShareName. Zostaw zmienną pustą, aby przywrócić ją w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="5f836-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="5f836-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f836-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="5f836-148">Grupa zasobów, do której są przywracane zarządzane dyski.</span><span class="sxs-lookup"><span data-stu-id="5f836-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="5f836-149">Dotyczy kopii zapasowych maszyny wirtualnej z zarządzanymi dyskami</span><span class="sxs-lookup"><span data-stu-id="5f836-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="5f836-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5f836-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="5f836-151">Konto magazynu, do którego ma zostać przywrócony udział plików.</span><span class="sxs-lookup"><span data-stu-id="5f836-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5f836-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5f836-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="5f836-153">Użyj tego przełącznika, jeśli dyski z punktu odzyskiwania zostaną przywrócone do oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f836-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="5f836-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5f836-154">-VaultId</span></span>
<span data-ttu-id="5f836-155">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5f836-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5f836-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="5f836-156">-VaultLocation</span></span>
<span data-ttu-id="5f836-157">Lokalizacja magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5f836-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5f836-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f836-158">-Confirm</span></span>
<span data-ttu-id="5f836-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f836-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f836-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f836-160">-WhatIf</span></span>
<span data-ttu-id="5f836-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f836-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f836-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f836-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f836-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f836-163">CommonParameters</span></span>
<span data-ttu-id="5f836-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f836-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f836-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f836-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f836-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f836-166">INPUTS</span></span>

### <span data-ttu-id="5f836-167">System. String</span><span class="sxs-lookup"><span data-stu-id="5f836-167">System.String</span></span>
<span data-ttu-id="5f836-168">Parametry: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f836-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="5f836-169">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5f836-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="5f836-170">Parametry: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f836-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="5f836-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f836-171">OUTPUTS</span></span>

### <span data-ttu-id="5f836-172">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5f836-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5f836-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f836-173">NOTES</span></span>

## <span data-ttu-id="5f836-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f836-174">RELATED LINKS</span></span>

[<span data-ttu-id="5f836-175">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5f836-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5f836-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5f836-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5f836-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5f836-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


