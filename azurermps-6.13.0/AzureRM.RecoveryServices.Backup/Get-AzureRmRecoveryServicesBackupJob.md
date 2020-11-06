---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551139"
---
# <span data-ttu-id="ee724-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ee724-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ee724-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee724-102">SYNOPSIS</span></span>
<span data-ttu-id="ee724-103">Pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ee724-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee724-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee724-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee724-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee724-105">DESCRIPTION</span></span>
<span data-ttu-id="ee724-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="ee724-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="ee724-107">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="ee724-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ee724-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee724-108">EXAMPLES</span></span>

### <span data-ttu-id="ee724-109">Przykład 1: uzyskiwanie wszystkich zadań w trakcie wykonywania</span><span class="sxs-lookup"><span data-stu-id="ee724-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="ee724-110">Pierwsze polecenie pobiera stan zadania w trakcie wykonywania jako tablicę, a następnie zapisuje je w zmiennej $Joblist.</span><span class="sxs-lookup"><span data-stu-id="ee724-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="ee724-111">Drugie polecenie wyświetla pierwszy element tablicy $Joblist.</span><span class="sxs-lookup"><span data-stu-id="ee724-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="ee724-112">Przykład 2: pobieranie wszystkich zadań zakończonych niepowodzeniem w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="ee724-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="ee724-113">To polecenie pobiera nieudane zadania z ostatniego tygodnia w magazynie.</span><span class="sxs-lookup"><span data-stu-id="ee724-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="ee724-114">Parametr *from* określa godzinę określoną w ubiegłym ciągu siedem dni (UTC).</span><span class="sxs-lookup"><span data-stu-id="ee724-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="ee724-115">W poleceniu nie określono *wartości parametru to* .</span><span class="sxs-lookup"><span data-stu-id="ee724-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ee724-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="ee724-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ee724-117">Przykład 3: uzyskiwanie zadania w trakcie wykonywania i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="ee724-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="ee724-118">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="ee724-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="ee724-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee724-119">PARAMETERS</span></span>

### <span data-ttu-id="ee724-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ee724-120">-BackupManagementType</span></span>
<span data-ttu-id="ee724-121">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="ee724-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="ee724-122">Obecnie obsługiwana jest tylko AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="ee724-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee724-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee724-123">-DefaultProfile</span></span>
<span data-ttu-id="ee724-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee724-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee724-125">-Od</span><span class="sxs-lookup"><span data-stu-id="ee724-125">-From</span></span>
<span data-ttu-id="ee724-126">Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee724-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ee724-127">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ee724-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="ee724-128">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ee724-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ee724-129">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="ee724-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="ee724-130">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="ee724-130">-Job</span></span>
<span data-ttu-id="ee724-131">Określa nazwę zadania kopii zapasowej, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="ee724-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="ee724-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="ee724-132">-JobId</span></span>
<span data-ttu-id="ee724-133">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee724-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ee724-134">Identyfikator jest właściwością InstanceId obiektu **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ee724-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="ee724-135">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupJob** , użyj polecenie Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ee724-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="ee724-136">-Operation</span><span class="sxs-lookup"><span data-stu-id="ee724-136">-Operation</span></span>
<span data-ttu-id="ee724-137">Określa działanie zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee724-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ee724-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ee724-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee724-139">Wykonania</span><span class="sxs-lookup"><span data-stu-id="ee724-139">Backup</span></span>
- <span data-ttu-id="ee724-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ee724-140">ConfigureBackup</span></span>
- <span data-ttu-id="ee724-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ee724-141">DeleteBackupData</span></span>
- <span data-ttu-id="ee724-142">Zarejestruj</span><span class="sxs-lookup"><span data-stu-id="ee724-142">Register</span></span>
- <span data-ttu-id="ee724-143">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="ee724-143">Restore</span></span>
- <span data-ttu-id="ee724-144">Nie Chroń</span><span class="sxs-lookup"><span data-stu-id="ee724-144">UnProtect</span></span>
- <span data-ttu-id="ee724-145">Wyrejestrowywanie</span><span class="sxs-lookup"><span data-stu-id="ee724-145">Unregister</span></span>

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

### <span data-ttu-id="ee724-146">-Status</span><span class="sxs-lookup"><span data-stu-id="ee724-146">-Status</span></span>
<span data-ttu-id="ee724-147">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee724-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ee724-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ee724-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee724-149">W trakcie</span><span class="sxs-lookup"><span data-stu-id="ee724-149">InProgress</span></span>
- <span data-ttu-id="ee724-150">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="ee724-150">Failed</span></span>
- <span data-ttu-id="ee724-151">Anulowania</span><span class="sxs-lookup"><span data-stu-id="ee724-151">Cancelled</span></span>
- <span data-ttu-id="ee724-152">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="ee724-152">Cancelling</span></span>
- <span data-ttu-id="ee724-153">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="ee724-153">Completed</span></span>
- <span data-ttu-id="ee724-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="ee724-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="ee724-155">-To</span><span class="sxs-lookup"><span data-stu-id="ee724-155">-To</span></span>
<span data-ttu-id="ee724-156">Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee724-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ee724-157">Wartością domyślną jest bieżąca godzina systemowa.</span><span class="sxs-lookup"><span data-stu-id="ee724-157">The default value is the current system time.</span></span>
<span data-ttu-id="ee724-158">W przypadku określenia tego parametru należy również określić parametr *from* .</span><span class="sxs-lookup"><span data-stu-id="ee724-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="ee724-159">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="ee724-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="ee724-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ee724-160">-VaultId</span></span>
<span data-ttu-id="ee724-161">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="ee724-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ee724-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee724-162">CommonParameters</span></span>
<span data-ttu-id="ee724-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee724-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee724-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee724-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee724-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee724-165">INPUTS</span></span>

### <span data-ttu-id="ee724-166">System. String</span><span class="sxs-lookup"><span data-stu-id="ee724-166">System.String</span></span>
<span data-ttu-id="ee724-167">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee724-167">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="ee724-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee724-168">OUTPUTS</span></span>

### <span data-ttu-id="ee724-169">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ee724-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ee724-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee724-170">NOTES</span></span>

## <span data-ttu-id="ee724-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee724-171">RELATED LINKS</span></span>

[<span data-ttu-id="ee724-172">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="ee724-172">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="ee724-173">Zatrzymaj — AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ee724-173">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="ee724-174">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ee724-174">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


