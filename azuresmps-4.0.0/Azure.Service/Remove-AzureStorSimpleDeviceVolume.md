---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055426"
---
# <span data-ttu-id="7b642-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7b642-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="7b642-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b642-102">SYNOPSIS</span></span>
<span data-ttu-id="7b642-103">Usuwa wolumin z urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="7b642-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="7b642-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b642-104">SYNTAX</span></span>

### <span data-ttu-id="7b642-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="7b642-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7b642-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="7b642-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7b642-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7b642-107">DESCRIPTION</span></span>
<span data-ttu-id="7b642-108">Polecenie cmdlet **Remove-AzureStorSimpleDeviceVolume** usuwa wolumin z urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="7b642-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="7b642-109">To polecenie cmdlet monituje o potwierdzenie, o ile nie określi się parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="7b642-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="7b642-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b642-110">EXAMPLES</span></span>

### <span data-ttu-id="7b642-111">Przykład 1: Usuwanie woluminu za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="7b642-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="7b642-112">To polecenie pobiera wolumin o nazwie Volume18 na urządzeniu o nazwie Contoso63-AppVm, a następnie przekazuje ten wolumin do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7b642-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b642-113">Bieżące polecenie cmdlet rozpoczyna zadanie, które usuwa wolumin, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="7b642-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="7b642-114">Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="7b642-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="7b642-115">Polecenie nie określa parametru *Force* , więc polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7b642-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="7b642-116">Przykład 2: Usuwanie woluminu bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="7b642-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="7b642-117">To polecenie usuwa wolumin o nazwie Volume18 z urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="7b642-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="7b642-118">Polecenie określa parametr *Force* , więc polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7b642-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7b642-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b642-119">PARAMETERS</span></span>

### <span data-ttu-id="7b642-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7b642-120">-DeviceName</span></span>
<span data-ttu-id="7b642-121">Określa nazwę urządzenia StorSimple, na którym ma zostać usunięty wolumin.</span><span class="sxs-lookup"><span data-stu-id="7b642-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="7b642-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7b642-122">-Force</span></span>
<span data-ttu-id="7b642-123">Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7b642-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="7b642-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="7b642-124">-Profile</span></span>
<span data-ttu-id="7b642-125">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7b642-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7b642-126">-Volume</span><span class="sxs-lookup"><span data-stu-id="7b642-126">-Volume</span></span>
<span data-ttu-id="7b642-127">Określa wolumin, który należy usunąć, jako obiekt **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="7b642-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="7b642-128">Aby uzyskać obiekt **VirtualDisk** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="7b642-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

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

### <span data-ttu-id="7b642-129">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="7b642-129">-VolumeName</span></span>
<span data-ttu-id="7b642-130">Określa nazwę woluminu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="7b642-130">Specifies the name of the volume to remove.</span></span>

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

### <span data-ttu-id="7b642-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7b642-131">-WaitForComplete</span></span>
<span data-ttu-id="7b642-132">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="7b642-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7b642-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b642-133">CommonParameters</span></span>
<span data-ttu-id="7b642-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b642-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b642-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b642-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b642-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b642-136">INPUTS</span></span>

### <span data-ttu-id="7b642-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="7b642-137">VirtualDisk</span></span>
<span data-ttu-id="7b642-138">To polecenie cmdlet umożliwia zaakceptowanie usunięcia obiektu **VirtualDisk** lub nazwy woluminu **VirtualDisk** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="7b642-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="7b642-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b642-139">OUTPUTS</span></span>

### <span data-ttu-id="7b642-140">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="7b642-140">TaskStatusInfo</span></span>
<span data-ttu-id="7b642-141">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="7b642-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="7b642-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b642-142">NOTES</span></span>

## <span data-ttu-id="7b642-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b642-143">RELATED LINKS</span></span>

[<span data-ttu-id="7b642-144">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7b642-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7b642-145">Nowe — AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7b642-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7b642-146">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7b642-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7b642-147">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="7b642-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


