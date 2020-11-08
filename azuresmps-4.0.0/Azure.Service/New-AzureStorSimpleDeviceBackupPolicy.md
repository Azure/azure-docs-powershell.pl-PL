---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055174"
---
# <span data-ttu-id="279bd-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="279bd-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="279bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="279bd-102">SYNOPSIS</span></span>
<span data-ttu-id="279bd-103">Tworzy zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="279bd-103">Creates a backup policy.</span></span>

## <span data-ttu-id="279bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="279bd-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="279bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="279bd-105">DESCRIPTION</span></span>
<span data-ttu-id="279bd-106">Polecenie cmdlet **New-AzureStorSimpleDeviceBackupPolicy** tworzy zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="279bd-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="279bd-107">Zasady tworzenia kopii zapasowej zawierają co najmniej jeden harmonogram kopii zapasowych, który może być uruchomiony w jednym lub większej liczbie woluminów.</span><span class="sxs-lookup"><span data-stu-id="279bd-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="279bd-108">Aby utworzyć harmonogram wykonywania kopii zapasowych, użyj polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="279bd-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="279bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="279bd-109">EXAMPLES</span></span>

### <span data-ttu-id="279bd-110">Przykład 1. Tworzenie zasad tworzenia kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="279bd-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="279bd-111">Pierwsze polecenie tworzy obiekt konfiguracji Harmonogram kopii zapasowych przy użyciu polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , a następnie zapisuje ten obiekt w zmiennej $Schedule 01.</span><span class="sxs-lookup"><span data-stu-id="279bd-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="279bd-112">Drugie polecenie tworzy inny obiekt konfiguracji kopii zapasowej przy użyciu polecenia **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , a następnie zapisuje ten obiekt w zmiennej $Schedule 02.</span><span class="sxs-lookup"><span data-stu-id="279bd-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="279bd-113">W trzecim poleceniu jest tworzona pusta zmienna tablicowa o nazwie $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="279bd-114">Następne dwa polecenia dodają obiekty utworzone w pierwszych dwóch poleceniach do $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="279bd-115">Szóste polecenie pobiera kontener woluminowy dla urządzenia o nazwie Contoso63-AppVm przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** , a następnie zapisuje ten obiekt kontenera w zmiennej $DeviceContainer.</span><span class="sxs-lookup"><span data-stu-id="279bd-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="279bd-116">Po siódmym poleceniu jest pobierany wolumin kontenera woluminu przechowywanego w pierwszym członku $DeviceContainer przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolume** , a następnie zapisanie tego woluminu w zmiennej $Volume.</span><span class="sxs-lookup"><span data-stu-id="279bd-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="279bd-117">W przypadku ósmego polecenia zostanie utworzona pusta zmienna tablicowa o nazwie $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="279bd-118">Polecenie Next (następne) dodaje identyfikator woluminu do $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="279bd-119">Ta wartość identyfikuje wolumin przechowywany w $Volume, na którym są uruchamiane zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="279bd-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="279bd-120">Możesz dodać kolejne identyfikatory woluminów do $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="279bd-121">Ostatnie polecenie tworzy zasady tworzenia kopii zapasowych o nazwie GeneralPolicy07 dla urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="279bd-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="279bd-122">To polecenie Określa obiekty konfiguracji harmonogramu przechowywane w $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="279bd-123">Polecenie określa wolumin lub woluminy, do których mają być stosowane zasady, w $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="279bd-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="279bd-124">Zasady tworzenia kopii zapasowych można zweryfikować przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="279bd-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="279bd-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="279bd-125">PARAMETERS</span></span>

### <span data-ttu-id="279bd-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="279bd-126">-BackupPolicyName</span></span>
<span data-ttu-id="279bd-127">Określa nazwę zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="279bd-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="279bd-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="279bd-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="279bd-129">Określa tablicę obiektów **BackupScheduleBase** , które należy dodać do zasad.</span><span class="sxs-lookup"><span data-stu-id="279bd-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="279bd-130">Każdy obiekt przedstawia harmonogram.</span><span class="sxs-lookup"><span data-stu-id="279bd-130">Each object represents a schedule.</span></span>
<span data-ttu-id="279bd-131">Zasady tworzenia kopii zapasowej zawierają jeden lub więcej harmonogramów.</span><span class="sxs-lookup"><span data-stu-id="279bd-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="279bd-132">Aby uzyskać obiekt **BackupScheduleBase** , użyj polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="279bd-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279bd-133">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="279bd-133">-DeviceName</span></span>
<span data-ttu-id="279bd-134">Określa nazwę urządzenia StorSimple, na którym należy utworzyć zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="279bd-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="279bd-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="279bd-135">-Profile</span></span>
<span data-ttu-id="279bd-136">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="279bd-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="279bd-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="279bd-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="279bd-138">Określa tablicę identyfikatorów woluminów dodawanych do zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="279bd-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279bd-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="279bd-139">-WaitForComplete</span></span>
<span data-ttu-id="279bd-140">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="279bd-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="279bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279bd-141">CommonParameters</span></span>
<span data-ttu-id="279bd-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279bd-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="279bd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279bd-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="279bd-144">INPUTS</span></span>

### <span data-ttu-id="279bd-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="279bd-145">None</span></span>

## <span data-ttu-id="279bd-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="279bd-146">OUTPUTS</span></span>

### <span data-ttu-id="279bd-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="279bd-147">BackupPolicy</span></span>
<span data-ttu-id="279bd-148">To polecenie cmdlet zwraca obiekt **BackupPolicy** , który zawiera nowe harmonogramy i woluminy.</span><span class="sxs-lookup"><span data-stu-id="279bd-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="279bd-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="279bd-149">NOTES</span></span>

## <span data-ttu-id="279bd-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="279bd-150">RELATED LINKS</span></span>

[<span data-ttu-id="279bd-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="279bd-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="279bd-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="279bd-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="279bd-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="279bd-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="279bd-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="279bd-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="279bd-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="279bd-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="279bd-156">Nowe — AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="279bd-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


