---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490813"
---
# <span data-ttu-id="b368a-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b368a-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b368a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b368a-102">SYNOPSIS</span></span>

<span data-ttu-id="b368a-103">Rozpoczyna tworzenie kopii zapasowej elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b368a-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="b368a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b368a-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b368a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b368a-105">DESCRIPTION</span></span>

<span data-ttu-id="b368a-106">Polecenie cmdlet **Backup-AzRecoveryServicesBackupItem** pobiera kopię zapasową chronionego elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b368a-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="b368a-107">Za pomocą tego polecenia cmdlet możesz wykonać wstępną kopię zapasową natychmiast po włączeniu ochrony lub uruchomieniu kopii zapasowej w przypadku niepowodzenia zaplanowanej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b368a-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="b368a-108">To polecenie cmdlet może być również używane do przechowywania niestandardowych danych z datą wygaśnięcia lub bez nich — informacje na temat parametrów można znaleźć w tekście pomocy.</span><span class="sxs-lookup"><span data-stu-id="b368a-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="b368a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b368a-109">EXAMPLES</span></span>

### <span data-ttu-id="b368a-110">Przykład 1. Rozpoczynanie wykonywania kopii zapasowej elementu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b368a-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="b368a-111">Pierwsze polecenie pobiera kontener kopii zapasowych typu AzureVM o nazwie pstestv2vm1, a następnie zapisuje go w zmiennej $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="b368a-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="b368a-112">Drugie polecenie pobiera element kopii zapasowej odpowiadający kontenerowi w $NamedContainer, a następnie zapisuje go w zmiennej $Item.</span><span class="sxs-lookup"><span data-stu-id="b368a-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="b368a-113">Ostatnie polecenie wyzwala zadanie kopii zapasowej dla elementu kopii zapasowej w $Item.</span><span class="sxs-lookup"><span data-stu-id="b368a-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="b368a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b368a-114">Example 2</span></span>

<span data-ttu-id="b368a-115">Rozpoczyna tworzenie kopii zapasowej elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b368a-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="b368a-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="b368a-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="b368a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b368a-117">PARAMETERS</span></span>

### <span data-ttu-id="b368a-118">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="b368a-118">-BackupType</span></span>

<span data-ttu-id="b368a-119">Typ kopii zapasowej do wykonania</span><span class="sxs-lookup"><span data-stu-id="b368a-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="b368a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b368a-120">-DefaultProfile</span></span>

<span data-ttu-id="b368a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b368a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b368a-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="b368a-122">-EnableCompression</span></span>

<span data-ttu-id="b368a-123">Jeśli jest wymagane włączenie kompresji</span><span class="sxs-lookup"><span data-stu-id="b368a-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="b368a-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="b368a-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="b368a-125">Określa czas wygaśnięcia punktu odzyskiwania jako obiekt DateTime, jeśli nic nie jest podane, przyjmuje wartość domyślną równą 30 dni.</span><span class="sxs-lookup"><span data-stu-id="b368a-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="b368a-126">Dotyczy maszyny wirtualnej, SQL (tylko w przypadku typu kopii zapasowej tylko do kopiowania), elementy kopii zapasowej AFS.</span><span class="sxs-lookup"><span data-stu-id="b368a-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="b368a-127">-Item</span><span class="sxs-lookup"><span data-stu-id="b368a-127">-Item</span></span>

<span data-ttu-id="b368a-128">Określa element kopii zapasowej, dla którego to polecenie cmdlet rozpoczyna operację tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b368a-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="b368a-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b368a-129">-VaultId</span></span>

<span data-ttu-id="b368a-130">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="b368a-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b368a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b368a-131">-Confirm</span></span>

<span data-ttu-id="b368a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b368a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b368a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b368a-133">-WhatIf</span></span>

<span data-ttu-id="b368a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b368a-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="b368a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b368a-135">CommonParameters</span></span>
<span data-ttu-id="b368a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b368a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b368a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b368a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b368a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b368a-138">INPUTS</span></span>

### <span data-ttu-id="b368a-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="b368a-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="b368a-140">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b368a-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b368a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b368a-141">System.String</span></span>

## <span data-ttu-id="b368a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b368a-142">OUTPUTS</span></span>

### <span data-ttu-id="b368a-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b368a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b368a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b368a-144">NOTES</span></span>

## <span data-ttu-id="b368a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b368a-145">RELATED LINKS</span></span>

[<span data-ttu-id="b368a-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b368a-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="b368a-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b368a-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b368a-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b368a-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
