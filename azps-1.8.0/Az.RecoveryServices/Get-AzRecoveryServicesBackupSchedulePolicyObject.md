---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708651"
---
# <span data-ttu-id="7a8dc-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="7a8dc-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="7a8dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8dc-103">Pobiera obiekt zasad dotyczących harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="7a8dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a8dc-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a8dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="7a8dc-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** pobiera **AzureRMRecoveryServicesSchedulePolicyObject** bazowy.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="7a8dc-107">Ten obiekt nie jest utrwalony w systemie.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="7a8dc-108">Jest to obiekt tymczasowy, który można manipulować i używać z poleceniem cmdlet New-AzRecoveryServicesBackupProtectionPolicy, aby utworzyć nowe zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="7a8dc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a8dc-109">EXAMPLES</span></span>

### <span data-ttu-id="7a8dc-110">Przykład 1. Ustaw częstotliwość harmonogramu na co tydzień</span><span class="sxs-lookup"><span data-stu-id="7a8dc-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7a8dc-111">Pierwsze polecenie pobiera obiekt zasady przechowywania, a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="7a8dc-112">Drugie polecenie pobiera obiekt zasad harmonogramu, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="7a8dc-113">Trzecia zmiana częstotliwości dla zasad harmonogramu na co tydzień.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="7a8dc-114">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej ze zaktualizowanym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="7a8dc-115">Przykład 2: Ustawianie czasu wykonywania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="7a8dc-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7a8dc-116">Pierwsze polecenie powoduje wyświetlenie obiektu zasad harmonogramu, a następnie zapisanie go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="7a8dc-117">Drugie polecenie usuwa wszystkie zaplanowane czasy uruchamiania z $SchPol.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="7a8dc-118">W trzecim poleceniu jest pobierana aktualna Data i godzina, a następnie jest ona przechowywana w zmiennej $DT.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="7a8dc-119">Czwarte polecenie zamienia zaplanowane czasy uruchamiania na bieżącą godzinę.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="7a8dc-120">Kopię zapasową można wykonać tylko raz dziennie, aby zresetować czas wykonywania kopii zapasowej, zastępując oryginalny harmonogram.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="7a8dc-121">Ostatnie polecenie tworzy zasady ochrony kopii zapasowych przy użyciu nowego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="7a8dc-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a8dc-122">PARAMETERS</span></span>

### <span data-ttu-id="7a8dc-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7a8dc-123">-BackupManagementType</span></span>
<span data-ttu-id="7a8dc-124">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="7a8dc-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7a8dc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a8dc-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7a8dc-126">AzureVM</span></span> 
- <span data-ttu-id="7a8dc-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7a8dc-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="7a8dc-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7a8dc-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8dc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8dc-129">-DefaultProfile</span></span>
<span data-ttu-id="7a8dc-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a8dc-131">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="7a8dc-131">-WorkloadType</span></span>
<span data-ttu-id="7a8dc-132">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-132">Specifies the workload type.</span></span>
<span data-ttu-id="7a8dc-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7a8dc-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a8dc-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7a8dc-134">AzureVM</span></span> 
- <span data-ttu-id="7a8dc-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7a8dc-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="7a8dc-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="7a8dc-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8dc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8dc-137">CommonParameters</span></span>
<span data-ttu-id="7a8dc-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8dc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8dc-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a8dc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8dc-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a8dc-140">INPUTS</span></span>

### <span data-ttu-id="7a8dc-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7a8dc-141">None</span></span>

## <span data-ttu-id="7a8dc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a8dc-142">OUTPUTS</span></span>

### <span data-ttu-id="7a8dc-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="7a8dc-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="7a8dc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a8dc-144">NOTES</span></span>

## <span data-ttu-id="7a8dc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a8dc-145">RELATED LINKS</span></span>

[<span data-ttu-id="7a8dc-146">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a8dc-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7a8dc-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a8dc-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


