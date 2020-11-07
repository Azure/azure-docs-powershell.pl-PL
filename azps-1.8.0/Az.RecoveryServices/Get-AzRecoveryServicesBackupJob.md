---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708672"
---
# <span data-ttu-id="d2d6a-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2d6a-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d2d6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d6a-103">Pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="d2d6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2d6a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2d6a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="d2d6a-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="d2d6a-107">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d2d6a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2d6a-108">EXAMPLES</span></span>

### <span data-ttu-id="d2d6a-109">Przykład 1: uzyskiwanie wszystkich zadań w trakcie wykonywania</span><span class="sxs-lookup"><span data-stu-id="d2d6a-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="d2d6a-110">Pierwsze polecenie pobiera stan zadania w trakcie wykonywania jako tablicę, a następnie zapisuje je w zmiennej $Joblist.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="d2d6a-111">Drugie polecenie wyświetla pierwszy element tablicy $Joblist.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="d2d6a-112">Przykład 2: pobieranie wszystkich zadań zakończonych niepowodzeniem w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="d2d6a-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="d2d6a-113">To polecenie pobiera nieudane zadania z ostatniego tygodnia w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="d2d6a-114">Parametr *from* określa godzinę określoną w ubiegłym ciągu siedem dni (UTC).</span><span class="sxs-lookup"><span data-stu-id="d2d6a-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="d2d6a-115">W poleceniu nie określono *wartości parametru to* .</span><span class="sxs-lookup"><span data-stu-id="d2d6a-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="d2d6a-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="d2d6a-117">Przykład 3: uzyskiwanie zadania w trakcie wykonywania i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="d2d6a-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="d2d6a-118">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="d2d6a-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2d6a-119">PARAMETERS</span></span>

### <span data-ttu-id="d2d6a-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d2d6a-120">-BackupManagementType</span></span>
<span data-ttu-id="d2d6a-121">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="d2d6a-122">Obecnie obsługiwana jest tylko AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d6a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d6a-123">-DefaultProfile</span></span>
<span data-ttu-id="d2d6a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d6a-125">-Od</span><span class="sxs-lookup"><span data-stu-id="d2d6a-125">-From</span></span>
<span data-ttu-id="d2d6a-126">Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d2d6a-127">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="d2d6a-128">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d2d6a-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="d2d6a-129">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="d2d6a-130">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="d2d6a-130">-Job</span></span>
<span data-ttu-id="d2d6a-131">Określa nazwę zadania kopii zapasowej, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="d2d6a-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="d2d6a-132">-JobId</span></span>
<span data-ttu-id="d2d6a-133">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="d2d6a-134">Identyfikator jest właściwością InstanceId obiektu **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="d2d6a-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="d2d6a-135">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupJob** , użyj polecenie Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="d2d6a-136">-Operation</span><span class="sxs-lookup"><span data-stu-id="d2d6a-136">-Operation</span></span>
<span data-ttu-id="d2d6a-137">Określa działanie zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d2d6a-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2d6a-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2d6a-139">Wykonania</span><span class="sxs-lookup"><span data-stu-id="d2d6a-139">Backup</span></span>
- <span data-ttu-id="d2d6a-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="d2d6a-140">ConfigureBackup</span></span>
- <span data-ttu-id="d2d6a-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="d2d6a-141">DeleteBackupData</span></span>
- <span data-ttu-id="d2d6a-142">Zarejestruj</span><span class="sxs-lookup"><span data-stu-id="d2d6a-142">Register</span></span>
- <span data-ttu-id="d2d6a-143">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="d2d6a-143">Restore</span></span>
- <span data-ttu-id="d2d6a-144">Nie Chroń</span><span class="sxs-lookup"><span data-stu-id="d2d6a-144">UnProtect</span></span>
- <span data-ttu-id="d2d6a-145">Wyrejestrowywanie</span><span class="sxs-lookup"><span data-stu-id="d2d6a-145">Unregister</span></span>

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

### <span data-ttu-id="d2d6a-146">-Status</span><span class="sxs-lookup"><span data-stu-id="d2d6a-146">-Status</span></span>
<span data-ttu-id="d2d6a-147">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d2d6a-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2d6a-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2d6a-149">W trakcie</span><span class="sxs-lookup"><span data-stu-id="d2d6a-149">InProgress</span></span>
- <span data-ttu-id="d2d6a-150">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="d2d6a-150">Failed</span></span>
- <span data-ttu-id="d2d6a-151">Anulowania</span><span class="sxs-lookup"><span data-stu-id="d2d6a-151">Cancelled</span></span>
- <span data-ttu-id="d2d6a-152">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="d2d6a-152">Cancelling</span></span>
- <span data-ttu-id="d2d6a-153">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="d2d6a-153">Completed</span></span>
- <span data-ttu-id="d2d6a-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="d2d6a-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="d2d6a-155">-To</span><span class="sxs-lookup"><span data-stu-id="d2d6a-155">-To</span></span>
<span data-ttu-id="d2d6a-156">Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d2d6a-157">Wartością domyślną jest bieżąca godzina systemowa.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-157">The default value is the current system time.</span></span>
<span data-ttu-id="d2d6a-158">W przypadku określenia tego parametru należy również określić parametr *from* .</span><span class="sxs-lookup"><span data-stu-id="d2d6a-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="d2d6a-159">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="d2d6a-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d2d6a-160">-VaultId</span></span>
<span data-ttu-id="d2d6a-161">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d2d6a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d6a-162">CommonParameters</span></span>
<span data-ttu-id="d2d6a-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2d6a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d6a-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d6a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d6a-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2d6a-165">INPUTS</span></span>

### <span data-ttu-id="d2d6a-166">System. String</span><span class="sxs-lookup"><span data-stu-id="d2d6a-166">System.String</span></span>

## <span data-ttu-id="d2d6a-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2d6a-167">OUTPUTS</span></span>

### <span data-ttu-id="d2d6a-168">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d2d6a-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d2d6a-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2d6a-169">NOTES</span></span>

## <span data-ttu-id="d2d6a-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2d6a-170">RELATED LINKS</span></span>

[<span data-ttu-id="d2d6a-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="d2d6a-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="d2d6a-172">Zatrzymaj — AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2d6a-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="d2d6a-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2d6a-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


