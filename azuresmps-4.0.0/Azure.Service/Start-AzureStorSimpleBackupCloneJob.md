---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054714"
---
# <span data-ttu-id="6ac2f-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="6ac2f-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="6ac2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ac2f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac2f-103">Rozpoczyna zadanie, które powoduje sklonowanie kopii zapasowej na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="6ac2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ac2f-104">SYNTAX</span></span>

### <span data-ttu-id="6ac2f-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6ac2f-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6ac2f-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="6ac2f-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6ac2f-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="6ac2f-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ac2f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ac2f-108">DESCRIPTION</span></span>
<span data-ttu-id="6ac2f-109">Polecenie cmdlet **Start-AzureStorSimpleBackupCloneJob** rozpoczyna zadanie, które umożliwia sklonowanie istniejącej kopii zapasowej na urządzeniu z systemem StorSimple.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="6ac2f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ac2f-110">EXAMPLES</span></span>

### <span data-ttu-id="6ac2f-111">Przykład 1: klonowanie kopii zapasowej do innego woluminu przy użyciu nazw urządzeń</span><span class="sxs-lookup"><span data-stu-id="6ac2f-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="6ac2f-112">Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="6ac2f-113">Polecenie zapisuje kopię zapasową w zmiennej $Backup.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="6ac2f-114">Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="6ac2f-115">Polecenie zapisuje wyniki w zmiennej $Acrs.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="6ac2f-116">Polecenie ostatnie rozpoczyna zadanie, które powiela określoną kopię zapasową woluminu na urządzeniu do innego woluminu na tym samym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="6ac2f-117">W tym przykładzie określono nazwę urządzenia według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-117">This example specifies the device by name.</span></span>
<span data-ttu-id="6ac2f-118">W poleceniu są używane wartości przechowywane w $Backup i $Acrs.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="6ac2f-119">Polecenie zwraca identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="6ac2f-120">Przykład 2: klonowanie kopii zapasowej do innego woluminu przy użyciu identyfikatorów urządzeń</span><span class="sxs-lookup"><span data-stu-id="6ac2f-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="6ac2f-121">Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="6ac2f-122">Polecenie zapisuje kopię zapasową w zmiennej $Backup.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="6ac2f-123">Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="6ac2f-124">Polecenie zapisuje wyniki w zmiennej $Acrs.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="6ac2f-125">Polecenie ostatnie rozpoczyna zadanie, które powiela określoną kopię zapasową woluminu na urządzeniu do innego woluminu na tym samym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="6ac2f-126">W tym przykładzie określono urządzenie według identyfikatora urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="6ac2f-127">W poleceniu są używane wartości przechowywane w $Backup i $Acrs.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="6ac2f-128">Polecenie zwraca identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="6ac2f-129">Przykład 3: klonowanie kopii zapasowej do woluminu na innym urządzeniu przy użyciu nazw urządzeń</span><span class="sxs-lookup"><span data-stu-id="6ac2f-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="6ac2f-130">Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="6ac2f-131">Polecenie zapisuje kopię zapasową w zmiennej $Backup.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="6ac2f-132">Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="6ac2f-133">Polecenie zapisuje wyniki w zmiennej $Acrs.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="6ac2f-134">Polecenie ostatnie rozpoczyna zadanie, które powiela określoną kopię zapasową woluminu na urządzeniu na innym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="6ac2f-135">W tym przykładzie określono urządzenia według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="6ac2f-136">W poleceniu są używane wartości przechowywane w $Backup i $Acrs.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="6ac2f-137">Polecenie zwraca identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="6ac2f-138">Przykład 4: klonowanie kopii zapasowej do innego woluminu przy użyciu nazw urządzeń i operatora potoku</span><span class="sxs-lookup"><span data-stu-id="6ac2f-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="6ac2f-139">Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="6ac2f-140">Polecenie zapisuje kopię zapasową w zmiennej $Backup.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="6ac2f-141">Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="6ac2f-142">Polecenie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ac2f-143">Bieżące polecenie cmdlet rozpoczyna zadanie, które sklonowa określoną kopię zapasową woluminu na urządzeniu do innego woluminu na tym samym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="6ac2f-144">W tym przykładzie określono nazwę urządzenia według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-144">This example specifies the device by name.</span></span>
<span data-ttu-id="6ac2f-145">W poleceniu użyto wartości przechowywanej w $Backup.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="6ac2f-146">Polecenie pobiera wartość parametru *TargetAccessControlRecords* z rurociągu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="6ac2f-147">Polecenie zwraca identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="6ac2f-148">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ac2f-148">PARAMETERS</span></span>

### <span data-ttu-id="6ac2f-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="6ac2f-149">-BackupId</span></span>
<span data-ttu-id="6ac2f-150">Określa identyfikator wystąpienia kopii zapasowej do sklonowania.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="6ac2f-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="6ac2f-151">-CloneVolumeName</span></span>
<span data-ttu-id="6ac2f-152">Określa nazwę nowego sklonowanego woluminu na urządzeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="6ac2f-153">-Force</span><span class="sxs-lookup"><span data-stu-id="6ac2f-153">-Force</span></span>
<span data-ttu-id="6ac2f-154">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ac2f-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ac2f-155">-Profile</span></span>
<span data-ttu-id="6ac2f-156">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6ac2f-157">-Migawka</span><span class="sxs-lookup"><span data-stu-id="6ac2f-157">-Snapshot</span></span>
<span data-ttu-id="6ac2f-158">Określa obiekt migawki, który jest klonem tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac2f-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="6ac2f-159">-SourceDeviceId</span></span>
<span data-ttu-id="6ac2f-160">Określa identyfikator wystąpienia urządzenia źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="6ac2f-161">To polecenie cmdlet powoduje klonowanie z powrotem z urządzenia źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac2f-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="6ac2f-162">-SourceDeviceName</span></span>
<span data-ttu-id="6ac2f-163">Określa nazwę urządzenia źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="6ac2f-164">To polecenie cmdlet powoduje klonowanie z powrotem z urządzenia źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac2f-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="6ac2f-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="6ac2f-166">Określa rekordy kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac2f-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="6ac2f-167">-TargetDeviceId</span></span>
<span data-ttu-id="6ac2f-168">Określa identyfikator wystąpienia urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac2f-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="6ac2f-169">-TargetDeviceName</span></span>
<span data-ttu-id="6ac2f-170">Określa nazwę urządzenia, do którego to polecenie cmdlet klonuje kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac2f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac2f-171">CommonParameters</span></span>
<span data-ttu-id="6ac2f-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac2f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac2f-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac2f-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ac2f-174">INPUTS</span></span>

### <span data-ttu-id="6ac2f-175">Migawka, lista AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6ac2f-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="6ac2f-176">Do tego polecenia cmdlet można potoku obiekty typu **migawka** lub lista obiektów **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="6ac2f-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="6ac2f-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ac2f-177">OUTPUTS</span></span>

## <span data-ttu-id="6ac2f-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ac2f-178">NOTES</span></span>

## <span data-ttu-id="6ac2f-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ac2f-179">RELATED LINKS</span></span>

[<span data-ttu-id="6ac2f-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="6ac2f-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="6ac2f-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6ac2f-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


