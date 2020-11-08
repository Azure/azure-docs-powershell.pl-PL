---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054524"
---
# <span data-ttu-id="f368f-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="f368f-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="f368f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f368f-102">SYNOPSIS</span></span>
<span data-ttu-id="f368f-103">Pobiera zadania StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f368f-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="f368f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f368f-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f368f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f368f-105">DESCRIPTION</span></span>
<span data-ttu-id="f368f-106">Polecenie cmdlet **Get-AzureStorSimpleJob** pobiera zadania usługi Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f368f-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="f368f-107">Określ identyfikator wystąpienia, aby uzyskać określone zadanie.</span><span class="sxs-lookup"><span data-stu-id="f368f-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="f368f-108">Określ inne parametry, aby ograniczyć zadania, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f368f-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="f368f-109">To polecenie cmdlet zwraca maksymalnie 200 zadań.</span><span class="sxs-lookup"><span data-stu-id="f368f-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="f368f-110">Jeśli istnieje więcej niż 200 zadań, Pobierz pozostałe zadania przy użyciu parametrów *pierwszy* i *Pomiń* .</span><span class="sxs-lookup"><span data-stu-id="f368f-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="f368f-111">Jeśli określisz wartość 100 dla pozycji *Pomiń* i 50 dla *pierwszego* , to polecenie cmdlet nie zwróci pierwszych 100 wyników.</span><span class="sxs-lookup"><span data-stu-id="f368f-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="f368f-112">Zwraca następne 50 wyników po 100, które pominie.</span><span class="sxs-lookup"><span data-stu-id="f368f-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="f368f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f368f-113">EXAMPLES</span></span>

### <span data-ttu-id="f368f-114">Przykład 1: uzyskiwanie zadania przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="f368f-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="f368f-115">To polecenie pobiera informacje dotyczące zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="f368f-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="f368f-116">Przykład 2: pobieranie zadań przy użyciu nazwy urządzenia</span><span class="sxs-lookup"><span data-stu-id="f368f-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="f368f-117">To polecenie pobiera informacje dotyczące zadań związanych z urządzeniem o nazwie 8600 – Bravo 001.</span><span class="sxs-lookup"><span data-stu-id="f368f-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="f368f-118">Polecenie pobiera pierwsze dwa zadania dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="f368f-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="f368f-119">Przykład 3: pobieranie ukończonych zadań</span><span class="sxs-lookup"><span data-stu-id="f368f-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="f368f-120">To polecenie pobiera ukończone zadania.</span><span class="sxs-lookup"><span data-stu-id="f368f-120">This command gets completed jobs.</span></span>
<span data-ttu-id="f368f-121">Polecenie pobiera tylko dwa pierwsze zadania po pominięciu pierwszych dziesięciu zadań.</span><span class="sxs-lookup"><span data-stu-id="f368f-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="f368f-122">Przykład 4: pobieranie ręcznych zadań kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f368f-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="f368f-123">To polecenie pobiera zadania ręcznego typu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f368f-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="f368f-124">Przykład 5: pobieranie zadań między określonymi godzinami</span><span class="sxs-lookup"><span data-stu-id="f368f-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="f368f-125">Dwa pierwsze polecenia tworzą obiekty **DateTime** przy użyciu Get-Date polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f368f-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="f368f-126">Nowe godziny w $StartTime i $EndTime zmiennych są zapisywane w tych poleceniach.</span><span class="sxs-lookup"><span data-stu-id="f368f-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="f368f-127">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f368f-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="f368f-128">Polecenie ostatnie pobiera zadania dla urządzenia o nazwie Device07 między godzinami przechowywanymi w $StartTime i $EndTime.</span><span class="sxs-lookup"><span data-stu-id="f368f-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="f368f-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f368f-129">PARAMETERS</span></span>

