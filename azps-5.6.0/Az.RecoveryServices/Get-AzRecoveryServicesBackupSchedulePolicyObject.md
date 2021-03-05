---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979434"
---
# <span data-ttu-id="e0f3e-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e0f3e-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="e0f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f3e-103">Pobiera obiekt zasad harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="e0f3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0f3e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0f3e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="e0f3e-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** otrzymuje podstawowe polecenie **cmdlet AzureRMRecoveryServicesSchedulePolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="e0f3e-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="e0f3e-107">Ten obiekt nie jest utrwalony w systemie.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="e0f3e-108">Jest to obiekt tymczasowy, na który można manipulować i używać go razem z New-AzRecoveryServicesBackupProtectionPolicy cmdlet w celu utworzenia nowych zasad ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="e0f3e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0f3e-109">EXAMPLES</span></span>

### <span data-ttu-id="e0f3e-110">Przykład 1. Ustawianie częstotliwości planowania na wartość tygodniową</span><span class="sxs-lookup"><span data-stu-id="e0f3e-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e0f3e-111">Pierwsze polecenie pobiera obiekt zasad przechowywania, a następnie zapisuje go w $RetPol danych.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="e0f3e-112">Drugie polecenie pobiera obiekt zasad harmonogramu, a następnie przechowuje je w $SchPol zmienną.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="e0f3e-113">Trzecie polecenie zmienia częstotliwość stosowania zasad harmonogramu na tygodniowe.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="e0f3e-114">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej ze zaktualizowanym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="e0f3e-115">Przykład 2. Ustawianie czasu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="e0f3e-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e0f3e-116">Pierwsze polecenie pobiera obiekt zasad harmonogramu, a następnie przechowuje je w $SchPol zmienną.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="e0f3e-117">Drugie polecenie usuwa z aplikacji wszystkie zaplanowane czasy $SchPol.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="e0f3e-118">Trzecie polecenie pobiera bieżącą datę i godzinę, a następnie przechowuje je w $DT zmienną.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="e0f3e-119">Czwarte polecenie zastępuje zaplanowane godziny uruchomienia bieżącą godziną.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="e0f3e-120">W usłudze AzureVM można wykonać kopię zapasową tylko raz dziennie, więc aby zresetować czas wykonywania kopii zapasowej, należy zastąpić oryginalny harmonogram.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="e0f3e-121">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej przy użyciu nowego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="e0f3e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0f3e-122">PARAMETERS</span></span>

### <span data-ttu-id="e0f3e-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e0f3e-123">-BackupManagementType</span></span>
<span data-ttu-id="e0f3e-124">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-124">The class of resources being protected.</span></span> <span data-ttu-id="e0f3e-125">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e0f3e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e0f3e-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e0f3e-126">AzureVM</span></span> 
- <span data-ttu-id="e0f3e-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e0f3e-127">AzureStorage</span></span>
- <span data-ttu-id="e0f3e-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="e0f3e-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f3e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f3e-129">-DefaultProfile</span></span>
<span data-ttu-id="e0f3e-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f3e-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e0f3e-131">-WorkloadType</span></span>
<span data-ttu-id="e0f3e-132">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-132">Workload type of the resource.</span></span> <span data-ttu-id="e0f3e-133">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e0f3e-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e0f3e-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e0f3e-134">AzureVM</span></span> 
- <span data-ttu-id="e0f3e-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="e0f3e-135">AzureFiles</span></span>
- <span data-ttu-id="e0f3e-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="e0f3e-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f3e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f3e-137">CommonParameters</span></span>
<span data-ttu-id="e0f3e-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f3e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0f3e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f3e-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0f3e-140">INPUTS</span></span>

### <span data-ttu-id="e0f3e-141">Brak</span><span class="sxs-lookup"><span data-stu-id="e0f3e-141">None</span></span>

## <span data-ttu-id="e0f3e-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0f3e-142">OUTPUTS</span></span>

### <span data-ttu-id="e0f3e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="e0f3e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="e0f3e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0f3e-144">NOTES</span></span>

## <span data-ttu-id="e0f3e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0f3e-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0f3e-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0f3e-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e0f3e-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0f3e-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


