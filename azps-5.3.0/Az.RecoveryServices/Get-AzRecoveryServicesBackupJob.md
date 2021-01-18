---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501373"
---
# <span data-ttu-id="5b6a8-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5b6a8-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="5b6a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b6a8-102">SYNOPSIS</span></span>

<span data-ttu-id="5b6a8-103">Pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="5b6a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b6a8-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b6a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b6a8-105">DESCRIPTION</span></span>

<span data-ttu-id="5b6a8-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="5b6a8-107">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="5b6a8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b6a8-108">EXAMPLES</span></span>

### <span data-ttu-id="5b6a8-109">Przykład 1: uzyskiwanie wszystkich zadań w trakcie wykonywania</span><span class="sxs-lookup"><span data-stu-id="5b6a8-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="5b6a8-110">Pierwsze polecenie pobiera stan zadań w trakcie wykonywania jako tablicę, a następnie zapisuje je w zmiennej $Joblist.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="5b6a8-111">Drugie polecenie wyświetla pierwszy element tablicy $Joblist.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="5b6a8-112">Przykład 2: pobieranie wszystkich zadań zakończonych niepowodzeniem w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="5b6a8-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="5b6a8-113">To polecenie pobiera nieudane zadania z ostatniego tygodnia w magazynie.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="5b6a8-114">Parametr *from* określa godzinę określoną w ubiegłym ciągu siedem dni (UTC).</span><span class="sxs-lookup"><span data-stu-id="5b6a8-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="5b6a8-115">W poleceniu nie określono *wartości parametru to* .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="5b6a8-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="5b6a8-117">Przykład 3: uzyskiwanie zadania w trakcie wykonywania i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="5b6a8-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="5b6a8-118">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="5b6a8-119">Uwaga: możesz poczekać na zakończenie zadania kopii zapasowej Azure zamiast pętli while za pomocą polecenia cmdlet **wait-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="5b6a8-120">Przykład 4: pobieranie wszystkich zadań AzureVM w ciągu ostatnich 2 dni, które zakończyły się powodzeniem</span><span class="sxs-lookup"><span data-stu-id="5b6a8-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="5b6a8-121">Pierwsze polecenie cmdlet pobiera obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="5b6a8-122">Drugie polecenie cmdlet przechowuje wszystkie zadania AzureVM w danym magazynie, które zostały ukończone w ciągu ostatnich 2 dni w celu $jobs.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="5b6a8-123">Zmień wartość parametru BackupManagementType na MAB w celu pobrania zadań agenta MAB.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="5b6a8-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b6a8-124">PARAMETERS</span></span>

### <span data-ttu-id="5b6a8-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5b6a8-125">-BackupManagementType</span></span>

<span data-ttu-id="5b6a8-126">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-126">The class of resources being protected.</span></span> <span data-ttu-id="5b6a8-127">Obecnie obsługiwane są wartości dla tego polecenia cmdlet to AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="5b6a8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6a8-128">-DefaultProfile</span></span>

<span data-ttu-id="5b6a8-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b6a8-130">-Od</span><span class="sxs-lookup"><span data-stu-id="5b6a8-130">-From</span></span>

<span data-ttu-id="5b6a8-131">Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5b6a8-132">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5b6a8-133">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="5b6a8-134">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="5b6a8-135">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="5b6a8-135">-Job</span></span>

<span data-ttu-id="5b6a8-136">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="5b6a8-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="5b6a8-137">-JobId</span></span>

<span data-ttu-id="5b6a8-138">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="5b6a8-139">Identyfikator jest właściwością JobId obiektu **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="5b6a8-140">-Operation</span><span class="sxs-lookup"><span data-stu-id="5b6a8-140">-Operation</span></span>

<span data-ttu-id="5b6a8-141">Określa działanie zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5b6a8-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b6a8-143">Wykonania</span><span class="sxs-lookup"><span data-stu-id="5b6a8-143">Backup</span></span>
- <span data-ttu-id="5b6a8-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="5b6a8-144">ConfigureBackup</span></span>
- <span data-ttu-id="5b6a8-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="5b6a8-145">DeleteBackupData</span></span>
- <span data-ttu-id="5b6a8-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="5b6a8-146">DisableBackup</span></span>
- <span data-ttu-id="5b6a8-147">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="5b6a8-147">Restore</span></span>
- <span data-ttu-id="5b6a8-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="5b6a8-148">BackupDataMove</span></span>

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

### <span data-ttu-id="5b6a8-149">-Status</span><span class="sxs-lookup"><span data-stu-id="5b6a8-149">-Status</span></span>

<span data-ttu-id="5b6a8-150">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5b6a8-151">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b6a8-152">W trakcie</span><span class="sxs-lookup"><span data-stu-id="5b6a8-152">InProgress</span></span>
- <span data-ttu-id="5b6a8-153">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="5b6a8-153">Failed</span></span>
- <span data-ttu-id="5b6a8-154">Anulowania</span><span class="sxs-lookup"><span data-stu-id="5b6a8-154">Cancelled</span></span>
- <span data-ttu-id="5b6a8-155">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="5b6a8-155">Cancelling</span></span>
- <span data-ttu-id="5b6a8-156">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="5b6a8-156">Completed</span></span>
- <span data-ttu-id="5b6a8-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="5b6a8-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="5b6a8-158">-To</span><span class="sxs-lookup"><span data-stu-id="5b6a8-158">-To</span></span>

<span data-ttu-id="5b6a8-159">Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5b6a8-160">Wartością domyślną jest bieżąca godzina systemowa.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-160">The default value is the current system time.</span></span>
<span data-ttu-id="5b6a8-161">W przypadku określenia tego parametru należy również określić parametr **-from** .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="5b6a8-162">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="5b6a8-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5b6a8-163">-VaultId</span></span>

<span data-ttu-id="5b6a8-164">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5b6a8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6a8-165">CommonParameters</span></span>
<span data-ttu-id="5b6a8-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6a8-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b6a8-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6a8-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-168">INPUTS</span></span>

### <span data-ttu-id="5b6a8-169">System. String</span><span class="sxs-lookup"><span data-stu-id="5b6a8-169">System.String</span></span>

## <span data-ttu-id="5b6a8-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b6a8-170">OUTPUTS</span></span>

### <span data-ttu-id="5b6a8-171">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5b6a8-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5b6a8-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b6a8-172">NOTES</span></span>

## <span data-ttu-id="5b6a8-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-173">RELATED LINKS</span></span>

[<span data-ttu-id="5b6a8-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="5b6a8-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="5b6a8-175">Zatrzymaj — AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5b6a8-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="5b6a8-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5b6a8-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