### <span data-ttu-id="f368f-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f368f-130">-DeviceName</span></span>
<span data-ttu-id="f368f-131">Określa nazwę urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f368f-131">Specifies the name of a StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-132">-First</span><span class="sxs-lookup"><span data-stu-id="f368f-132">-First</span></span>
<span data-ttu-id="f368f-133">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="f368f-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="f368f-134">Wprowadź liczbę obiektów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f368f-134">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-135">-Od</span><span class="sxs-lookup"><span data-stu-id="f368f-135">-From</span></span>
<span data-ttu-id="f368f-136">Określa datę i godzinę rozpoczęcia zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f368f-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f368f-137">-InstanceId</span></span>
<span data-ttu-id="f368f-138">Określa identyfikator zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f368f-138">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="f368f-139">-Profile</span></span>
<span data-ttu-id="f368f-140">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f368f-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f368f-141">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f368f-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="f368f-142">-Skip</span></span>
<span data-ttu-id="f368f-143">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="f368f-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="f368f-144">Wprowadź liczbę obiektów, które mają zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="f368f-144">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-145">-Status</span><span class="sxs-lookup"><span data-stu-id="f368f-145">-Status</span></span>
<span data-ttu-id="f368f-146">Określa stan.</span><span class="sxs-lookup"><span data-stu-id="f368f-146">Specifies the status.</span></span>
<span data-ttu-id="f368f-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f368f-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f368f-148">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="f368f-148">Running</span></span>
- <span data-ttu-id="f368f-149">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="f368f-149">Completed</span></span>
- <span data-ttu-id="f368f-150">Anulowania</span><span class="sxs-lookup"><span data-stu-id="f368f-150">Cancelled</span></span>
- <span data-ttu-id="f368f-151">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="f368f-151">Failed</span></span>
- <span data-ttu-id="f368f-152">Redukcji</span><span class="sxs-lookup"><span data-stu-id="f368f-152">Canceling</span></span>
- <span data-ttu-id="f368f-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="f368f-153">CompletedWithErrors</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-154">-To</span><span class="sxs-lookup"><span data-stu-id="f368f-154">-To</span></span>
<span data-ttu-id="f368f-155">Określa datę i godzinę zakończenia zadań, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f368f-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-156">-Type</span><span class="sxs-lookup"><span data-stu-id="f368f-156">-Type</span></span>
<span data-ttu-id="f368f-157">Określa typ zadania.</span><span class="sxs-lookup"><span data-stu-id="f368f-157">Specifies the job type.</span></span>
<span data-ttu-id="f368f-158">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f368f-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f368f-159">Wykonania</span><span class="sxs-lookup"><span data-stu-id="f368f-159">Backup</span></span>
- <span data-ttu-id="f368f-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="f368f-160">ManualBackup</span></span>
- <span data-ttu-id="f368f-161">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="f368f-161">Restore</span></span>
- <span data-ttu-id="f368f-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="f368f-162">CloneWorkflow</span></span>
- <span data-ttu-id="f368f-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="f368f-163">DeviceRestore</span></span>
- <span data-ttu-id="f368f-164">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="f368f-164">Update</span></span>
- <span data-ttu-id="f368f-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="f368f-165">SupportPackage</span></span>
- <span data-ttu-id="f368f-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="f368f-166">VirtualApplianceProvisioning</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f368f-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f368f-167">CommonParameters</span></span>
<span data-ttu-id="f368f-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f368f-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f368f-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f368f-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f368f-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f368f-170">INPUTS</span></span>

### <span data-ttu-id="f368f-171">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f368f-171">None</span></span>
<span data-ttu-id="f368f-172">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f368f-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="f368f-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f368f-173">OUTPUTS</span></span>

### <span data-ttu-id="f368f-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="f368f-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="f368f-175">To polecenie cmdlet zwraca listę obiektów szczegółów zadania lub, jeśli określisz parametr *InstanceId* , zwróci jeden obiekt szczegółów zadania.</span><span class="sxs-lookup"><span data-stu-id="f368f-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="f368f-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f368f-176">NOTES</span></span>

## <span data-ttu-id="f368f-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f368f-177">RELATED LINKS</span></span>

[<span data-ttu-id="f368f-178">Zatrzymaj — AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="f368f-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


