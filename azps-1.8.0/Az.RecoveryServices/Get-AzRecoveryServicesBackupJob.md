---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399825"
---
# <span data-ttu-id="69206-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="69206-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="69206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69206-102">SYNOPSIS</span></span>
<span data-ttu-id="69206-103">Otrzymuje zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="69206-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="69206-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69206-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69206-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69206-105">DESCRIPTION</span></span>
<span data-ttu-id="69206-106">Polecenie **cmdlet Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej platformy Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="69206-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="69206-107">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="69206-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69206-108">EXAMPLES</span></span>

### <span data-ttu-id="69206-109">Przykład 1. Uzyskiwanie wszystkich zadań w toku</span><span class="sxs-lookup"><span data-stu-id="69206-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="69206-110">Pierwsze polecenie otrzymuje stan zadania w toku jako tablicę, a następnie przechowuje je w $Joblist tablicy.</span><span class="sxs-lookup"><span data-stu-id="69206-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="69206-111">Drugie polecenie wyświetla pierwszy element w $Joblist tablicy.</span><span class="sxs-lookup"><span data-stu-id="69206-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="69206-112">Przykład 2. Uzyskiwanie wszystkich zadań, których nie udało się uzyskać w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="69206-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="69206-113">To polecenie pobiera zadania, których niepowodzenie zakończyło się w zeszłym tygodniu w magazynie.</span><span class="sxs-lookup"><span data-stu-id="69206-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="69206-114">Parametr *Od* określa czas siedmiu dni w przeszłości określonej w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="69206-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="69206-115">To polecenie nie określa wartości dla *parametru To.*</span><span class="sxs-lookup"><span data-stu-id="69206-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="69206-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="69206-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="69206-117">Przykład 3. Uzyskiwanie zadania w toku i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="69206-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="69206-118">Ten skrypt ankietuje pierwsze zadanie, które jest obecnie w toku, do momentu jego ukończenia.</span><span class="sxs-lookup"><span data-stu-id="69206-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="69206-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69206-119">PARAMETERS</span></span>

### <span data-ttu-id="69206-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="69206-120">-BackupManagementType</span></span>
<span data-ttu-id="69206-121">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="69206-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="69206-122">Obecnie jest obsługiwana tylko usługa AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="69206-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="69206-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69206-123">-DefaultProfile</span></span>
<span data-ttu-id="69206-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69206-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69206-125">— Od</span><span class="sxs-lookup"><span data-stu-id="69206-125">-From</span></span>
<span data-ttu-id="69206-126">Określa rozpoczęcie (jako obiekt **DateTime)** zakresu czasu dla zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69206-127">Aby uzyskać obiekt **DateTime,** użyj Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="69206-128">Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.</span><span class="sxs-lookup"><span data-stu-id="69206-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="69206-129">Daty należy stosować w formacie UTC.</span><span class="sxs-lookup"><span data-stu-id="69206-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="69206-130">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="69206-130">-Job</span></span>
<span data-ttu-id="69206-131">Określa nazwę zadania kopii zapasowej do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="69206-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="69206-132">- JobId</span><span class="sxs-lookup"><span data-stu-id="69206-132">-JobId</span></span>
<span data-ttu-id="69206-133">Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="69206-134">Identyfikator jest właściwością InstanceId obiektu **AzureRmRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="69206-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="69206-135">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupJob,** użyj narzędzia Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="69206-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="69206-136">— Operacja</span><span class="sxs-lookup"><span data-stu-id="69206-136">-Operation</span></span>
<span data-ttu-id="69206-137">Określa operację zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69206-138">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="69206-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69206-139">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="69206-139">Backup</span></span>
- <span data-ttu-id="69206-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="69206-140">ConfigureBackup</span></span>
- <span data-ttu-id="69206-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="69206-141">DeleteBackupData</span></span>
- <span data-ttu-id="69206-142">Zarejestruj się</span><span class="sxs-lookup"><span data-stu-id="69206-142">Register</span></span>
- <span data-ttu-id="69206-143">Przywróć</span><span class="sxs-lookup"><span data-stu-id="69206-143">Restore</span></span>
- <span data-ttu-id="69206-144">UnProtect</span><span class="sxs-lookup"><span data-stu-id="69206-144">UnProtect</span></span>
- <span data-ttu-id="69206-145">Wyrejestruj</span><span class="sxs-lookup"><span data-stu-id="69206-145">Unregister</span></span>

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

### <span data-ttu-id="69206-146">— Status</span><span class="sxs-lookup"><span data-stu-id="69206-146">-Status</span></span>
<span data-ttu-id="69206-147">Określa stan zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69206-148">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="69206-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69206-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="69206-149">InProgress</span></span>
- <span data-ttu-id="69206-150">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="69206-150">Failed</span></span>
- <span data-ttu-id="69206-151">Anulowano</span><span class="sxs-lookup"><span data-stu-id="69206-151">Cancelled</span></span>
- <span data-ttu-id="69206-152">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="69206-152">Cancelling</span></span>
- <span data-ttu-id="69206-153">Ukończono</span><span class="sxs-lookup"><span data-stu-id="69206-153">Completed</span></span>
- <span data-ttu-id="69206-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="69206-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="69206-155">— Do</span><span class="sxs-lookup"><span data-stu-id="69206-155">-To</span></span>
<span data-ttu-id="69206-156">Określa koniec (jako obiekt **DateTime)** zakresu czasu dla zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69206-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="69206-157">Wartość domyślna to bieżący czas systemowy.</span><span class="sxs-lookup"><span data-stu-id="69206-157">The default value is the current system time.</span></span>
<span data-ttu-id="69206-158">Jeśli określisz ten parametr, musisz również określić parametr *Od.*</span><span class="sxs-lookup"><span data-stu-id="69206-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="69206-159">Daty należy stosować w formacie UTC.</span><span class="sxs-lookup"><span data-stu-id="69206-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="69206-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="69206-160">-VaultId</span></span>
<span data-ttu-id="69206-161">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="69206-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="69206-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69206-162">CommonParameters</span></span>
<span data-ttu-id="69206-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69206-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69206-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69206-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69206-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69206-165">INPUTS</span></span>

### <span data-ttu-id="69206-166">System.String</span><span class="sxs-lookup"><span data-stu-id="69206-166">System.String</span></span>

## <span data-ttu-id="69206-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69206-167">OUTPUTS</span></span>

### <span data-ttu-id="69206-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="69206-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="69206-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69206-169">NOTES</span></span>

## <span data-ttu-id="69206-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69206-170">RELATED LINKS</span></span>


[<span data-ttu-id="69206-171">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="69206-171">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="69206-172">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="69206-172">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


