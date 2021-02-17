---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191298"
---
# <span data-ttu-id="b2e3c-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2e3c-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b2e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e3c-103">Modyfikuje zasady ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="b2e3c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2e3c-104">SYNTAX</span></span>

### <span data-ttu-id="b2e3c-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="b2e3c-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e3c-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="b2e3c-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e3c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2e3c-107">DESCRIPTION</span></span>
<span data-ttu-id="b2e3c-108">Polecenie **cmdlet Set-AzRecoveryServicesBackupProtectionPolicy** modyfikuje istniejące zasady ochrony usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="b2e3c-109">Można modyfikować składniki harmonogramu i zasad przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="b2e3c-110">Wszelkie wprowadzone zmiany wpływają na tworzenie kopii zapasowej i przechowywanie elementów skojarzonych z zasadami.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="b2e3c-111">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b2e3c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2e3c-112">EXAMPLES</span></span>

### <span data-ttu-id="b2e3c-113">Przykład 1. Modyfikowanie zasad ochrony kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b2e3c-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="b2e3c-114">Oto szczegółowy opis czynności, które należy wykonać w celu zmodyfikowania zasad ochrony:</span><span class="sxs-lookup"><span data-stu-id="b2e3c-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="b2e3c-115">Uzyskaj podstawową grafikę SchedulePolicyObject i podstawową wartość RetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="b2e3c-116">Przechowuj je w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="b2e3c-117">Ustaw różne parametry obiektu zasad harmonogramu i przechowywania zgodnie z wymaganiami.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="b2e3c-118">Na przykład w powyższym przykładowym skrypcie próbujemy ustawić tygodniowe zasady ochrony.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="b2e3c-119">Dlatego zmieniono częstotliwość harmonogramu na "Tygodniowy", a także zaktualizowano czas uruchamiania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="b2e3c-120">W obiekcie zasad przechowywania zaktualizowaliśmy tygodniowy czas trwania przechowywania i ustawiliśmy poprawną flagę "Włączony harmonogram tygodniowy".</span><span class="sxs-lookup"><span data-stu-id="b2e3c-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="b2e3c-121">Jeśli chcesz ustawić zasady dzienne, ustaw flagę "Harmonogram dzienny włączony" na prawda i przypisz odpowiednie wartości dla innych parametrów obiektu.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="b2e3c-122">Uzyskaj zasady ochrony kopii zapasowej, które chcesz zmodyfikować, i przechowuj je w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="b2e3c-123">W powyższym przykładzie pobrano zasady kopii zapasowej o nazwie "TestPolicy", którą chcemy zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="b2e3c-124">Modyfikowanie zasad ochrony kopii zapasowej pobranych w kroku 3 przy użyciu obiektu zmodyfikowanych zasad harmonogramu i obiektu zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="b2e3c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e3c-125">PARAMETERS</span></span>

### <span data-ttu-id="b2e3c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e3c-126">-DefaultProfile</span></span>
<span data-ttu-id="b2e3c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e3c-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="b2e3c-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="b2e3c-129">Przełącz parametr wskazujący, czy chcesz ponowić aktualizację zasad dla elementów, których niepowodzenie zakończyło się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e3c-130">— Zasady</span><span class="sxs-lookup"><span data-stu-id="b2e3c-130">-Policy</span></span>
<span data-ttu-id="b2e3c-131">Określa zasady ochrony kopii zapasowej, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="b2e3c-132">Aby uzyskać obiekt **BackupProtectionPolicy,** użyj Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="b2e3c-133">- RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2e3c-133">-RetentionPolicy</span></span>
<span data-ttu-id="b2e3c-134">Określa podstawowe zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="b2e3c-135">Aby uzyskać obiekt **RetentionPolicy,** użyj Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e3c-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="b2e3c-136">-SchedulePolicy</span></span>
<span data-ttu-id="b2e3c-137">Określa obiekt zasad harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="b2e3c-138">Aby uzyskać obiekt **SchedulePolicy,** użyj Get-AzRecoveryServicesBackupSchedulePolicyObject obiekt.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e3c-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b2e3c-139">-VaultId</span></span>
<span data-ttu-id="b2e3c-140">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b2e3c-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2e3c-141">-Confirm</span></span>
<span data-ttu-id="b2e3c-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e3c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e3c-143">-WhatIf</span></span>
<span data-ttu-id="b2e3c-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="b2e3c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e3c-145">CommonParameters</span></span>
<span data-ttu-id="b2e3c-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e3c-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2e3c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e3c-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2e3c-148">INPUTS</span></span>

### <span data-ttu-id="b2e3c-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b2e3c-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="b2e3c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b2e3c-150">System.String</span></span>

## <span data-ttu-id="b2e3c-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2e3c-151">OUTPUTS</span></span>

### <span data-ttu-id="b2e3c-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="b2e3c-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b2e3c-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2e3c-153">NOTES</span></span>

## <span data-ttu-id="b2e3c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2e3c-154">RELATED LINKS</span></span>

[<span data-ttu-id="b2e3c-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2e3c-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b2e3c-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b2e3c-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="b2e3c-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2e3c-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b2e3c-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2e3c-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


