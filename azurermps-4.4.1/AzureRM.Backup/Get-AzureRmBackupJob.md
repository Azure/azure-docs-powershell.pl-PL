---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527714"
---
# <span data-ttu-id="9d73d-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9d73d-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="9d73d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d73d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d73d-103">Pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9d73d-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d73d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d73d-104">SYNTAX</span></span>

### <span data-ttu-id="9d73d-105">FiltersSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d73d-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d73d-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="9d73d-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d73d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d73d-107">DESCRIPTION</span></span>
<span data-ttu-id="9d73d-108">Polecenie cmdlet **Get-AzureRmBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="9d73d-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="9d73d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d73d-109">EXAMPLES</span></span>

### <span data-ttu-id="9d73d-110">Przykład 1: pobieranie wszystkich zadań w magazynie kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="9d73d-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="9d73d-111">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="9d73d-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="9d73d-112">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d73d-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9d73d-113">Drugie polecenie pobiera wszystkie zadania dla magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d73d-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="9d73d-114">Przykład 2: pobieranie ukończonych zadań</span><span class="sxs-lookup"><span data-stu-id="9d73d-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="9d73d-115">To polecenie pobiera ukończone zadania z magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d73d-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="9d73d-116">Przykład 3: pobieranie zadań zakończonych niepowodzeniem z ostatniego tygodnia</span><span class="sxs-lookup"><span data-stu-id="9d73d-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="9d73d-117">To polecenie pobiera nieudane zadania z ostatniego tygodnia z magazynu w $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d73d-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="9d73d-118">Parametr *from* określa godzinę w ciągu siedmiu dni.</span><span class="sxs-lookup"><span data-stu-id="9d73d-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="9d73d-119">W poleceniu nie określono *wartości parametru to* .</span><span class="sxs-lookup"><span data-stu-id="9d73d-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="9d73d-120">W związku z tym używana jest wartość domyślna bieżącego czasu.</span><span class="sxs-lookup"><span data-stu-id="9d73d-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="9d73d-121">Przykład 4: Tworzenie kopii zapasowej ankiety dla zadania w toku, które kończy się</span><span class="sxs-lookup"><span data-stu-id="9d73d-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="9d73d-122">Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="9d73d-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="9d73d-123">W pierwszym wierszu skryptu są pobierane wszystkie zadania w $Vault trwające, a następnie te zadania są przechowywane w zmiennej tablicowej $Jobs.</span><span class="sxs-lookup"><span data-stu-id="9d73d-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="9d73d-124">W drugim wierszu jest przechowywane pierwsze zadanie z tablicy $Jobs w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="9d73d-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="9d73d-125">Trzeci wiersz rozpoczyna pętlę **while** , która sprawdza bieżący stan zadania do momentu ukończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="9d73d-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="9d73d-126">Aby uzyskać informacje na temat słowa kluczowego **while** , wpisz `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="9d73d-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="9d73d-127">Pętla **while** zapisuje wiadomość na konsoli, uśpienie przez dziesięć sekund, a następnie aktualizuje zmienną $Job.</span><span class="sxs-lookup"><span data-stu-id="9d73d-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="9d73d-128">Skrypt aktualizuje zmienną $Job, korzystając z istniejącej wartości $Job i bieżącego polecenia cmdlet w celu uzyskania bieżącego stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="9d73d-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="9d73d-129">Aby uzyskać informacje na temat poleceń cmdlet programu Windows PowerShell, wpisz `Get-Help Write-Host` i `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="9d73d-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="9d73d-130">W ostatnim wierszu skryptu zostanie wyświetlony komunikat z informacją o zakończeniu skryptu.</span><span class="sxs-lookup"><span data-stu-id="9d73d-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="9d73d-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d73d-131">PARAMETERS</span></span>

