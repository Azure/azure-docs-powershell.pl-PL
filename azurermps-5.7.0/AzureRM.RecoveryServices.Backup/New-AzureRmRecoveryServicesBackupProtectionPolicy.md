---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526681"
---
# <span data-ttu-id="2e79c-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e79c-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="2e79c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e79c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e79c-103">Tworzy zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="2e79c-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e79c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e79c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e79c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e79c-105">DESCRIPTION</span></span>
<span data-ttu-id="2e79c-106">Polecenie cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** tworzy zasady ochrony kopii zapasowych w magazynie.</span><span class="sxs-lookup"><span data-stu-id="2e79c-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="2e79c-107">Zasady ochrony są skojarzone z co najmniej jednym zasadami przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2e79c-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="2e79c-108">Zasady przechowywania definiują czas przechowywania punktu odzyskiwania w usłudze Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="2e79c-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="2e79c-109">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać domyślne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2e79c-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="2e79c-110">Możesz też użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać domyślne zasady dotyczące harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="2e79c-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="2e79c-111">Obiekty **SchedulePolicy** i **RetentionPolicy** są używane jako dane wejściowe polecenia cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="2e79c-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="2e79c-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="2e79c-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2e79c-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e79c-113">EXAMPLES</span></span>

### <span data-ttu-id="2e79c-114">Przykład 1. Tworzenie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="2e79c-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="2e79c-115">Pierwsze polecenie uzyskuje podstawowy **SchedulePolicyObject** , a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="2e79c-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="2e79c-116">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="2e79c-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="2e79c-117">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę.</span><span class="sxs-lookup"><span data-stu-id="2e79c-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="2e79c-118">Czwarte polecenie dodaje bieżącą datę i godzinę w $Dt jako zaplanowany czas wykonania do zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="2e79c-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="2e79c-119">Piąte polecenie uzyskuje podstawowy obiekt **RetentionPolicy** , a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="2e79c-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="2e79c-120">Szóste polecenie ustawia zasady czasu trwania retencji na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="2e79c-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="2e79c-121">Polecenie ostatnie tworzy obiekt **BackupProtectionPolicy** na podstawie zasad harmonogramu i przechowywania utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="2e79c-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="2e79c-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e79c-122">PARAMETERS</span></span>

### <span data-ttu-id="2e79c-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2e79c-123">-BackupManagementType</span></span>
<span data-ttu-id="2e79c-124">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="2e79c-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="2e79c-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2e79c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e79c-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2e79c-126">AzureVM</span></span> 
- <span data-ttu-id="2e79c-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="2e79c-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e79c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e79c-128">-DefaultProfile</span></span>
<span data-ttu-id="2e79c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e79c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e79c-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e79c-130">-Name</span></span>
<span data-ttu-id="2e79c-131">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="2e79c-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="2e79c-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e79c-132">-RetentionPolicy</span></span>
<span data-ttu-id="2e79c-133">Określa podstawowy obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="2e79c-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="2e79c-134">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="2e79c-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e79c-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="2e79c-135">-SchedulePolicy</span></span>
<span data-ttu-id="2e79c-136">Określa podstawowy obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="2e79c-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="2e79c-137">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="2e79c-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e79c-138">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="2e79c-138">-WorkloadType</span></span>
<span data-ttu-id="2e79c-139">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="2e79c-139">Specifies the workload type.</span></span>
<span data-ttu-id="2e79c-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2e79c-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e79c-141">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2e79c-141">AzureVM</span></span> 
- <span data-ttu-id="2e79c-142">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="2e79c-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e79c-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e79c-143">-Confirm</span></span>
<span data-ttu-id="2e79c-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e79c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e79c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e79c-145">-WhatIf</span></span>
<span data-ttu-id="2e79c-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e79c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e79c-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e79c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e79c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e79c-148">CommonParameters</span></span>
<span data-ttu-id="2e79c-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e79c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e79c-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e79c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e79c-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e79c-151">INPUTS</span></span>

### <span data-ttu-id="2e79c-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2e79c-152">None</span></span>
<span data-ttu-id="2e79c-153">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2e79c-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e79c-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e79c-154">OUTPUTS</span></span>

### <span data-ttu-id="2e79c-155">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="2e79c-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="2e79c-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e79c-156">NOTES</span></span>

## <span data-ttu-id="2e79c-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e79c-157">RELATED LINKS</span></span>

[<span data-ttu-id="2e79c-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2e79c-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2e79c-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e79c-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2e79c-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="2e79c-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="2e79c-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="2e79c-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="2e79c-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e79c-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2e79c-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2e79c-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


