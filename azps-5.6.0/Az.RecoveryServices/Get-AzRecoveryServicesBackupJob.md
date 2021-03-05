---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 011b27cfff166173d485636a1e8890d917484651
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984241"
---
# <span data-ttu-id="00809-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="00809-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="00809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00809-102">SYNOPSIS</span></span>

<span data-ttu-id="00809-103">Otrzymuje zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="00809-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="00809-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00809-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00809-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="00809-105">DESCRIPTION</span></span>

<span data-ttu-id="00809-106">Polecenie **cmdlet Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej platformy Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="00809-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="00809-107">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="00809-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="00809-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00809-108">EXAMPLES</span></span>

### <span data-ttu-id="00809-109">Przykład 1. Uzyskiwanie wszystkich zadań w toku</span><span class="sxs-lookup"><span data-stu-id="00809-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="00809-110">Pierwsze polecenie otrzymuje stan zadań w toku jako tablicę, a następnie przechowuje je w $Joblist tablicy.</span><span class="sxs-lookup"><span data-stu-id="00809-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="00809-111">Drugie polecenie wyświetla pierwszy element w $Joblist tablicy.</span><span class="sxs-lookup"><span data-stu-id="00809-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="00809-112">Przykład 2. Uzyskiwanie wszystkich zadań, których nie udało się uzyskać w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="00809-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="00809-113">To polecenie pobiera zadania, których niepowodzenie zakończyło się w zeszłym tygodniu w magazynie.</span><span class="sxs-lookup"><span data-stu-id="00809-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="00809-114">Parametr *From* określa czas siedmiu dni w przeszłości określonej w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="00809-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="00809-115">To polecenie nie określa wartości dla *parametru To.*</span><span class="sxs-lookup"><span data-stu-id="00809-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="00809-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="00809-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="00809-117">Przykład 3. Uzyskiwanie zadania w toku i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="00809-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="00809-118">Ten skrypt ankietuje pierwsze zadanie, które jest obecnie w toku, do momentu jego ukończenia.</span><span class="sxs-lookup"><span data-stu-id="00809-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="00809-119">Uwaga: Możesz użyć polecenia cmdlet **Wait-AzRecoveryServicesBackupJob,** aby zaczekać na ukończenie zadania kopii zapasowej platformy Azure, zamiast podczas pętli.</span><span class="sxs-lookup"><span data-stu-id="00809-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="00809-120">Przykład 4. Uzyskiwanie wszystkich zadań AzureVM w ciągu ostatnich 2 dni, które zakończyły się pomyślnie</span><span class="sxs-lookup"><span data-stu-id="00809-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="00809-121">Pierwsze polecenie cmdlet pobiera obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="00809-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="00809-122">Drugie polecenie cmdlet przechowuje wszystkie zadania AzureVM w danym magazynie, które zostały ukończone w ciągu ostatnich 2 dni w celu $jobs.</span><span class="sxs-lookup"><span data-stu-id="00809-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="00809-123">Zmień wartość parametru BackupManagementType na mab w celu zdalnego dostępu do zadań agenta MAB.</span><span class="sxs-lookup"><span data-stu-id="00809-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="00809-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00809-124">PARAMETERS</span></span>

### <span data-ttu-id="00809-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="00809-125">-BackupManagementType</span></span>

<span data-ttu-id="00809-126">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="00809-126">The class of resources being protected.</span></span> <span data-ttu-id="00809-127">Obecnie wartości obsługiwane dla tego polecenia cmdlet to: AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="00809-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00809-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00809-128">-DefaultProfile</span></span>

<span data-ttu-id="00809-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00809-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00809-130">— Od</span><span class="sxs-lookup"><span data-stu-id="00809-130">-From</span></span>

<span data-ttu-id="00809-131">Określa rozpoczęcie (jako obiekt **DateTime)** zakresu czasu dla zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00809-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="00809-132">Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="00809-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="00809-133">Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.</span><span class="sxs-lookup"><span data-stu-id="00809-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="00809-134">Daty należy stosować w formacie UTC.</span><span class="sxs-lookup"><span data-stu-id="00809-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="00809-135">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="00809-135">-Job</span></span>

<span data-ttu-id="00809-136">Określa zadanie do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="00809-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="00809-137">- JobId</span><span class="sxs-lookup"><span data-stu-id="00809-137">-JobId</span></span>

<span data-ttu-id="00809-138">Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00809-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="00809-139">Identyfikator jest właściwością JobId obiektu **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="00809-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="00809-140">— Operacja</span><span class="sxs-lookup"><span data-stu-id="00809-140">-Operation</span></span>

<span data-ttu-id="00809-141">Określa operację zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00809-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="00809-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="00809-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00809-143">Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="00809-143">Backup</span></span>
- <span data-ttu-id="00809-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="00809-144">ConfigureBackup</span></span>
- <span data-ttu-id="00809-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="00809-145">DeleteBackupData</span></span>
- <span data-ttu-id="00809-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="00809-146">DisableBackup</span></span>
- <span data-ttu-id="00809-147">Przywróć</span><span class="sxs-lookup"><span data-stu-id="00809-147">Restore</span></span>
- <span data-ttu-id="00809-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="00809-148">BackupDataMove</span></span>

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

### <span data-ttu-id="00809-149">— Status</span><span class="sxs-lookup"><span data-stu-id="00809-149">-Status</span></span>

<span data-ttu-id="00809-150">Określa stan zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00809-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="00809-151">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="00809-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00809-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="00809-152">InProgress</span></span>
- <span data-ttu-id="00809-153">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="00809-153">Failed</span></span>
- <span data-ttu-id="00809-154">Anulowano</span><span class="sxs-lookup"><span data-stu-id="00809-154">Cancelled</span></span>
- <span data-ttu-id="00809-155">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="00809-155">Cancelling</span></span>
- <span data-ttu-id="00809-156">Ukończono</span><span class="sxs-lookup"><span data-stu-id="00809-156">Completed</span></span>
- <span data-ttu-id="00809-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="00809-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="00809-158">— Do</span><span class="sxs-lookup"><span data-stu-id="00809-158">-To</span></span>

<span data-ttu-id="00809-159">Określa koniec (jako obiekt **DateTime)** zakresu czasu dla zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00809-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="00809-160">Wartość domyślna to bieżący czas systemowy.</span><span class="sxs-lookup"><span data-stu-id="00809-160">The default value is the current system time.</span></span>
<span data-ttu-id="00809-161">Jeśli określisz ten parametr, musisz także określić parametr **-From.**</span><span class="sxs-lookup"><span data-stu-id="00809-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="00809-162">Daty należy stosować w formacie UTC.</span><span class="sxs-lookup"><span data-stu-id="00809-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="00809-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="00809-163">-VaultId</span></span>

<span data-ttu-id="00809-164">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="00809-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="00809-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00809-165">CommonParameters</span></span>
<span data-ttu-id="00809-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00809-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00809-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00809-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00809-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00809-168">INPUTS</span></span>

### <span data-ttu-id="00809-169">System.String</span><span class="sxs-lookup"><span data-stu-id="00809-169">System.String</span></span>

## <span data-ttu-id="00809-170">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00809-170">OUTPUTS</span></span>

### <span data-ttu-id="00809-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="00809-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="00809-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00809-172">NOTES</span></span>

## <span data-ttu-id="00809-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00809-173">RELATED LINKS</span></span>

[<span data-ttu-id="00809-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="00809-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="00809-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="00809-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="00809-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="00809-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
