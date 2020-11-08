---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054713"
---
# <span data-ttu-id="928d1-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="928d1-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="928d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="928d1-102">SYNOPSIS</span></span>
<span data-ttu-id="928d1-103">Rozpoczyna zadanie przywracające kopię zapasową na urządzeniu StorSimple.</span><span class="sxs-lookup"><span data-stu-id="928d1-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="928d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="928d1-104">SYNTAX</span></span>

### <span data-ttu-id="928d1-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="928d1-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="928d1-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="928d1-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="928d1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="928d1-107">DESCRIPTION</span></span>
<span data-ttu-id="928d1-108">Polecenie cmdlet **Start-AzureStorSimpleDeviceBackupRestoreJob** rozpoczyna zadanie przywracające kopię zapasową na urządzeniu StorSimple.</span><span class="sxs-lookup"><span data-stu-id="928d1-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="928d1-109">Określ identyfikator kopii zapasowej oraz opcjonalny identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="928d1-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="928d1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="928d1-110">EXAMPLES</span></span>

### <span data-ttu-id="928d1-111">Przykład 1. uruchomienie zadania przywrócenia kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="928d1-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="928d1-112">To polecenie uruchamia zadanie, które przywraca obiekt kopii zapasowej o określonym IDENTYFIKATORze i skojarzone z nim migawki na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="928d1-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="928d1-113">Polecenie określa parametr *WaitForComplete* , więc zadanie kończy się, zanim polecenie cmdlet zwróci sterowanie do konsoli.</span><span class="sxs-lookup"><span data-stu-id="928d1-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="928d1-114">Przykład 2: rozpoczęcie zadania przywrócenia konkretnej migawki</span><span class="sxs-lookup"><span data-stu-id="928d1-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="928d1-115">To polecenie uruchamia zadanie, które powoduje przywrócenie migawki kopii zapasowej o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="928d1-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="928d1-116">Polecenie określa obiekt kopii zapasowej według identyfikatora na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="928d1-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="928d1-117">Polecenie określa parametr *Force* , więc rozpoczyna zadanie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="928d1-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="928d1-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="928d1-118">PARAMETERS</span></span>

### <span data-ttu-id="928d1-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="928d1-119">-BackupId</span></span>
<span data-ttu-id="928d1-120">Określa identyfikator wystąpienia kopii zapasowej do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="928d1-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="928d1-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="928d1-121">-DeviceName</span></span>
<span data-ttu-id="928d1-122">Określa nazwę urządzenia StorSimple, na którym znajduje się kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="928d1-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="928d1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="928d1-123">-Force</span></span>
<span data-ttu-id="928d1-124">Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="928d1-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="928d1-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="928d1-125">-Profile</span></span>
<span data-ttu-id="928d1-126">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="928d1-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="928d1-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="928d1-127">-SnapshotId</span></span>
<span data-ttu-id="928d1-128">Określa identyfikator wystąpienia migawki do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="928d1-128">Specifies the instance ID of the snapshot to restore.</span></span>

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

### <span data-ttu-id="928d1-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="928d1-129">-WaitForComplete</span></span>
<span data-ttu-id="928d1-130">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="928d1-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="928d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928d1-131">CommonParameters</span></span>
<span data-ttu-id="928d1-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928d1-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928d1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928d1-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="928d1-134">INPUTS</span></span>

### <span data-ttu-id="928d1-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="928d1-135">None</span></span>

## <span data-ttu-id="928d1-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="928d1-136">OUTPUTS</span></span>

### <span data-ttu-id="928d1-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="928d1-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="928d1-138">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="928d1-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="928d1-139">Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="928d1-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="928d1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="928d1-140">NOTES</span></span>

## <span data-ttu-id="928d1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="928d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="928d1-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="928d1-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="928d1-143">Start — AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="928d1-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


