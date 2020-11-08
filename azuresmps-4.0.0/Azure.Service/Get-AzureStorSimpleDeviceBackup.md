---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055256"
---
# <span data-ttu-id="d3bee-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="d3bee-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="d3bee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3bee-102">SYNOPSIS</span></span>
<span data-ttu-id="d3bee-103">Pobiera kopie zapasowe z urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d3bee-103">Gets backups from a device.</span></span>

## <span data-ttu-id="d3bee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3bee-104">SYNTAX</span></span>

### <span data-ttu-id="d3bee-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d3bee-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3bee-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="d3bee-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3bee-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="d3bee-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3bee-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="d3bee-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3bee-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="d3bee-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3bee-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d3bee-110">DESCRIPTION</span></span>
<span data-ttu-id="d3bee-111">Polecenie cmdlet **Get-AzureStorSimpleDeviceBackup** pobiera kopie zapasowe z urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d3bee-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="d3bee-112">Możesz określić zasady tworzenia kopii zapasowych, głośność i czas utworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d3bee-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="d3bee-113">To polecenie cmdlet może zwrócić maksymalnie 100 kopii zapasowych na pierwszej stronie.</span><span class="sxs-lookup"><span data-stu-id="d3bee-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="d3bee-114">Jeśli istnieje więcej niż 100 kopii zapasowych, Pobierz kolejne strony przy użyciu parametrów *pierwszy* i *Pomiń* .</span><span class="sxs-lookup"><span data-stu-id="d3bee-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="d3bee-115">Jeśli określisz wartość 100 dla pozycji *Pomiń* i 50 dla *pierwszego* , to polecenie cmdlet nie zwróci pierwszych 100 wyników.</span><span class="sxs-lookup"><span data-stu-id="d3bee-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="d3bee-116">Zwraca następne 50 wyników po 100, które pominie.</span><span class="sxs-lookup"><span data-stu-id="d3bee-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="d3bee-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3bee-117">EXAMPLES</span></span>

### <span data-ttu-id="d3bee-118">Przykład 1: pobieranie wszystkich kopii zapasowych na urządzeniu</span><span class="sxs-lookup"><span data-stu-id="d3bee-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="d3bee-119">To polecenie pobiera wszystkie kopie zapasowe istniejące na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="d3bee-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="d3bee-120">Jeśli na pierwszej stronie jest dozwolonych maksymalnie 100 kopii zapasowych, użyj parametrów *First* i *Skip* , aby wyświetlić dodatkowe wyniki.</span><span class="sxs-lookup"><span data-stu-id="d3bee-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="d3bee-121">Przykład 2: pobieranie kopii zapasowych utworzonych między dwiema datami</span><span class="sxs-lookup"><span data-stu-id="d3bee-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="d3bee-122">To polecenie pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm, które zostały utworzone w dniu lub po 10/7/2014 lub przed 10/8/2014.</span><span class="sxs-lookup"><span data-stu-id="d3bee-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="d3bee-123">To polecenie cmdlet pomija pierwszy wynik i zwraca pierwsze dwa wyniki po pierwszym wyniku.</span><span class="sxs-lookup"><span data-stu-id="d3bee-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="d3bee-124">Zmodyfikuj wartości *najpierw* i *Pomiń* , aby wyświetlić inne wyniki.</span><span class="sxs-lookup"><span data-stu-id="d3bee-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="d3bee-125">Przykład 3: pobieranie kopii zapasowych dla identyfikatora zasad kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="d3bee-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="d3bee-126">To polecenie pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm utworzonego w dniu lub przed określoną datą.</span><span class="sxs-lookup"><span data-stu-id="d3bee-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="d3bee-127">Polecenie pobiera kopie zapasowe utworzone przy użyciu zasad tworzenia kopii zapasowych o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="d3bee-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="d3bee-128">To polecenie określa *pierwszy* parametr, więc zwraca tylko 10 pierwszych wyników.</span><span class="sxs-lookup"><span data-stu-id="d3bee-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="d3bee-129">Przykład 4: pobieranie kopii zapasowych obiektu zasad kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="d3bee-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="d3bee-130">To polecenie pobiera obiekt **BackupPolicyDetails** za pomocą polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** , a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d3bee-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3bee-131">To polecenie cmdlet pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm utworzonego za pomocą zasad tworzenia kopii zapasowych z pierwszej części polecenia.</span><span class="sxs-lookup"><span data-stu-id="d3bee-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="d3bee-132">Polecenie pobiera kopie zapasowe utworzone w dniu lub przed określoną datą, tak jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="d3bee-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="d3bee-133">To polecenie zwraca tylko 10 pierwszych wyników.</span><span class="sxs-lookup"><span data-stu-id="d3bee-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="d3bee-134">Przykład 5: uzyskiwanie kopii zapasowej identyfikatora woluminu</span><span class="sxs-lookup"><span data-stu-id="d3bee-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="d3bee-135">To polecenie pobiera kopię zapasową na urządzeniu utworzonym na woluminie o określonym IDENTYFIKATORze wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d3bee-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="d3bee-136">To polecenie określa *pierwszy* parametr, więc zwraca tylko pierwszy wynik.</span><span class="sxs-lookup"><span data-stu-id="d3bee-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="d3bee-137">Przykład 6: pobieranie kopii zapasowej dla nazwy woluminu</span><span class="sxs-lookup"><span data-stu-id="d3bee-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="d3bee-138">To polecenie pobiera obiekt **VirtualDisk** za pomocą polecenia cmdlet **Get-AzureStorSimpleDeviceVolume** , a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d3bee-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3bee-139">To polecenie cmdlet pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm utworzonego na woluminie z pierwszej części polecenia.</span><span class="sxs-lookup"><span data-stu-id="d3bee-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="d3bee-140">To polecenie zwraca tylko pierwszy wynik.</span><span class="sxs-lookup"><span data-stu-id="d3bee-140">This command returns only the first result.</span></span>

