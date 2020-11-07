---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886618"
---
# <span data-ttu-id="cf46c-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cf46c-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="cf46c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf46c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf46c-103">Modyfikuje zasady ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cf46c-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="cf46c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf46c-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf46c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf46c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf46c-106">Polecenie cmdlet **Set-AzBackupProtectionPolicy** modyfikuje istniejące zasady ochrony kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf46c-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="cf46c-107">Można modyfikować składniki Harmonogram kopii zapasowych i zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cf46c-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="cf46c-108">Wszelkie wprowadzone zmiany mają wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z tymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="cf46c-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="cf46c-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="cf46c-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="cf46c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf46c-110">EXAMPLES</span></span>

### <span data-ttu-id="cf46c-111">Przykład 1. modyfikacja zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="cf46c-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="cf46c-112">Pierwsze polecenie uzyskuje podstawowy obiekt SchedulePolicy, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="cf46c-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="cf46c-113">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="cf46c-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="cf46c-114">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę, a następnie przechowywać ją w zmiennej $DT.</span><span class="sxs-lookup"><span data-stu-id="cf46c-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="cf46c-115">Czwarte polecenie umożliwia dodanie daty i godziny w $DT do harmonogramu czasu uruchomienia zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="cf46c-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="cf46c-116">W piątym poleceniu jest pobierany podstawowy obiekt zasady przechowywania, a następnie jest on przechowywany w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="cf46c-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="cf46c-117">Szóste polecenie ustawia czas trwania przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="cf46c-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="cf46c-118">Po siódmym poleceniu otrzymano zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="cf46c-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="cf46c-119">Polecenie ostatnie modyfikuje zasady ochrony kopii zapasowej w $Pol przy użyciu zasad harmonogramu w $SchPol i zasad przechowywania w $RetPol.</span><span class="sxs-lookup"><span data-stu-id="cf46c-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="cf46c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf46c-120">PARAMETERS</span></span>

### <span data-ttu-id="cf46c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf46c-121">-DefaultProfile</span></span>
<span data-ttu-id="cf46c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf46c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf46c-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="cf46c-123">-Policy</span></span>
<span data-ttu-id="cf46c-124">Określa zasady ochrony kopii zapasowej, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf46c-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="cf46c-125">Aby uzyskać obiekt **BackupProtectionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cf46c-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cf46c-126">-RetentionPolicy</span></span>
<span data-ttu-id="cf46c-127">Określa podstawowe zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cf46c-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="cf46c-128">Aby uzyskać obiekt **RetentionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="cf46c-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="cf46c-129">-SchedulePolicy</span></span>
<span data-ttu-id="cf46c-130">Określa obiekt zasad dotyczących harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="cf46c-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="cf46c-131">Aby uzyskać obiekt **SchedulePolicy** , użyj obiektu Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="cf46c-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf46c-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cf46c-132">-VaultId</span></span>
<span data-ttu-id="cf46c-133">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="cf46c-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cf46c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf46c-134">-Confirm</span></span>
<span data-ttu-id="cf46c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf46c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf46c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf46c-136">-WhatIf</span></span>
<span data-ttu-id="cf46c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf46c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf46c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf46c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf46c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf46c-139">CommonParameters</span></span>
<span data-ttu-id="cf46c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf46c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf46c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf46c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf46c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf46c-142">INPUTS</span></span>

### <span data-ttu-id="cf46c-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="cf46c-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="cf46c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cf46c-144">System.String</span></span>

## <span data-ttu-id="cf46c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf46c-145">OUTPUTS</span></span>

### <span data-ttu-id="cf46c-146">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="cf46c-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cf46c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf46c-147">NOTES</span></span>

## <span data-ttu-id="cf46c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf46c-148">RELATED LINKS</span></span>

[<span data-ttu-id="cf46c-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cf46c-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="cf46c-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="cf46c-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="cf46c-151">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cf46c-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="cf46c-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cf46c-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


