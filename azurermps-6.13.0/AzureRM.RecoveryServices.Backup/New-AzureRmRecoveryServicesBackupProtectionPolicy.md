---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1a9eb2ef731e7ce555fbac1a08cd8468de83ebc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551132"
---
# <span data-ttu-id="4c888-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c888-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="4c888-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c888-102">SYNOPSIS</span></span>
<span data-ttu-id="4c888-103">Tworzy zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="4c888-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c888-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c888-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c888-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c888-105">DESCRIPTION</span></span>
<span data-ttu-id="4c888-106">Polecenie cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** tworzy zasady ochrony kopii zapasowych w magazynie.</span><span class="sxs-lookup"><span data-stu-id="4c888-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="4c888-107">Zasady ochrony są skojarzone z co najmniej jednym zasadami przechowywania.</span><span class="sxs-lookup"><span data-stu-id="4c888-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="4c888-108">Zasady przechowywania definiują czas przechowywania punktu odzyskiwania w usłudze Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="4c888-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="4c888-109">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać domyślne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="4c888-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="4c888-110">Możesz też użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać domyślne zasady dotyczące harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4c888-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="4c888-111">Obiekty **SchedulePolicy** i **RetentionPolicy** są używane jako dane wejściowe polecenia cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="4c888-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="4c888-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="4c888-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4c888-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c888-113">EXAMPLES</span></span>

### <span data-ttu-id="4c888-114">Przykład 1. Tworzenie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="4c888-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="4c888-115">Pierwsze polecenie uzyskuje podstawowy **SchedulePolicyObject** , a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="4c888-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="4c888-116">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="4c888-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="4c888-117">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę.</span><span class="sxs-lookup"><span data-stu-id="4c888-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="4c888-118">Czwarte polecenie dodaje bieżącą datę i godzinę w $Dt jako zaplanowany czas wykonania do zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4c888-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="4c888-119">Piąte polecenie uzyskuje podstawowy obiekt **RetentionPolicy** , a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="4c888-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="4c888-120">Szóste polecenie ustawia zasady czasu trwania retencji na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="4c888-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="4c888-121">Polecenie ostatnie tworzy obiekt **BackupProtectionPolicy** na podstawie zasad harmonogramu i przechowywania utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="4c888-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="4c888-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c888-122">PARAMETERS</span></span>

### <span data-ttu-id="4c888-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4c888-123">-BackupManagementType</span></span>
<span data-ttu-id="4c888-124">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="4c888-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="4c888-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4c888-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c888-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c888-126">AzureVM</span></span> 
- <span data-ttu-id="4c888-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="4c888-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c888-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c888-128">-DefaultProfile</span></span>
<span data-ttu-id="4c888-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c888-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c888-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c888-130">-Name</span></span>
<span data-ttu-id="4c888-131">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="4c888-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="4c888-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c888-132">-RetentionPolicy</span></span>
<span data-ttu-id="4c888-133">Określa podstawowy obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="4c888-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="4c888-134">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="4c888-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="4c888-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="4c888-135">-SchedulePolicy</span></span>
<span data-ttu-id="4c888-136">Określa podstawowy obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="4c888-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="4c888-137">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="4c888-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="4c888-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4c888-138">-VaultId</span></span>
<span data-ttu-id="4c888-139">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4c888-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4c888-140">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="4c888-140">-WorkloadType</span></span>
<span data-ttu-id="4c888-141">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="4c888-141">Specifies the workload type.</span></span>
<span data-ttu-id="4c888-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4c888-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c888-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c888-143">AzureVM</span></span> 
- <span data-ttu-id="4c888-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="4c888-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c888-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c888-145">-Confirm</span></span>
<span data-ttu-id="4c888-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c888-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c888-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c888-147">-WhatIf</span></span>
<span data-ttu-id="4c888-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c888-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c888-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c888-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c888-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c888-150">CommonParameters</span></span>
<span data-ttu-id="4c888-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c888-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c888-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c888-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c888-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c888-153">INPUTS</span></span>

### <span data-ttu-id="4c888-154">Microsoft. Azure. Commands. RecoveryServices. Backup. polecenia. models. Obciążeniatype</span><span class="sxs-lookup"><span data-stu-id="4c888-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="4c888-155">System. Nullable "1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. BackupManagementType, Microsoft. Azure. Commands. RecoveryServices. Backup. MODELES, Version = 4.3.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4c888-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.Commands.RecoveryServices.Backup.Models, Version=4.3.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4c888-156">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="4c888-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="4c888-157">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="4c888-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="4c888-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4c888-158">System.String</span></span>
<span data-ttu-id="4c888-159">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c888-159">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="4c888-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c888-160">OUTPUTS</span></span>

### <span data-ttu-id="4c888-161">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4c888-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="4c888-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c888-162">NOTES</span></span>

## <span data-ttu-id="4c888-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c888-163">RELATED LINKS</span></span>

[<span data-ttu-id="4c888-164">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4c888-164">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="4c888-165">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c888-165">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4c888-166">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4c888-166">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="4c888-167">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="4c888-167">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="4c888-168">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c888-168">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4c888-169">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c888-169">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


