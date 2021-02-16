---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189298"
---
# <span data-ttu-id="69a63-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69a63-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="69a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a63-102">SYNOPSIS</span></span>
<span data-ttu-id="69a63-103">Tworzy zasady ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="69a63-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="69a63-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69a63-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a63-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69a63-105">DESCRIPTION</span></span>
<span data-ttu-id="69a63-106">Polecenie **cmdlet New-AzRecoveryServicesBackupProtectionPolicy** tworzy zasady ochrony kopii zapasowej w magazynie.</span><span class="sxs-lookup"><span data-stu-id="69a63-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="69a63-107">Zasady ochrony są skojarzone z co najmniej jedną zasadą przechowywania.</span><span class="sxs-lookup"><span data-stu-id="69a63-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="69a63-108">Zasady przechowywania określają, jak długo punkt odzyskiwania jest przechowywany za pomocą usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="69a63-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="69a63-109">Możesz użyć polecenia cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject, aby uzyskać domyślne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="69a63-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="69a63-110">Możesz też użyć polecenia cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject, aby uzyskać domyślne zasady harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="69a63-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="69a63-111">Obiekty **SchedulePolicy** i **RetentionPolicy** są używane jako dane wejściowe polecenia cmdlet **New-AzRecoveryServicesBackupProtectionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="69a63-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="69a63-112">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a63-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="69a63-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69a63-113">EXAMPLES</span></span>

### <span data-ttu-id="69a63-114">Przykład 1. Tworzenie zasad ochrony kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="69a63-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="69a63-115">Pierwsze polecenie uzyskuje bazę **SchedulePolicyObject,** a następnie przechowuje je w $SchPol zmienną.</span><span class="sxs-lookup"><span data-stu-id="69a63-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="69a63-116">Drugie polecenie usuwa wszystkie zaplanowane czasy uruchamiania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="69a63-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="69a63-117">Trzecie polecenie używa Get-Date cmdlet w celu uzyskania bieżącej daty i czasu.</span><span class="sxs-lookup"><span data-stu-id="69a63-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="69a63-118">Czwarte polecenie dodaje bieżącą datę i godzinę w programie $Dt jako zaplanowany czas uruchamiania do zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="69a63-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="69a63-119">Piąte polecenie otrzymuje podstawowy obiekt **RetentionPolicy,** a następnie zapisuje go w $RetPol danych.</span><span class="sxs-lookup"><span data-stu-id="69a63-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="69a63-120">Szóste polecenie ustawia zasady przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="69a63-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="69a63-121">Końcowe polecenie tworzy obiekt **BackupProtectionPolicy** na podstawie harmonogramu i zasad przechowywania utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="69a63-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="69a63-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="69a63-122">Example 2</span></span>

<span data-ttu-id="69a63-123">Tworzy zasady ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="69a63-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="69a63-124">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="69a63-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="69a63-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69a63-125">PARAMETERS</span></span>

### <span data-ttu-id="69a63-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="69a63-126">-BackupManagementType</span></span>
<span data-ttu-id="69a63-127">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="69a63-127">The class of resources being protected.</span></span> <span data-ttu-id="69a63-128">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="69a63-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69a63-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="69a63-129">AzureVM</span></span> 
- <span data-ttu-id="69a63-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="69a63-130">AzureStorage</span></span>
- <span data-ttu-id="69a63-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="69a63-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a63-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a63-132">-DefaultProfile</span></span>
<span data-ttu-id="69a63-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69a63-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69a63-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69a63-134">-Name</span></span>
<span data-ttu-id="69a63-135">Określa nazwę zasad.</span><span class="sxs-lookup"><span data-stu-id="69a63-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="69a63-136">- RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="69a63-136">-RetentionPolicy</span></span>
<span data-ttu-id="69a63-137">Określa obiekt **base RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="69a63-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="69a63-138">Za pomocą tego Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet można uzyskać obiekt **RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="69a63-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a63-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="69a63-139">-SchedulePolicy</span></span>
<span data-ttu-id="69a63-140">Określa obiekt **base SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="69a63-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="69a63-141">Możesz użyć Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet w celu uzyskania **obiektu SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="69a63-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a63-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="69a63-142">-VaultId</span></span>
<span data-ttu-id="69a63-143">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="69a63-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="69a63-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="69a63-144">-WorkloadType</span></span>
<span data-ttu-id="69a63-145">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="69a63-145">Workload type of the resource.</span></span> <span data-ttu-id="69a63-146">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="69a63-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69a63-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="69a63-147">AzureVM</span></span> 
- <span data-ttu-id="69a63-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="69a63-148">AzureFiles</span></span>
- <span data-ttu-id="69a63-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="69a63-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a63-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69a63-150">-Confirm</span></span>
<span data-ttu-id="69a63-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69a63-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a63-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a63-152">-WhatIf</span></span>
<span data-ttu-id="69a63-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a63-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="69a63-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a63-154">CommonParameters</span></span>
<span data-ttu-id="69a63-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a63-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a63-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69a63-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a63-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69a63-157">INPUTS</span></span>

### <span data-ttu-id="69a63-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="69a63-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="69a63-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlet.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="69a63-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="69a63-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="69a63-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="69a63-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="69a63-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="69a63-162">System.String</span><span class="sxs-lookup"><span data-stu-id="69a63-162">System.String</span></span>

## <span data-ttu-id="69a63-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69a63-163">OUTPUTS</span></span>

### <span data-ttu-id="69a63-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="69a63-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="69a63-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69a63-165">NOTES</span></span>

## <span data-ttu-id="69a63-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69a63-166">RELATED LINKS</span></span>

[<span data-ttu-id="69a63-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="69a63-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="69a63-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69a63-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="69a63-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="69a63-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="69a63-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="69a63-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="69a63-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69a63-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="69a63-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="69a63-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