## <span data-ttu-id="d3bee-141">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3bee-141">PARAMETERS</span></span>

### <span data-ttu-id="d3bee-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d3bee-142">-BackupPolicy</span></span>
<span data-ttu-id="d3bee-143">Określa obiekt **BackupPolicyDetails** .</span><span class="sxs-lookup"><span data-stu-id="d3bee-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="d3bee-144">To polecenie cmdlet wykorzystuje **Identyfikator InstanceId** tego obiektu do określenia, które kopie zapasowe mają zostać wyświetlone.</span><span class="sxs-lookup"><span data-stu-id="d3bee-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="d3bee-145">Aby uzyskać obiekt **BackupPolicyDetails** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="d3bee-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3bee-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="d3bee-146">-BackupPolicyId</span></span>
<span data-ttu-id="d3bee-147">Określa identyfikator wystąpienia zasad tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d3bee-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="d3bee-148">To polecenie cmdlet pobiera kopie zapasowe urządzeń dla zasad, których ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d3bee-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3bee-149">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d3bee-149">-DeviceName</span></span>
<span data-ttu-id="d3bee-150">Określa nazwę urządzenia StorSimple, dla którego należy pobrać kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="d3bee-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

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

### <span data-ttu-id="d3bee-151">-First</span><span class="sxs-lookup"><span data-stu-id="d3bee-151">-First</span></span>
<span data-ttu-id="d3bee-152">Pobiera tylko określoną liczbę obiektów.</span><span class="sxs-lookup"><span data-stu-id="d3bee-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="d3bee-153">Wprowadź liczbę obiektów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d3bee-153">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="d3bee-154">-Od</span><span class="sxs-lookup"><span data-stu-id="d3bee-154">-From</span></span>
<span data-ttu-id="d3bee-155">Określa datę i godzinę rozpoczęcia wykonywania kopii zapasowych, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3bee-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3bee-156">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3bee-156">-Profile</span></span>
<span data-ttu-id="d3bee-157">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3bee-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d3bee-158">-Skip</span><span class="sxs-lookup"><span data-stu-id="d3bee-158">-Skip</span></span>
<span data-ttu-id="d3bee-159">Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="d3bee-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="d3bee-160">Wprowadź liczbę obiektów, które mają zostać pominięte.</span><span class="sxs-lookup"><span data-stu-id="d3bee-160">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="d3bee-161">-To</span><span class="sxs-lookup"><span data-stu-id="d3bee-161">-To</span></span>
<span data-ttu-id="d3bee-162">Określa datę i godzinę zakończenia wykonywania kopii zapasowych, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3bee-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3bee-163">-Volume</span><span class="sxs-lookup"><span data-stu-id="d3bee-163">-Volume</span></span>
<span data-ttu-id="d3bee-164">Określa obiekt **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="d3bee-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="d3bee-165">To polecenie cmdlet wykorzystuje **Identyfikator InstanceId** tego obiektu do określenia woluminu, w którym istnieją kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="d3bee-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="d3bee-166">Aby uzyskać obiekt **VirtualDisk** , użyj parametru **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="d3bee-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3bee-167">-Identyfikator woluminu</span><span class="sxs-lookup"><span data-stu-id="d3bee-167">-VolumeId</span></span>
<span data-ttu-id="d3bee-168">Określa identyfikator wystąpienia woluminu, w którym istnieją kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="d3bee-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3bee-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3bee-169">CommonParameters</span></span>
<span data-ttu-id="d3bee-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3bee-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3bee-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3bee-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3bee-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3bee-172">INPUTS</span></span>

### <span data-ttu-id="d3bee-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="d3bee-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="d3bee-174">To polecenie cmdlet umożliwia akceptowanie obiektów **BackupPolicyDetails** i **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="d3bee-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="d3bee-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3bee-175">OUTPUTS</span></span>

### <span data-ttu-id="d3bee-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="d3bee-176">IList\<Backup\></span></span>
<span data-ttu-id="d3bee-177">To polecenie cmdlet zwraca listę obiektów **kopii zapasowej** .</span><span class="sxs-lookup"><span data-stu-id="d3bee-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="d3bee-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3bee-178">NOTES</span></span>

## <span data-ttu-id="d3bee-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3bee-179">RELATED LINKS</span></span>

[<span data-ttu-id="d3bee-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="d3bee-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="d3bee-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d3bee-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="d3bee-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="d3bee-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


