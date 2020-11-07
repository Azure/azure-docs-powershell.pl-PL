---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872707"
---
# <span data-ttu-id="ae073-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ae073-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ae073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae073-102">SYNOPSIS</span></span>

<span data-ttu-id="ae073-103">Pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ae073-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="ae073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae073-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae073-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae073-105">DESCRIPTION</span></span>

<span data-ttu-id="ae073-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="ae073-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="ae073-107">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="ae073-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="ae073-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae073-108">EXAMPLES</span></span>

### <span data-ttu-id="ae073-109">Przykład 1: uzyskiwanie wszystkich zadań w trakcie wykonywania</span><span class="sxs-lookup"><span data-stu-id="ae073-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="ae073-110">Pierwsze polecenie pobiera stan zadań w trakcie wykonywania jako tablicę, a następnie zapisuje je w zmiennej $Joblist.</span><span class="sxs-lookup"><span data-stu-id="ae073-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="ae073-111">Drugie polecenie wyświetla pierwszy element tablicy $Joblist.</span><span class="sxs-lookup"><span data-stu-id="ae073-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="ae073-112">Przykład 2: pobieranie wszystkich zadań zakończonych niepowodzeniem w ciągu ostatnich 7 dni</span><span class="sxs-lookup"><span data-stu-id="ae073-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="ae073-113">To polecenie pobiera nieudane zadania z ostatniego tygodnia w magazynie.</span><span class="sxs-lookup"><span data-stu-id="ae073-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="ae073-114">Parametr *from* określa godzinę określoną w ubiegłym ciągu siedem dni (UTC).</span><span class="sxs-lookup"><span data-stu-id="ae073-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="ae073-115">W poleceniu nie określono *wartości parametru to* .</span><span class="sxs-lookup"><span data-stu-id="ae073-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ae073-116">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="ae073-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ae073-117">Przykład 3: uzyskiwanie zadania w trakcie wykonywania i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="ae073-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="ae073-118">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="ae073-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="ae073-119">Uwaga: możesz poczekać na zakończenie zadania kopii zapasowej Azure zamiast pętli while za pomocą polecenia cmdlet **wait-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ae073-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="ae073-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae073-120">PARAMETERS</span></span>

### <span data-ttu-id="ae073-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ae073-121">-BackupManagementType</span></span>

<span data-ttu-id="ae073-122">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="ae073-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="ae073-123">Obecnie obsługiwana jest tylko AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="ae073-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="ae073-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae073-124">-DefaultProfile</span></span>

<span data-ttu-id="ae073-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae073-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae073-126">-Od</span><span class="sxs-lookup"><span data-stu-id="ae073-126">-From</span></span>

<span data-ttu-id="ae073-127">Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae073-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ae073-128">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="ae073-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ae073-129">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ae073-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ae073-130">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="ae073-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="ae073-131">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="ae073-131">-Job</span></span>

<span data-ttu-id="ae073-132">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ae073-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="ae073-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="ae073-133">-JobId</span></span>

<span data-ttu-id="ae073-134">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae073-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ae073-135">Identyfikator jest właściwością JobId obiektu **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="ae073-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="ae073-136">-Operation</span><span class="sxs-lookup"><span data-stu-id="ae073-136">-Operation</span></span>

<span data-ttu-id="ae073-137">Określa działanie zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae073-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ae073-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae073-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae073-139">Wykonania</span><span class="sxs-lookup"><span data-stu-id="ae073-139">Backup</span></span>
- <span data-ttu-id="ae073-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ae073-140">ConfigureBackup</span></span>
- <span data-ttu-id="ae073-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ae073-141">DeleteBackupData</span></span>
- <span data-ttu-id="ae073-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="ae073-142">DisableBackup</span></span>
- <span data-ttu-id="ae073-143">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="ae073-143">Restore</span></span>

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

### <span data-ttu-id="ae073-144">-Status</span><span class="sxs-lookup"><span data-stu-id="ae073-144">-Status</span></span>

<span data-ttu-id="ae073-145">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae073-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ae073-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae073-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae073-147">W trakcie</span><span class="sxs-lookup"><span data-stu-id="ae073-147">InProgress</span></span>
- <span data-ttu-id="ae073-148">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="ae073-148">Failed</span></span>
- <span data-ttu-id="ae073-149">Anulowania</span><span class="sxs-lookup"><span data-stu-id="ae073-149">Cancelled</span></span>
- <span data-ttu-id="ae073-150">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="ae073-150">Cancelling</span></span>
- <span data-ttu-id="ae073-151">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="ae073-151">Completed</span></span>
- <span data-ttu-id="ae073-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="ae073-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="ae073-153">-To</span><span class="sxs-lookup"><span data-stu-id="ae073-153">-To</span></span>

<span data-ttu-id="ae073-154">Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae073-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ae073-155">Wartością domyślną jest bieżąca godzina systemowa.</span><span class="sxs-lookup"><span data-stu-id="ae073-155">The default value is the current system time.</span></span>
<span data-ttu-id="ae073-156">W przypadku określenia tego parametru należy również określić parametr **-from** .</span><span class="sxs-lookup"><span data-stu-id="ae073-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="ae073-157">Użyj formatu UTC dla dat.</span><span class="sxs-lookup"><span data-stu-id="ae073-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="ae073-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ae073-158">-VaultId</span></span>

<span data-ttu-id="ae073-159">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="ae073-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ae073-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae073-160">-CommonParameters</span></span>

<span data-ttu-id="ae073-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae073-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae073-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae073-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae073-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae073-163">INPUTS</span></span>

### <span data-ttu-id="ae073-164">System. String</span><span class="sxs-lookup"><span data-stu-id="ae073-164">System.String</span></span>

## <span data-ttu-id="ae073-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae073-165">OUTPUTS</span></span>

### <span data-ttu-id="ae073-166">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ae073-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ae073-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae073-167">NOTES</span></span>

## <span data-ttu-id="ae073-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae073-168">RELATED LINKS</span></span>

[<span data-ttu-id="ae073-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="ae073-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="ae073-170">Zatrzymaj — AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ae073-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="ae073-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ae073-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
