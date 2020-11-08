---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055062"
---
# <span data-ttu-id="c4925-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="c4925-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="c4925-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4925-102">SYNOPSIS</span></span>
<span data-ttu-id="c4925-103">Usuwa rekord kontroli dostępu z konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="c4925-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="c4925-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4925-104">SYNTAX</span></span>

### <span data-ttu-id="c4925-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="c4925-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c4925-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="c4925-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4925-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c4925-107">DESCRIPTION</span></span>
<span data-ttu-id="c4925-108">Polecenie cmdlet **Remove-AzureStorSimpleAccessControlRecord** usuwa rekord kontroli dostępu z konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="c4925-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="c4925-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4925-109">EXAMPLES</span></span>

### <span data-ttu-id="c4925-110">Przykład 1: usuwanie kontrolki sterowania Controlaccess w programie Access recordaccess</span><span class="sxs-lookup"><span data-stu-id="c4925-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="c4925-111">To polecenie usuwa rekord kontroli dostępu o nazwie Acr10.</span><span class="sxs-lookup"><span data-stu-id="c4925-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="c4925-112">To polecenie określa parametr *WaitForComplete* , a więc polecenie czeka na zakończenie operacji, a następnie zwraca obiekt **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="c4925-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="c4925-113">Przykład 2: Usuwanie rekordu kontrolki programu Access Controlaccess przy użyciu pipelineAccess Controlaccess Controlaccess</span><span class="sxs-lookup"><span data-stu-id="c4925-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="c4925-114">To polecenie używa polecenia **Get-AzureStorSimpleAccessControlRecord** w celu uzyskania **AccessControlRecord** o nazwie Acr10, a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c4925-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c4925-115">Polecenie rozpoczyna operację usuwającą obiekt **AccessControlRecord** , a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="c4925-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="c4925-116">Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="c4925-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="c4925-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4925-117">PARAMETERS</span></span>

### <span data-ttu-id="c4925-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="c4925-118">-ACR</span></span>
<span data-ttu-id="c4925-119">Określa obiekt **AccessControlRecord** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c4925-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="c4925-120">Aby uzyskać obiekt **AccessControlRecord** , użyj polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="c4925-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4925-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="c4925-121">-ACRName</span></span>
<span data-ttu-id="c4925-122">Określa nazwę rekordu kontroli dostępu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c4925-122">Specifies a name of the access control record to delete.</span></span>

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

### <span data-ttu-id="c4925-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c4925-123">-Force</span></span>
<span data-ttu-id="c4925-124">Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c4925-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="c4925-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4925-125">-Profile</span></span>
<span data-ttu-id="c4925-126">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4925-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c4925-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="c4925-127">-WaitForComplete</span></span>
<span data-ttu-id="c4925-128">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="c4925-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="c4925-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4925-129">CommonParameters</span></span>
<span data-ttu-id="c4925-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4925-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4925-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4925-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4925-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4925-132">INPUTS</span></span>

### <span data-ttu-id="c4925-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="c4925-133">AccessControlRecord</span></span>
<span data-ttu-id="c4925-134">To polecenie cmdlet akceptuje obiekt **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="c4925-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="c4925-135">Obiekt **AccessControlRecord** zawiera następujące pola:</span><span class="sxs-lookup"><span data-stu-id="c4925-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="c4925-136">**GlobalId** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="c4925-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="c4925-137">**Initiatorname** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="c4925-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="c4925-138">**InstanceId** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="c4925-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="c4925-139">**Name** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="c4925-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="c4925-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="c4925-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="c4925-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="c4925-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="c4925-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4925-142">OUTPUTS</span></span>

### <span data-ttu-id="c4925-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="c4925-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="c4925-144">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="c4925-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="c4925-145">Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="c4925-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="c4925-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4925-146">NOTES</span></span>

## <span data-ttu-id="c4925-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4925-147">RELATED LINKS</span></span>

[<span data-ttu-id="c4925-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="c4925-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="c4925-149">Nowe — AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="c4925-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="c4925-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="c4925-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="c4925-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="c4925-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


