---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055415"
---
# <span data-ttu-id="e0403-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e0403-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="e0403-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0403-102">SYNOPSIS</span></span>
<span data-ttu-id="e0403-103">Usuwa istniejące poświadczenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0403-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="e0403-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0403-104">SYNTAX</span></span>

### <span data-ttu-id="e0403-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="e0403-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0403-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="e0403-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0403-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e0403-107">DESCRIPTION</span></span>
<span data-ttu-id="e0403-108">Polecenie cmdlet **Remove-AzureStorSimpleStorageAccountCredential** usuwa istniejące poświadczenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0403-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="e0403-109">Określ konto według nazwy lub użyj polecenia cmdlet **Get-AzureStorSimpleStorageAccountCredential** , aby uzyskać obiekt **StorageAccountCredential** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e0403-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="e0403-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0403-110">EXAMPLES</span></span>

### <span data-ttu-id="e0403-111">Przykład 1: usuwanie poświadczenia konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e0403-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="e0403-112">To polecenie umożliwia usunięcie poświadczenia konta dla konta magazynu o nazwie ContosoStorage07.</span><span class="sxs-lookup"><span data-stu-id="e0403-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="e0403-113">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="e0403-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e0403-114">Polecenie cmdlet usuwa poświadczenie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0403-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="e0403-115">Przykład 2: usuwanie poświadczenia konta magazynu przy użyciu operatora potoku</span><span class="sxs-lookup"><span data-stu-id="e0403-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="e0403-116">To polecenie uzyskuje konto magazynu o nazwie ContosoStorage07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleStorageAccountCredential** , a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0403-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="e0403-117">Bieżące polecenie cmdlet usuwa poświadczenie dla tego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0403-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="e0403-118">To polecenie określa parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="e0403-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="e0403-119">Polecenie cmdlet nie zwraca kontrolki do konsoli, dopóki nie zakończy się operacja usuwania.</span><span class="sxs-lookup"><span data-stu-id="e0403-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="e0403-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0403-120">PARAMETERS</span></span>

### <span data-ttu-id="e0403-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e0403-121">-Force</span></span>
<span data-ttu-id="e0403-122">Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0403-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="e0403-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0403-123">-Profile</span></span>
<span data-ttu-id="e0403-124">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0403-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e0403-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="e0403-125">-SAC</span></span>
<span data-ttu-id="e0403-126">Określa poświadczenia jako obiekt **StorageAccountCredential** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e0403-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="e0403-127">Aby uzyskać obiekt **StorageAccountCredential** , użyj polecenia cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="e0403-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0403-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e0403-128">-StorageAccountName</span></span>
<span data-ttu-id="e0403-129">Określa nazwę poświadczenia konta magazynu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e0403-129">Specifies the name of the storage account credential to delete.</span></span>

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

### <span data-ttu-id="e0403-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e0403-130">-WaitForComplete</span></span>
<span data-ttu-id="e0403-131">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="e0403-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e0403-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0403-132">CommonParameters</span></span>
<span data-ttu-id="e0403-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0403-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0403-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0403-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0403-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0403-135">INPUTS</span></span>

### <span data-ttu-id="e0403-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e0403-136">StorageAccountCredential</span></span>
<span data-ttu-id="e0403-137">To polecenie cmdlet akceptuje obiekt **StorageAccountCredential** za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="e0403-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="e0403-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0403-138">OUTPUTS</span></span>

### <span data-ttu-id="e0403-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="e0403-139">TaskStatusInfo</span></span>
<span data-ttu-id="e0403-140">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="e0403-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="e0403-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0403-141">NOTES</span></span>

## <span data-ttu-id="e0403-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0403-142">RELATED LINKS</span></span>

[<span data-ttu-id="e0403-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e0403-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="e0403-144">Nowe — AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e0403-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="e0403-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e0403-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="e0403-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e0403-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


