---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526685"
---
# <span data-ttu-id="a0f0e-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a0f0e-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a0f0e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f0e-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f0e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0f0e-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f0e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f0e-106">Polecenie cmdlet **Restore-AzureRmRecoveryServicesBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="a0f0e-107">To polecenie cmdlet rozpoczyna przywracanie z magazynu usług Recovery Services na konto magazynu klienta.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="a0f0e-108">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="a0f0e-109">Przywraca dane dyskowe i informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="a0f0e-110">Po zakończeniu operacji przywracania musisz utworzyć maszynę wirtualną i ją uruchomić.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="a0f0e-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a0f0e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0f0e-112">EXAMPLES</span></span>

### <span data-ttu-id="a0f0e-113">Przykład 1: Przywracanie elementu do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="a0f0e-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="a0f0e-114">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="a0f0e-115">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM z $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="a0f0e-116">Trzecia wersja polecenia otrzymuje datę z siedmiu dni, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="a0f0e-117">W czwartym poleceniu jest pobierana bieżąca data, a następnie przechowywana w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="a0f0e-118">W piątym poleceniu jest pobierana lista punktów odzyskiwania dla konkretnego elementu kopii zapasowej filtrowanego przez $StartDate i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="a0f0e-119">Określony zakres dat to ostatnie 7 dni.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="a0f0e-120">Ostatnie polecenie przywraca dyski do docelowego konta magazynu DestAccount w grupie zasobów DestRG.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="a0f0e-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0f0e-121">PARAMETERS</span></span>

### <span data-ttu-id="a0f0e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f0e-122">-DefaultProfile</span></span>
<span data-ttu-id="a0f0e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-124">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a0f0e-124">-RecoveryPoint</span></span>
<span data-ttu-id="a0f0e-125">Określa punkt odzyskiwania, do którego ma zostać przywrócona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-125">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="a0f0e-126">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-126">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a0f0e-127">-StorageAccountName</span></span>
<span data-ttu-id="a0f0e-128">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-128">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="a0f0e-129">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-129">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-130">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f0e-130">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="a0f0e-131">Określa nazwę grupy zasobów zawierającej docelowe konto magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-131">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="a0f0e-132">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-132">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-133">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0f0e-133">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="a0f0e-134">Użyj tego przełącznika, jeśli dyski z punktu odzyskiwania zostaną przywrócone do oryginalnych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-134">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0f0e-135">-Confirm</span></span>
<span data-ttu-id="a0f0e-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f0e-137">-WhatIf</span></span>
<span data-ttu-id="a0f0e-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0f0e-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f0e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f0e-140">CommonParameters</span></span>
<span data-ttu-id="a0f0e-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f0e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f0e-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f0e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f0e-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0f0e-143">INPUTS</span></span>

### <span data-ttu-id="a0f0e-144">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a0f0e-144">RecoveryPointBase</span></span>
<span data-ttu-id="a0f0e-145">Parametr "RecoveryPoint" akceptuje wartość typu "RecoveryPointBase" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a0f0e-145">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="a0f0e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0f0e-146">OUTPUTS</span></span>

### <span data-ttu-id="a0f0e-147">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a0f0e-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a0f0e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0f0e-148">NOTES</span></span>

## <span data-ttu-id="a0f0e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0f0e-149">RELATED LINKS</span></span>

[<span data-ttu-id="a0f0e-150">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a0f0e-150">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="a0f0e-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a0f0e-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="a0f0e-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a0f0e-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


