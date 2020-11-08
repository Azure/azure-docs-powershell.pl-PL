---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054489"
---
# <span data-ttu-id="8aca7-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="8aca7-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="8aca7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8aca7-102">SYNOPSIS</span></span>
<span data-ttu-id="8aca7-103">Tworzy wolumin w określonym kontenerze woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="8aca7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8aca7-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8aca7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8aca7-105">DESCRIPTION</span></span>
<span data-ttu-id="8aca7-106">Polecenie cmdlet **New-AzureStorSimpleDeviceVolume** tworzy wolumin w określonym kontenerze woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="8aca7-107">To polecenie cmdlet kojarzy każdy wolumin z jednym lub kilkoma rekordami kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="8aca7-108">Aby uzyskać obiekty **AccessControlRecord** , użyj polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="8aca7-109">Określ nazwę, rozmiar i AppType dla woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="8aca7-110">Określ także, czy chcesz utworzyć wolumin w trybie online, czy włączyć opcję tworzenia kopii zapasowej, czy włączyć monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="8aca7-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="8aca7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8aca7-111">EXAMPLES</span></span>

### <span data-ttu-id="8aca7-112">Przykład 1. Tworzenie woluminu</span><span class="sxs-lookup"><span data-stu-id="8aca7-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="8aca7-113">Pierwsze polecenie pobiera rekordy kontroli dostępu w konfiguracji usługi StorSimple managera przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** , a następnie zapisuje je w zmiennej $AcrList.</span><span class="sxs-lookup"><span data-stu-id="8aca7-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="8aca7-114">Drugie polecenie pobiera kontener woluminu o nazwie VolumeContainer07 dla urządzenia o nazwie Contoso63-AppVm przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="8aca7-115">Polecenie przekazuje ten kontener do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8aca7-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8aca7-116">To polecenie cmdlet tworzy wolumin.</span><span class="sxs-lookup"><span data-stu-id="8aca7-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="8aca7-117">Polecenie określa nazwę woluminu, rozmiar i rekordy kontroli dostępu przechowywane w $AcrList.</span><span class="sxs-lookup"><span data-stu-id="8aca7-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="8aca7-118">To polecenie uruchamia zadanie, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="8aca7-119">Aby wyświetlić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="8aca7-120">Przykład 2: Tworzenie woluminu bez dostępu Controlaccess kontrolka sterowania recordsaccess</span><span class="sxs-lookup"><span data-stu-id="8aca7-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="8aca7-121">To polecenie pobiera kontener woluminu o nazwie VolumeContainer01 dla urządzenia o nazwie Contoso63-AppVm przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="8aca7-122">Polecenie przekazuje ten kontener do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8aca7-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8aca7-123">To polecenie cmdlet tworzy wolumin.</span><span class="sxs-lookup"><span data-stu-id="8aca7-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="8aca7-124">Polecenie określa nazwę woluminu, rozmiar i wartość pustą dla rekordów kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="8aca7-125">To polecenie określa parametr *WaitForComplete* , więc zwraca **TaskStatusInfo** po utworzeniu woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="8aca7-126">Ponieważ polecenie nie określa rekordów kontroli dostępu, nie można uzyskać dostępu do tego woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="8aca7-127">Program Access można dodać później, korzystając z polecenia cmdlet **Set-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="8aca7-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8aca7-128">PARAMETERS</span></span>

### <span data-ttu-id="8aca7-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="8aca7-129">-AccessControlRecords</span></span>
<span data-ttu-id="8aca7-130">Określa listę rekordów kontroli dostępu, które mają zostać skojarzone z woluminem.</span><span class="sxs-lookup"><span data-stu-id="8aca7-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8aca7-131">-DeviceName</span></span>
<span data-ttu-id="8aca7-132">Określa nazwę urządzenia StorSimple, na którym ma być utworzony wolumin.</span><span class="sxs-lookup"><span data-stu-id="8aca7-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="8aca7-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="8aca7-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="8aca7-134">Określa, czy włączyć domyślną kopię zapasową woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-134">Specifies whether to enable default backup for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="8aca7-135">-EnableMonitoring</span></span>
<span data-ttu-id="8aca7-136">Określa, czy włączyć monitorowanie dla woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-136">Specifies whether to enable monitoring for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-137">-Online</span><span class="sxs-lookup"><span data-stu-id="8aca7-137">-Online</span></span>
<span data-ttu-id="8aca7-138">Określa, czy utworzyć wolumin w trybie online.</span><span class="sxs-lookup"><span data-stu-id="8aca7-138">Specifies whether to create the volume online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="8aca7-139">-Profile</span></span>
<span data-ttu-id="8aca7-140">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8aca7-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8aca7-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="8aca7-141">-VolumeAppType</span></span>
<span data-ttu-id="8aca7-142">Określa, czy ma zostać utworzony wolumin podstawowy, czy archiwum.</span><span class="sxs-lookup"><span data-stu-id="8aca7-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="8aca7-143">Prawidłowe wartości to: PrimaryVolume oraz ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="8aca7-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8aca7-144">-VolumeContainer</span></span>
<span data-ttu-id="8aca7-145">Określa kontener jako obiekt kontenera **datacontainer** , w którym można utworzyć wolumin.</span><span class="sxs-lookup"><span data-stu-id="8aca7-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="8aca7-146">Aby uzyskać obiekt **VirtualDisk** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="8aca7-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-147">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="8aca7-147">-VolumeName</span></span>
<span data-ttu-id="8aca7-148">Określa nazwę nowego woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="8aca7-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="8aca7-150">Określa rozmiar woluminu w bajtach.</span><span class="sxs-lookup"><span data-stu-id="8aca7-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aca7-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8aca7-151">-WaitForComplete</span></span>
<span data-ttu-id="8aca7-152">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="8aca7-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="8aca7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aca7-153">CommonParameters</span></span>
<span data-ttu-id="8aca7-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aca7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aca7-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aca7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aca7-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aca7-156">INPUTS</span></span>

### <span data-ttu-id="8aca7-157">Kontenery z, lista\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="8aca7-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="8aca7-158">To polecenie cmdlet akceptuje obiekt **Datakonteneru** oraz listę obiektów **AccessControlRecord** dla nowego woluminu.</span><span class="sxs-lookup"><span data-stu-id="8aca7-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="8aca7-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8aca7-159">OUTPUTS</span></span>

### <span data-ttu-id="8aca7-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="8aca7-160">TaskStatusInfo</span></span>
<span data-ttu-id="8aca7-161">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="8aca7-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="8aca7-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8aca7-162">NOTES</span></span>

## <span data-ttu-id="8aca7-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aca7-163">RELATED LINKS</span></span>

[<span data-ttu-id="8aca7-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="8aca7-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="8aca7-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="8aca7-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="8aca7-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="8aca7-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="8aca7-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="8aca7-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="8aca7-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8aca7-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="8aca7-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="8aca7-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


