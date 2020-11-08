---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055384"
---
# <span data-ttu-id="46290-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="46290-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="46290-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46290-102">SYNOPSIS</span></span>
<span data-ttu-id="46290-103">Aktualizuje właściwości istniejącego woluminu.</span><span class="sxs-lookup"><span data-stu-id="46290-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="46290-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46290-104">SYNTAX</span></span>

### <span data-ttu-id="46290-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="46290-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="46290-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="46290-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="46290-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46290-107">DESCRIPTION</span></span>
<span data-ttu-id="46290-108">Polecenie cmdlet **Set-AzureStorSimpleDeviceVolume** aktualizuje właściwości istniejącego woluminu.</span><span class="sxs-lookup"><span data-stu-id="46290-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="46290-109">To polecenie cmdlet kojarzy wolumin z jednym lub kilkoma rekordami kontroli dostępu.</span><span class="sxs-lookup"><span data-stu-id="46290-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="46290-110">Aby uzyskać obiekty **AccessControlRecord** , użyj polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="46290-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="46290-111">Zaktualizuj rozmiar lub typ woluminu.</span><span class="sxs-lookup"><span data-stu-id="46290-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="46290-112">Zaktualizuj także, czy utworzyć wolumin w trybie online.</span><span class="sxs-lookup"><span data-stu-id="46290-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="46290-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46290-113">EXAMPLES</span></span>

### <span data-ttu-id="46290-114">Przykład 1: aktualizowanie wartości online dla woluminu</span><span class="sxs-lookup"><span data-stu-id="46290-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="46290-115">To polecenie aktualizuje wolumin o nazwie Volume18, aby uzyskać wartość online $False.</span><span class="sxs-lookup"><span data-stu-id="46290-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="46290-116">To polecenie uruchamia zadanie, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="46290-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="46290-117">Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="46290-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="46290-118">Przykład 2: modyfikowanie wartości i typu w trybie online</span><span class="sxs-lookup"><span data-stu-id="46290-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="46290-119">To polecenie aktualizuje wolumin o nazwie Volume18.</span><span class="sxs-lookup"><span data-stu-id="46290-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="46290-120">Modyfikuje typ i zmienia wartość parametru *online* na $true.</span><span class="sxs-lookup"><span data-stu-id="46290-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="46290-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46290-121">PARAMETERS</span></span>

### <span data-ttu-id="46290-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="46290-122">-AccessControlRecords</span></span>
<span data-ttu-id="46290-123">Określa listę rekordów kontroli dostępu, które mają zostać skojarzone z woluminem.</span><span class="sxs-lookup"><span data-stu-id="46290-123">Specifies a list of access control records to associate with the volume.</span></span>

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

### <span data-ttu-id="46290-124">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="46290-124">-DeviceName</span></span>
<span data-ttu-id="46290-125">Określa nazwę urządzenia StorSimple, na którym należy zaktualizować wolumin.</span><span class="sxs-lookup"><span data-stu-id="46290-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="46290-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="46290-126">-InformationAction</span></span>
<span data-ttu-id="46290-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="46290-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46290-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="46290-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46290-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="46290-129">Continue</span></span>
- <span data-ttu-id="46290-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="46290-130">Ignore</span></span>
- <span data-ttu-id="46290-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="46290-131">Inquire</span></span>
- <span data-ttu-id="46290-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="46290-132">SilentlyContinue</span></span>
- <span data-ttu-id="46290-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="46290-133">Stop</span></span>
- <span data-ttu-id="46290-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="46290-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46290-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="46290-135">-InformationVariable</span></span>
<span data-ttu-id="46290-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="46290-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46290-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="46290-137">-NewName</span></span>
<span data-ttu-id="46290-138">Określa nową nazwę urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="46290-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="46290-139">-Online</span><span class="sxs-lookup"><span data-stu-id="46290-139">-Online</span></span>
<span data-ttu-id="46290-140">Określa, czy wolumin jest dostępny w trybie online.</span><span class="sxs-lookup"><span data-stu-id="46290-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46290-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="46290-141">-Profile</span></span>
<span data-ttu-id="46290-142">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="46290-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="46290-143">-Volume</span><span class="sxs-lookup"><span data-stu-id="46290-143">-Volume</span></span>
<span data-ttu-id="46290-144">Określa nazwę woluminu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="46290-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46290-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="46290-145">-VolumeAppType</span></span>
<span data-ttu-id="46290-146">Określa, czy wolumin ma być aktualizowany w woluminie podstawowym, czy archiwalnym.</span><span class="sxs-lookup"><span data-stu-id="46290-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="46290-147">Prawidłowe wartości to: PrimaryVolume oraz ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="46290-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46290-148">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="46290-148">-VolumeName</span></span>
<span data-ttu-id="46290-149">Określa nazwę woluminu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="46290-149">Specifies the name of the volume to update.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46290-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="46290-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="46290-151">Określa zaktualizowany rozmiar woluminu (w bajtach).</span><span class="sxs-lookup"><span data-stu-id="46290-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46290-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="46290-152">-WaitForComplete</span></span>
<span data-ttu-id="46290-153">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="46290-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="46290-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46290-154">CommonParameters</span></span>
<span data-ttu-id="46290-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46290-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46290-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46290-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46290-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46290-157">INPUTS</span></span>

### <span data-ttu-id="46290-158">Lista\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="46290-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="46290-159">To polecenie cmdlet akceptuje listę obiektów **AccessControlRecord** , które mają zostać skojarzone z woluminem.</span><span class="sxs-lookup"><span data-stu-id="46290-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="46290-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46290-160">OUTPUTS</span></span>

### <span data-ttu-id="46290-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="46290-161">TaskStatusInfo</span></span>
<span data-ttu-id="46290-162">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="46290-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="46290-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46290-163">NOTES</span></span>

## <span data-ttu-id="46290-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46290-164">RELATED LINKS</span></span>

[<span data-ttu-id="46290-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="46290-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="46290-166">Nowe — AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="46290-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="46290-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="46290-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="46290-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="46290-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="46290-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="46290-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


