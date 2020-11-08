---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054993"
---
# <span data-ttu-id="f7aeb-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7aeb-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="f7aeb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="f7aeb-103">Rozpoczyna nowe zadanie tworzenia kopii zapasowej z istniejących zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="f7aeb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7aeb-104">SYNTAX</span></span>

### <span data-ttu-id="f7aeb-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f7aeb-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f7aeb-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="f7aeb-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f7aeb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7aeb-107">DESCRIPTION</span></span>
<span data-ttu-id="f7aeb-108">Polecenie cmdlet **Start-AzureStorSimpleDeviceBackupJob** rozpoczyna nowe zadanie, które tworzy kopię zapasową z istniejących zasad tworzenia kopii zapasowych na urządzeniu z systemem StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="f7aeb-109">Domyślnie to polecenie cmdlet tworzy kopię zapasową lokalnej migawki.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="f7aeb-110">Aby utworzyć kopię zapasową w chmurze, określ wartość CloudSnapshot dla parametru *backuptype* .</span><span class="sxs-lookup"><span data-stu-id="f7aeb-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="f7aeb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7aeb-111">EXAMPLES</span></span>

### <span data-ttu-id="f7aeb-112">Przykład 1. Tworzenie kopii zapasowej lokalnej migawki</span><span class="sxs-lookup"><span data-stu-id="f7aeb-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="f7aeb-113">To polecenie tworzy kopię zapasową lokalnej migawki dla określonego identyfikatora zasad.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="f7aeb-114">To polecenie uruchamia zadanie, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="f7aeb-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="f7aeb-115">Aby wyświetlić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="f7aeb-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="f7aeb-116">Przykład 2: Tworzenie kopii zapasowej migawki w chmurze i oczekiwanie na zakończenie</span><span class="sxs-lookup"><span data-stu-id="f7aeb-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="f7aeb-117">To polecenie tworzy kopię zapasową migawki chmury dla określonego identyfikatora zasad.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="f7aeb-118">To polecenie określa parametr *WaitForComplete* , więc polecenie wykonuje zadanie, a następnie zwraca obiekt **TaskStatusInfo** dla zadania.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="f7aeb-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7aeb-119">PARAMETERS</span></span>

### <span data-ttu-id="f7aeb-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="f7aeb-120">-BackupPolicyId</span></span>
<span data-ttu-id="f7aeb-121">Określa identyfikator zasad tworzenia kopii zapasowych, które mają zostać użyte do utworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="f7aeb-122">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="f7aeb-122">-BackupType</span></span>
<span data-ttu-id="f7aeb-123">Określa typ kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-123">Specifies the backup type.</span></span>
<span data-ttu-id="f7aeb-124">Prawidłowe wartości to: LocalSnapshot oraz CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7aeb-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f7aeb-125">-DeviceName</span></span>
<span data-ttu-id="f7aeb-126">Określa nazwę urządzenia StorSimple, na którym ma zostać uruchomione zadanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="f7aeb-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="f7aeb-127">-Profile</span></span>
<span data-ttu-id="f7aeb-128">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f7aeb-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f7aeb-129">-WaitForComplete</span></span>
<span data-ttu-id="f7aeb-130">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f7aeb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7aeb-131">CommonParameters</span></span>
<span data-ttu-id="f7aeb-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7aeb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7aeb-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7aeb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7aeb-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7aeb-134">INPUTS</span></span>

### <span data-ttu-id="f7aeb-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7aeb-135">None</span></span>

## <span data-ttu-id="f7aeb-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7aeb-136">OUTPUTS</span></span>

### <span data-ttu-id="f7aeb-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="f7aeb-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="f7aeb-138">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="f7aeb-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="f7aeb-139">Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="f7aeb-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="f7aeb-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7aeb-140">NOTES</span></span>

## <span data-ttu-id="f7aeb-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7aeb-141">RELATED LINKS</span></span>

[<span data-ttu-id="f7aeb-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="f7aeb-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="f7aeb-143">Start — AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="f7aeb-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


