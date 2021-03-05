---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3ce18989f737a28cc0949027cb4ea827116b89a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963841"
---
# <span data-ttu-id="d1a2d-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1a2d-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d1a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a2d-102">SYNOPSIS</span></span>

<span data-ttu-id="d1a2d-103">Uruchamia kopię zapasową elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="d1a2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1a2d-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1a2d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1a2d-105">DESCRIPTION</span></span>

<span data-ttu-id="d1a2d-106">Polecenie **cmdlet Backup-AzRecoveryServicesBackupItem** pobiera dodatkową kopię zapasową chronionego elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="d1a2d-107">Za pomocą tego polecenia cmdlet możesz wykonać początkową kopię zapasową natychmiast po włączeniu ochrony lub uruchomić kopię zapasową, jeśli zaplanowana kopia zapasowa zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="d1a2d-108">To polecenie cmdlet może być również używane do niestandardowego przechowywania z datą wygaśnięcia lub bez tego terminu — aby uzyskać więcej szczegółowych informacji, zapoznaj się z tekstem pomocy parametrów.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="d1a2d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1a2d-109">EXAMPLES</span></span>

### <span data-ttu-id="d1a2d-110">Przykład 1. Uruchamianie kopii zapasowej elementu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="d1a2d-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="d1a2d-111">Pierwsze polecenie pobiera kontener kopii zapasowej typu AzureVM o nazwie pstestv2vm1, a następnie przechowuje go w $NamedContainer zmienną.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="d1a2d-112">Drugie polecenie pobiera element kopii zapasowej odpowiadający kontenerowi w $NamedContainer, a następnie przechowuje go w $Item danych.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="d1a2d-113">Ostatnie polecenie wyzwala zadanie kopii zapasowej dla elementu kopii zapasowej w programie $Item.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="d1a2d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d1a2d-114">Example 2</span></span>

<span data-ttu-id="d1a2d-115">Uruchamia kopię zapasową elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="d1a2d-116">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="d1a2d-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="d1a2d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a2d-117">PARAMETERS</span></span>

### <span data-ttu-id="d1a2d-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="d1a2d-118">-BackupType</span></span>

<span data-ttu-id="d1a2d-119">Typ kopii zapasowej do wykonania</span><span class="sxs-lookup"><span data-stu-id="d1a2d-119">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a2d-120">-DefaultProfile</span></span>

<span data-ttu-id="d1a2d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a2d-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="d1a2d-122">-EnableCompression</span></span>

<span data-ttu-id="d1a2d-123">Jeśli jest wymagane włączenie kompresji</span><span class="sxs-lookup"><span data-stu-id="d1a2d-123">If enabling compression is required</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a2d-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="d1a2d-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="d1a2d-125">Określa czas wygaśnięcia punktu odzyskiwania jako obiektu DateTime, jeśli nic nie zostanie podane, przyjmuje wartość domyślną 30 dni.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="d1a2d-126">Dotyczy maszyny wirtualnej, języka SQL (tylko kopię typu kopii zapasowej z pełną kopią), elementów kopii zapasowej AFS.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a2d-127">— element</span><span class="sxs-lookup"><span data-stu-id="d1a2d-127">-Item</span></span>

<span data-ttu-id="d1a2d-128">Określa element kopii zapasowej, dla którego to polecenie cmdlet uruchamia operację tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a2d-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d1a2d-129">-VaultId</span></span>

<span data-ttu-id="d1a2d-130">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d1a2d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1a2d-131">-Confirm</span></span>

<span data-ttu-id="d1a2d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a2d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a2d-133">-WhatIf</span></span>

<span data-ttu-id="d1a2d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="d1a2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a2d-135">CommonParameters</span></span>
<span data-ttu-id="d1a2d-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a2d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1a2d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a2d-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1a2d-138">INPUTS</span></span>

### <span data-ttu-id="d1a2d-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="d1a2d-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d1a2d-140">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d1a2d-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d1a2d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d1a2d-141">System.String</span></span>

## <span data-ttu-id="d1a2d-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1a2d-142">OUTPUTS</span></span>

### <span data-ttu-id="d1a2d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="d1a2d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d1a2d-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1a2d-144">NOTES</span></span>

## <span data-ttu-id="d1a2d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1a2d-145">RELATED LINKS</span></span>

[<span data-ttu-id="d1a2d-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d1a2d-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="d1a2d-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1a2d-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="d1a2d-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1a2d-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
