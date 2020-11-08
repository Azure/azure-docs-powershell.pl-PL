---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055433"
---
# <span data-ttu-id="f4cc7-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="f4cc7-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="f4cc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cc7-103">Usuwa obiekt kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-103">Deletes a backup object.</span></span>

## <span data-ttu-id="f4cc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4cc7-104">SYNTAX</span></span>

### <span data-ttu-id="f4cc7-105">IdentifyById (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4cc7-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4cc7-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="f4cc7-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4cc7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4cc7-107">DESCRIPTION</span></span>
<span data-ttu-id="f4cc7-108">Polecenie cmdlet **Remove-AzureStorSimpleDeviceBackup** usuwa jeden obiekt kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="f4cc7-109">Jeśli spróbujesz usunąć kopię zapasową, która została już usunięta, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="f4cc7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4cc7-110">EXAMPLES</span></span>

### <span data-ttu-id="f4cc7-111">Przykład 1: Usuwanie kopii zapasowej urządzenia</span><span class="sxs-lookup"><span data-stu-id="f4cc7-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="f4cc7-112">To polecenie usuwa kopię zapasową z określonym IDENTYFIKATORem urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f4cc7-113">Polecenie rozpoczyna operację, która usuwa obiekt **kopii zapasowej** , a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="f4cc7-114">Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="f4cc7-115">Przykład 2: usunięcie pierwszej kopii zapasowej urządzenia przy użyciu jego identyfikatora</span><span class="sxs-lookup"><span data-stu-id="f4cc7-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="f4cc7-116">Pierwsze polecenie pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm, a następnie zapisuje je w zmiennej $Backup.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="f4cc7-117">Drugie polecenie usuwa kopię zapasową z urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f4cc7-118">W poleceniu użyto standardowego zapisu kropkowego, aby odwołać się do właściwości **InstanceId** pierwszego elementu tablicy $Backup.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="f4cc7-119">To polecenie określa parametr *WaitForComplete* , a więc polecenie czeka na zakończenie operacji, a następnie zwraca obiekt **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="f4cc7-120">Przykład 3: usunięcie pierwszej kopii zapasowej urządzenia za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="f4cc7-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="f4cc7-121">Pierwsze polecenie pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm, a następnie zapisuje je w zmiennej $Backup.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="f4cc7-122">Drugie polecenie przekazuje pierwszy obiekt przechowywany w tablicy $Backup do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="f4cc7-123">To polecenie cmdlet usuwa kopię zapasową z urządzenia o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f4cc7-124">To polecenie określa parametr *WaitForComplete* , a więc polecenie czeka na zakończenie operacji, a następnie zwraca obiekt **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="f4cc7-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4cc7-125">PARAMETERS</span></span>

### <span data-ttu-id="f4cc7-126">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="f4cc7-126">-Backup</span></span>
<span data-ttu-id="f4cc7-127">Określa obiekt **kopii zapasowej** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="f4cc7-128">Aby uzyskać obiekt **kopii zapasowej** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cc7-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f4cc7-129">-BackupId</span></span>
<span data-ttu-id="f4cc7-130">Określa identyfikator wystąpienia kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="f4cc7-131">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f4cc7-131">-DeviceName</span></span>
<span data-ttu-id="f4cc7-132">Określa nazwę urządzenia StorSimple, na którym należy usunąć kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="f4cc7-133">-Force</span><span class="sxs-lookup"><span data-stu-id="f4cc7-133">-Force</span></span>
<span data-ttu-id="f4cc7-134">Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="f4cc7-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4cc7-135">-Profile</span></span>
<span data-ttu-id="f4cc7-136">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f4cc7-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f4cc7-137">-WaitForComplete</span></span>
<span data-ttu-id="f4cc7-138">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f4cc7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cc7-139">CommonParameters</span></span>
<span data-ttu-id="f4cc7-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cc7-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cc7-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4cc7-142">INPUTS</span></span>

### <span data-ttu-id="f4cc7-143">Wykonania</span><span class="sxs-lookup"><span data-stu-id="f4cc7-143">Backup</span></span>

## <span data-ttu-id="f4cc7-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4cc7-144">OUTPUTS</span></span>

### <span data-ttu-id="f4cc7-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="f4cc7-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="f4cc7-146">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określono parametr *WaitForComplete* , jeśli nie określono tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="f4cc7-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="f4cc7-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4cc7-147">NOTES</span></span>

## <span data-ttu-id="f4cc7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4cc7-148">RELATED LINKS</span></span>

[<span data-ttu-id="f4cc7-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="f4cc7-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