### <span data-ttu-id="9d73d-132">-Od</span><span class="sxs-lookup"><span data-stu-id="9d73d-132">-From</span></span>
<span data-ttu-id="9d73d-133">Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d73d-133">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d73d-134">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9d73d-134">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9d73d-135">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9d73d-135">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-136">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="9d73d-136">-Job</span></span>
<span data-ttu-id="9d73d-137">Określa zadanie, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d73d-137">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="9d73d-138">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9d73d-138">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d73d-139">-JobId</span></span>
<span data-ttu-id="9d73d-140">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d73d-140">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="9d73d-141">Identyfikator jest właściwością **InstanceId** obiektu **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="9d73d-141">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="9d73d-142">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenie Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9d73d-142">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-143">-Operation</span><span class="sxs-lookup"><span data-stu-id="9d73d-143">-Operation</span></span>
<span data-ttu-id="9d73d-144">Określa działanie zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d73d-144">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d73d-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9d73d-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d73d-146">Wykonania</span><span class="sxs-lookup"><span data-stu-id="9d73d-146">Backup</span></span> 
- <span data-ttu-id="9d73d-147">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="9d73d-147">ConfigureBackup</span></span> 
- <span data-ttu-id="9d73d-148">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="9d73d-148">DeleteBackupData</span></span> 
- <span data-ttu-id="9d73d-149">Zarejestruj</span><span class="sxs-lookup"><span data-stu-id="9d73d-149">Register</span></span> 
- <span data-ttu-id="9d73d-150">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="9d73d-150">Restore</span></span> 
- <span data-ttu-id="9d73d-151">Nie Chroń</span><span class="sxs-lookup"><span data-stu-id="9d73d-151">UnProtect</span></span> 
- <span data-ttu-id="9d73d-152">Wyrejestrowywanie</span><span class="sxs-lookup"><span data-stu-id="9d73d-152">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-153">-Status</span><span class="sxs-lookup"><span data-stu-id="9d73d-153">-Status</span></span>
<span data-ttu-id="9d73d-154">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d73d-154">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d73d-155">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9d73d-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d73d-156">W trakcie</span><span class="sxs-lookup"><span data-stu-id="9d73d-156">InProgress</span></span>
- <span data-ttu-id="9d73d-157">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="9d73d-157">Failed</span></span>
- <span data-ttu-id="9d73d-158">Anulowania</span><span class="sxs-lookup"><span data-stu-id="9d73d-158">Cancelled</span></span>
- <span data-ttu-id="9d73d-159">Anulowanie</span><span class="sxs-lookup"><span data-stu-id="9d73d-159">Cancelling</span></span>
- <span data-ttu-id="9d73d-160">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="9d73d-160">Completed</span></span>
- <span data-ttu-id="9d73d-161">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="9d73d-161">CompletedWithWarnings</span></span> 

<span data-ttu-id="9d73d-162">Możesz określić ten parametr, aby znaleźć wszystkie zadania w toku lub wszystkie zadania zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9d73d-162">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-163">-To</span><span class="sxs-lookup"><span data-stu-id="9d73d-163">-To</span></span>
<span data-ttu-id="9d73d-164">Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d73d-164">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9d73d-165">Wartością domyślną jest bieżąca godzina systemowa.</span><span class="sxs-lookup"><span data-stu-id="9d73d-165">The default value is the current system time.</span></span>
<span data-ttu-id="9d73d-166">W przypadku określenia tego parametru należy również określić parametr *from* .</span><span class="sxs-lookup"><span data-stu-id="9d73d-166">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-167">-Type</span><span class="sxs-lookup"><span data-stu-id="9d73d-167">-Type</span></span>
<span data-ttu-id="9d73d-168">Określa typ kontenera, dla którego to polecenie cmdlet pobiera zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9d73d-168">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="9d73d-169">Obecnie jedyną obsługiwaną wartością jest AzureVM.</span><span class="sxs-lookup"><span data-stu-id="9d73d-169">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-170">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="9d73d-170">-Vault</span></span>
<span data-ttu-id="9d73d-171">Określa magazyn kopii zapasowych, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="9d73d-171">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="9d73d-172">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="9d73d-172">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d73d-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d73d-173">-DefaultProfile</span></span>
<span data-ttu-id="9d73d-174">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d73d-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d73d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d73d-175">CommonParameters</span></span>
<span data-ttu-id="9d73d-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d73d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d73d-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d73d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d73d-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d73d-178">INPUTS</span></span>

### <span data-ttu-id="9d73d-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d73d-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="9d73d-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d73d-180">OUTPUTS</span></span>

### <span data-ttu-id="9d73d-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="9d73d-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="9d73d-182">To polecenie cmdlet zwraca co najmniej jedno zadanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9d73d-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="9d73d-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d73d-183">NOTES</span></span>
* <span data-ttu-id="9d73d-184">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d73d-184">None</span></span>

## <span data-ttu-id="9d73d-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d73d-185">RELATED LINKS</span></span>

[<span data-ttu-id="9d73d-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d73d-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="9d73d-187">Zatrzymaj — AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9d73d-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="9d73d-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9d73d-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


