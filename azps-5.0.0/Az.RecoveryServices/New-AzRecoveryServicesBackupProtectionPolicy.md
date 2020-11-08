---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233952"
---
# <span data-ttu-id="3a48c-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a48c-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="3a48c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a48c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a48c-103">Tworzy zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="3a48c-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="3a48c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a48c-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a48c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a48c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a48c-106">Polecenie cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** tworzy zasady ochrony kopii zapasowych w magazynie.</span><span class="sxs-lookup"><span data-stu-id="3a48c-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="3a48c-107">Zasady ochrony są skojarzone z co najmniej jednym zasadami przechowywania.</span><span class="sxs-lookup"><span data-stu-id="3a48c-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="3a48c-108">Zasady przechowywania definiują czas przechowywania punktu odzyskiwania w usłudze Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="3a48c-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="3a48c-109">Możesz użyć polecenia cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject, aby uzyskać domyślne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="3a48c-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="3a48c-110">Możesz też użyć polecenia cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject, aby uzyskać domyślne zasady dotyczące harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="3a48c-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="3a48c-111">Obiekty **SchedulePolicy** i **RetentionPolicy** są używane jako dane wejściowe polecenia cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="3a48c-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="3a48c-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="3a48c-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3a48c-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a48c-113">EXAMPLES</span></span>

### <span data-ttu-id="3a48c-114">Przykład 1. Tworzenie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="3a48c-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="3a48c-115">Pierwsze polecenie uzyskuje podstawowy **SchedulePolicyObject** , a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="3a48c-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="3a48c-116">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="3a48c-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="3a48c-117">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę.</span><span class="sxs-lookup"><span data-stu-id="3a48c-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="3a48c-118">Czwarte polecenie dodaje bieżącą datę i godzinę w $Dt jako zaplanowany czas wykonania do zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="3a48c-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="3a48c-119">Piąte polecenie uzyskuje podstawowy obiekt **RetentionPolicy** , a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="3a48c-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="3a48c-120">Szóste polecenie ustawia zasady czasu trwania retencji na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="3a48c-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="3a48c-121">Polecenie ostatnie tworzy obiekt **BackupProtectionPolicy** na podstawie zasad harmonogramu i przechowywania utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="3a48c-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="3a48c-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3a48c-122">Example 2</span></span>

<span data-ttu-id="3a48c-123">Tworzy zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="3a48c-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="3a48c-124">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="3a48c-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="3a48c-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a48c-125">PARAMETERS</span></span>

### <span data-ttu-id="3a48c-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3a48c-126">-BackupManagementType</span></span>
<span data-ttu-id="3a48c-127">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="3a48c-127">The class of resources being protected.</span></span> <span data-ttu-id="3a48c-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a48c-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a48c-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3a48c-129">AzureVM</span></span> 
- <span data-ttu-id="3a48c-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="3a48c-130">AzureStorage</span></span>
- <span data-ttu-id="3a48c-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="3a48c-131">AzureWorkload</span></span>

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

### <span data-ttu-id="3a48c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a48c-132">-DefaultProfile</span></span>
<span data-ttu-id="3a48c-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a48c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a48c-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a48c-134">-Name</span></span>
<span data-ttu-id="3a48c-135">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="3a48c-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="3a48c-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a48c-136">-RetentionPolicy</span></span>
<span data-ttu-id="3a48c-137">Określa podstawowy obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="3a48c-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="3a48c-138">Możesz użyć polecenia cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject, aby uzyskać obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="3a48c-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="3a48c-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="3a48c-139">-SchedulePolicy</span></span>
<span data-ttu-id="3a48c-140">Określa podstawowy obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="3a48c-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="3a48c-141">Możesz użyć polecenia cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject, aby uzyskać obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="3a48c-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="3a48c-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3a48c-142">-VaultId</span></span>
<span data-ttu-id="3a48c-143">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="3a48c-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3a48c-144">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="3a48c-144">-WorkloadType</span></span>
<span data-ttu-id="3a48c-145">Typ obciążenia pracą zasobu.</span><span class="sxs-lookup"><span data-stu-id="3a48c-145">Workload type of the resource.</span></span> <span data-ttu-id="3a48c-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a48c-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a48c-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3a48c-147">AzureVM</span></span> 
- <span data-ttu-id="3a48c-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="3a48c-148">AzureFiles</span></span>
- <span data-ttu-id="3a48c-149">Usługa</span><span class="sxs-lookup"><span data-stu-id="3a48c-149">MSSQL</span></span>

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

### <span data-ttu-id="3a48c-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a48c-150">-Confirm</span></span>
<span data-ttu-id="3a48c-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a48c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a48c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a48c-152">-WhatIf</span></span>
<span data-ttu-id="3a48c-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a48c-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="3a48c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a48c-154">CommonParameters</span></span>
<span data-ttu-id="3a48c-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a48c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a48c-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a48c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a48c-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a48c-157">INPUTS</span></span>

### <span data-ttu-id="3a48c-158">Microsoft. Azure. Commands. RecoveryServices. Backup. polecenia. models. Obciążeniatype</span><span class="sxs-lookup"><span data-stu-id="3a48c-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="3a48c-159">System. Nullable "1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. BackupManagementType, Microsoft. Azure. PowerShell. cmdlet. RecoveryServices. Backup. MODELES, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3a48c-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3a48c-160">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="3a48c-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="3a48c-161">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="3a48c-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="3a48c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3a48c-162">System.String</span></span>

## <span data-ttu-id="3a48c-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a48c-163">OUTPUTS</span></span>

### <span data-ttu-id="3a48c-164">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="3a48c-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="3a48c-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a48c-165">NOTES</span></span>

## <span data-ttu-id="3a48c-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a48c-166">RELATED LINKS</span></span>

[<span data-ttu-id="3a48c-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3a48c-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3a48c-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a48c-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3a48c-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3a48c-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="3a48c-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="3a48c-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="3a48c-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a48c-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="3a48c-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a48c-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


