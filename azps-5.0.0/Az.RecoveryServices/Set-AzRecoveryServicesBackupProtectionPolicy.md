---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224668"
---
# <span data-ttu-id="917fb-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="917fb-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="917fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="917fb-102">SYNOPSIS</span></span>
<span data-ttu-id="917fb-103">Modyfikuje zasady ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="917fb-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="917fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="917fb-104">SYNTAX</span></span>

### <span data-ttu-id="917fb-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="917fb-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="917fb-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="917fb-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="917fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="917fb-107">DESCRIPTION</span></span>
<span data-ttu-id="917fb-108">Polecenie cmdlet **Set-AzRecoveryServicesBackupProtectionPolicy** modyfikuje istniejące zasady ochrony kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="917fb-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="917fb-109">Można modyfikować składniki Harmonogram kopii zapasowych i zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="917fb-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="917fb-110">Wszelkie wprowadzone zmiany mają wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z tymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="917fb-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="917fb-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="917fb-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="917fb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="917fb-112">EXAMPLES</span></span>

### <span data-ttu-id="917fb-113">Przykład 1. modyfikacja zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="917fb-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="917fb-114">Pierwsze polecenie uzyskuje podstawowy obiekt SchedulePolicy, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="917fb-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="917fb-115">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="917fb-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="917fb-116">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę, a następnie przechowywać ją w zmiennej $DT.</span><span class="sxs-lookup"><span data-stu-id="917fb-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="917fb-117">Czwarte polecenie umożliwia dodanie daty i godziny w $DT do harmonogramu czasu uruchomienia zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="917fb-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="917fb-118">W piątym poleceniu jest pobierany podstawowy obiekt zasady przechowywania, a następnie jest on przechowywany w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="917fb-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="917fb-119">Szóste polecenie ustawia czas trwania przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="917fb-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="917fb-120">Po siódmym poleceniu otrzymano zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="917fb-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="917fb-121">Ósmy i dziewiąte ustawia parametry grupy zasobów skojarzone z zasadami, które przechowują punkty przywracania.</span><span class="sxs-lookup"><span data-stu-id="917fb-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="917fb-122">Polecenie ostatnie modyfikuje zasady ochrony kopii zapasowej w $Pol przy użyciu zasad harmonogramu w $SchPol i zasad przechowywania w $RetPol.</span><span class="sxs-lookup"><span data-stu-id="917fb-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="917fb-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="917fb-123">PARAMETERS</span></span>

### <span data-ttu-id="917fb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917fb-124">-DefaultProfile</span></span>
<span data-ttu-id="917fb-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="917fb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="917fb-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="917fb-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="917fb-127">Parametr Switch wskazujący, czy ponawianie aktualizacji zasad dla elementów, których nie można wykonać, nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="917fb-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="917fb-128">-Policy</span><span class="sxs-lookup"><span data-stu-id="917fb-128">-Policy</span></span>
<span data-ttu-id="917fb-129">Określa zasady ochrony kopii zapasowej, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="917fb-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="917fb-130">Aby uzyskać obiekt **BackupProtectionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="917fb-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="917fb-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="917fb-131">-RetentionPolicy</span></span>
<span data-ttu-id="917fb-132">Określa podstawowe zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="917fb-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="917fb-133">Aby uzyskać obiekt **RetentionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="917fb-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="917fb-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="917fb-134">-SchedulePolicy</span></span>
<span data-ttu-id="917fb-135">Określa obiekt zasad dotyczących harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="917fb-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="917fb-136">Aby uzyskać obiekt **SchedulePolicy** , użyj obiektu Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="917fb-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="917fb-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="917fb-137">-VaultId</span></span>
<span data-ttu-id="917fb-138">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="917fb-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="917fb-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="917fb-139">-Confirm</span></span>
<span data-ttu-id="917fb-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="917fb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917fb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917fb-141">-WhatIf</span></span>
<span data-ttu-id="917fb-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="917fb-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="917fb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917fb-143">CommonParameters</span></span>
<span data-ttu-id="917fb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917fb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917fb-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="917fb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917fb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="917fb-146">INPUTS</span></span>

### <span data-ttu-id="917fb-147">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="917fb-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="917fb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="917fb-148">System.String</span></span>

## <span data-ttu-id="917fb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="917fb-149">OUTPUTS</span></span>

### <span data-ttu-id="917fb-150">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="917fb-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="917fb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="917fb-151">NOTES</span></span>

## <span data-ttu-id="917fb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="917fb-152">RELATED LINKS</span></span>

[<span data-ttu-id="917fb-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="917fb-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="917fb-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="917fb-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="917fb-155">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="917fb-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="917fb-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="917fb-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


