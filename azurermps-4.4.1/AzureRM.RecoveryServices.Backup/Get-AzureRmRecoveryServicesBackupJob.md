---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553793"
---
# <span data-ttu-id="19c34-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="19c34-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="19c34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19c34-102">SYNOPSIS</span></span>
<span data-ttu-id="19c34-103">Pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="19c34-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19c34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19c34-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19c34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19c34-105">DESCRIPTION</span></span>
<span data-ttu-id="19c34-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="19c34-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="19c34-107">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="19c34-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="19c34-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19c34-108">EXAMPLES</span></span>

### <span data-ttu-id="19c34-109">Przykład 1: uzyskiwanie wszystkich zadań w trakcie wykonywania</span><span class="sxs-lookup"><span data-stu-id="19c34-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="19c34-110">Pierwsze polecenie pobiera stan zadania w trakcie wykonywania jako tablicę, a następnie zapisuje je w zmiennej $Joblist.</span><span class="sxs-lookup"><span data-stu-id="19c34-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="19c34-111">Drugie polecenie wyświetla pierwszy element tablicy $Joblist.</span><span class="sxs-lookup"><span data-stu-id="19c34-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="19c34-112">Przykład 2: pobieranie wszystkich zadań zakończonych niepowodzeniem w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="19c34-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="19c34-113">To polecenie pobiera nieudane zadania z ostatniego tygodnia w magazynie.</span><span class="sxs-lookup"><span data-stu-id="19c34-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="19c34-114">Parametr *from* określa godzinę określoną w ubiegłym ciągu siedem dni (UTC).</span><span class="sxs-lookup"><span data-stu-id="19c34-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="19c34-115">W poleceniu nie określono *wartości parametru to* .</span><span class="sxs-lookup"><span data-stu-id="19c34-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="19c34-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="19c34-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="19c34-117">Przykład 3: uzyskiwanie zadania w trakcie wykonywania i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="19c34-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="19c34-118">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="19c34-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="19c34-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19c34-119">PARAMETERS</span></span>

### <span data-ttu-id="19c34-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="19c34-120">-BackupManagementType</span></span>
<span data-ttu-id="19c34-121">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="19c34-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="19c34-122">Obecnie obsługiwana jest tylko AzureVM.</span><span class="sxs-lookup"><span data-stu-id="19c34-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-123">-Od</span><span class="sxs-lookup"><span data-stu-id="19c34-123">-From</span></span>
<span data-ttu-id="19c34-124">Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c34-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="19c34-125">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="19c34-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="19c34-126">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="19c34-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="19c34-127">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="19c34-127">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-128">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="19c34-128">-Job</span></span>
<span data-ttu-id="19c34-129">Określa nazwę zadania kopii zapasowej, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="19c34-129">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="19c34-130">-JobId</span></span>
<span data-ttu-id="19c34-131">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c34-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="19c34-132">Identyfikator jest właściwością InstanceId obiektu **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="19c34-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="19c34-133">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupJob** , użyj polecenie Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="19c34-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-134">-Operation</span><span class="sxs-lookup"><span data-stu-id="19c34-134">-Operation</span></span>
<span data-ttu-id="19c34-135">Określa działanie zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c34-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="19c34-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="19c34-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19c34-137">Wykonania</span><span class="sxs-lookup"><span data-stu-id="19c34-137">Backup</span></span>
- <span data-ttu-id="19c34-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="19c34-138">ConfigureBackup</span></span>
- <span data-ttu-id="19c34-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="19c34-139">DeleteBackupData</span></span>
- <span data-ttu-id="19c34-140">Zarejestruj</span><span class="sxs-lookup"><span data-stu-id="19c34-140">Register</span></span>
- <span data-ttu-id="19c34-141">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="19c34-141">Restore</span></span>
- <span data-ttu-id="19c34-142">Nie Chroń</span><span class="sxs-lookup"><span data-stu-id="19c34-142">UnProtect</span></span>
- <span data-ttu-id="19c34-143">Wyrejestrowywanie</span><span class="sxs-lookup"><span data-stu-id="19c34-143">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-144">-Status</span><span class="sxs-lookup"><span data-stu-id="19c34-144">-Status</span></span>
<span data-ttu-id="19c34-145">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c34-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="19c34-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="19c34-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19c34-147">W trakcie</span><span class="sxs-lookup"><span data-stu-id="19c34-147">InProgress</span></span>
- <span data-ttu-id="19c34-148">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="19c34-148">Failed</span></span>
- <span data-ttu-id="19c34-149">Anulowania</span><span class="sxs-lookup"><span data-stu-id="19c34-149">Cancelled</span></span>
- <span data-ttu-id="19c34-150">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="19c34-150">Cancelling</span></span>
- <span data-ttu-id="19c34-151">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="19c34-151">Completed</span></span>
- <span data-ttu-id="19c34-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="19c34-152">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-153">-To</span><span class="sxs-lookup"><span data-stu-id="19c34-153">-To</span></span>
<span data-ttu-id="19c34-154">Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c34-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="19c34-155">Wartością domyślną jest bieżąca godzina systemowa.</span><span class="sxs-lookup"><span data-stu-id="19c34-155">The default value is the current system time.</span></span>
<span data-ttu-id="19c34-156">W przypadku określenia tego parametru należy również określić parametr *from* .</span><span class="sxs-lookup"><span data-stu-id="19c34-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="19c34-157">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="19c34-157">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c34-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c34-158">-DefaultProfile</span></span>
<span data-ttu-id="19c34-159">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19c34-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c34-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c34-160">CommonParameters</span></span>
<span data-ttu-id="19c34-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c34-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c34-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c34-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c34-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19c34-163">INPUTS</span></span>

## <span data-ttu-id="19c34-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19c34-164">OUTPUTS</span></span>

### <span data-ttu-id="19c34-165">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="19c34-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="19c34-166">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. JobBase]</span><span class="sxs-lookup"><span data-stu-id="19c34-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="19c34-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19c34-167">NOTES</span></span>

## <span data-ttu-id="19c34-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19c34-168">RELATED LINKS</span></span>

[<span data-ttu-id="19c34-169">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="19c34-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="19c34-170">Zatrzymaj — AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="19c34-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="19c34-171">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="19c34-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


