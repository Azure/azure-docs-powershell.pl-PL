---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054818"
---
# <span data-ttu-id="338e5-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="338e5-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="338e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="338e5-102">SYNOPSIS</span></span>
<span data-ttu-id="338e5-103">Aktualizuje istniejące zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="338e5-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="338e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="338e5-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="338e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="338e5-105">DESCRIPTION</span></span>
<span data-ttu-id="338e5-106">Polecenie cmdlet **Set-AzureStorSimpleDeviceBackupPolicy** aktualizuje istniejące zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="338e5-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="338e5-107">Można zmieniać nazwy zasad, dodawać, aktualizować i usuwać harmonogramy oraz aktualizować woluminy skojarzone z tymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="338e5-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="338e5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="338e5-108">EXAMPLES</span></span>

### <span data-ttu-id="338e5-109">Przykład 1. Zmienianie nazwy zasad tworzenia kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="338e5-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="338e5-110">To polecenie zmienia nazwę zasad tworzenia kopii zapasowych o określonym IDENTYFIKATORze na UpdatedGeneralPolicy07.</span><span class="sxs-lookup"><span data-stu-id="338e5-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="338e5-111">To polecenie określa parametr *WaitForComplete* , więc polecenie wykonuje zadanie, a następnie zwraca obiekt **TaskStatusInfo** dla zadania.</span><span class="sxs-lookup"><span data-stu-id="338e5-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="338e5-112">Przykład 2: aktualizowanie harmonogramu dla zasad tworzenia kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="338e5-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="338e5-113">Pierwsze polecenie tworzy obiekt konfiguracji aktualizacji przy użyciu polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** , a następnie zapisuje go w zmiennej $UpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="338e5-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="338e5-114">Drugie polecenie tworzy nową zmienną tablicową o nazwie $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="338e5-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="338e5-115">Polecenie następne powoduje dodanie aktualizacji przechowywanej w $UpdateConfig do tej tablicy.</span><span class="sxs-lookup"><span data-stu-id="338e5-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="338e5-116">Do tablicy można dodać więcej niż jednej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="338e5-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="338e5-117">Ostatnie polecenie aktualizuje zasady tworzenia kopii zapasowych o określonym IDENTYFIKATORze na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="338e5-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="338e5-118">Zasady mają teraz zaktualizowany harmonogram przechowywany w $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="338e5-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="338e5-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="338e5-119">PARAMETERS</span></span>

### <span data-ttu-id="338e5-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="338e5-120">-BackupPolicyId</span></span>
<span data-ttu-id="338e5-121">Określa identyfikator wystąpienia obiektu **BackupPolicy** do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="338e5-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="338e5-122">-BackupPolicyName</span></span>
<span data-ttu-id="338e5-123">Określa nową nazwę zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="338e5-123">Specifies a new name for the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="338e5-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="338e5-125">Określa tablicę identyfikatorów wystąpień obiektów **BackupSchedule** , które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="338e5-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="338e5-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="338e5-127">Określa tablicę obiektów **BackupScheduleBase** , które należy dodać do zasad.</span><span class="sxs-lookup"><span data-stu-id="338e5-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="338e5-128">Aby uzyskać obiekt **BackupScheduleBase** , użyj polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="338e5-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="338e5-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="338e5-130">Określa tablicę obiektów **BackupScheduleUpdateRequest** do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="338e5-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="338e5-131">Aby uzyskać obiekt **BackupScheduleUpdateRequest** , użyj polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** .</span><span class="sxs-lookup"><span data-stu-id="338e5-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="338e5-132">-DeviceName</span></span>
<span data-ttu-id="338e5-133">Określa nazwę urządzenia StorSimple, dla którego ma zostać zaktualizowana zasada tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="338e5-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="338e5-134">-NewName</span></span>
<span data-ttu-id="338e5-135">Określa nazwę urządzenia.</span><span class="sxs-lookup"><span data-stu-id="338e5-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="338e5-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="338e5-136">-Profile</span></span>
<span data-ttu-id="338e5-137">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="338e5-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="338e5-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="338e5-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="338e5-139">Określa tablicę identyfikatorów woluminów, dla których należy zaktualizować zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="338e5-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="338e5-140">-WaitForComplete</span></span>
<span data-ttu-id="338e5-141">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="338e5-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338e5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338e5-142">CommonParameters</span></span>
<span data-ttu-id="338e5-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338e5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338e5-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338e5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338e5-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="338e5-145">INPUTS</span></span>

### <span data-ttu-id="338e5-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="338e5-146">None</span></span>

## <span data-ttu-id="338e5-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="338e5-147">OUTPUTS</span></span>

### <span data-ttu-id="338e5-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="338e5-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="338e5-149">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="338e5-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="338e5-150">Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="338e5-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="338e5-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="338e5-151">NOTES</span></span>

## <span data-ttu-id="338e5-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="338e5-152">RELATED LINKS</span></span>

[<span data-ttu-id="338e5-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="338e5-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="338e5-154">Nowe — AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="338e5-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="338e5-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="338e5-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="338e5-156">Nowe — AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="338e5-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


