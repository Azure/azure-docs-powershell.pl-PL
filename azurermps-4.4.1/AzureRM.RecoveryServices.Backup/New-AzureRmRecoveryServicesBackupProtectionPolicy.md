---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: a871aa624aaf8b7f24d06bd0ff04a45e29b95468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543095"
---
# <span data-ttu-id="1f4bb-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4bb-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1f4bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4bb-103">Tworzy zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f4bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f4bb-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f4bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4bb-106">Polecenie cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** tworzy zasady ochrony kopii zapasowych w magazynie.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="1f4bb-107">Zasady ochrony są skojarzone z co najmniej jednym zasadami przechowywania.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="1f4bb-108">Zasady przechowywania definiują czas przechowywania punktu odzyskiwania w usłudze Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="1f4bb-109">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać domyślne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="1f4bb-110">Możesz też użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać domyślne zasady dotyczące harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="1f4bb-111">Obiekty **SchedulePolicy** i **RetentionPolicy** są używane jako dane wejściowe polecenia cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="1f4bb-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="1f4bb-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1f4bb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f4bb-113">EXAMPLES</span></span>

### <span data-ttu-id="1f4bb-114">Przykład 1. Tworzenie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="1f4bb-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="1f4bb-115">Pierwsze polecenie uzyskuje podstawowy **SchedulePolicyObject** , a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="1f4bb-116">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="1f4bb-117">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="1f4bb-118">Czwarte polecenie dodaje bieżącą datę i godzinę w $Dt jako zaplanowany czas wykonania do zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="1f4bb-119">Piąte polecenie uzyskuje podstawowy obiekt **RetentionPolicy** , a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="1f4bb-120">Szóste polecenie ustawia zasady czasu trwania retencji na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="1f4bb-121">Polecenie ostatnie tworzy obiekt **BackupProtectionPolicy** na podstawie zasad harmonogramu i przechowywania utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="1f4bb-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f4bb-122">PARAMETERS</span></span>

### <span data-ttu-id="1f4bb-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1f4bb-123">-BackupManagementType</span></span>
<span data-ttu-id="1f4bb-124">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="1f4bb-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1f4bb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f4bb-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1f4bb-126">AzureVM</span></span> 
- <span data-ttu-id="1f4bb-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="1f4bb-127">AzureSQLDatabase</span></span>

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

### <span data-ttu-id="1f4bb-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f4bb-128">-Name</span></span>
<span data-ttu-id="1f4bb-129">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-129">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="1f4bb-130">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4bb-130">-RetentionPolicy</span></span>
<span data-ttu-id="1f4bb-131">Określa podstawowy obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="1f4bb-131">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="1f4bb-132">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać obiekt **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="1f4bb-132">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="1f4bb-133">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="1f4bb-133">-SchedulePolicy</span></span>
<span data-ttu-id="1f4bb-134">Określa podstawowy obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="1f4bb-134">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="1f4bb-135">Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać obiekt **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="1f4bb-135">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="1f4bb-136">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="1f4bb-136">-WorkloadType</span></span>
<span data-ttu-id="1f4bb-137">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-137">Specifies the workload type.</span></span>
<span data-ttu-id="1f4bb-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1f4bb-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f4bb-139">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1f4bb-139">AzureVM</span></span> 
- <span data-ttu-id="1f4bb-140">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="1f4bb-140">AzureSQLDatabase</span></span>

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

### <span data-ttu-id="1f4bb-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4bb-141">-DefaultProfile</span></span>
<span data-ttu-id="1f4bb-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f4bb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4bb-143">CommonParameters</span></span>
<span data-ttu-id="1f4bb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4bb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4bb-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f4bb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4bb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f4bb-146">INPUTS</span></span>

## <span data-ttu-id="1f4bb-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f4bb-147">OUTPUTS</span></span>

### <span data-ttu-id="1f4bb-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1f4bb-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="1f4bb-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f4bb-149">NOTES</span></span>

## <span data-ttu-id="1f4bb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f4bb-150">RELATED LINKS</span></span>

[<span data-ttu-id="1f4bb-151">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1f4bb-151">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="1f4bb-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4bb-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1f4bb-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1f4bb-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="1f4bb-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="1f4bb-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="1f4bb-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4bb-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1f4bb-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4bb-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


