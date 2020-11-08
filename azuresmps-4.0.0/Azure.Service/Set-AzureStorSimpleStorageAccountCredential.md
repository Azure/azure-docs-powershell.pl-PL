---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054817"
---
# <span data-ttu-id="2eee2-101">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2eee2-101">Set-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="2eee2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eee2-102">SYNOPSIS</span></span>
<span data-ttu-id="2eee2-103">Aktualizuje poświadczenia usługi Azure Storage Access.</span><span class="sxs-lookup"><span data-stu-id="2eee2-103">Updates an Azure storage access credential.</span></span>

## <span data-ttu-id="2eee2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eee2-104">SYNTAX</span></span>

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2eee2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2eee2-105">DESCRIPTION</span></span>
<span data-ttu-id="2eee2-106">Polecenie cmdlet **Set-AzureStorSimpleStorageAccountCredential** aktualizuje istniejące poświadczenia usługi Azure Storage Access używane przez StorSimple OneSDK polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eee2-106">The **Set-AzureStorSimpleStorageAccountCredential** cmdlet update an existing Azure storage access credential for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="2eee2-107">Aby uzyskać więcej informacji o tym, jak polecenia cmdlet StorSimple działają z kontami magazynu, zobacz temat pomocy dla New-AzureStorSimpleStorageAccountCredential polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eee2-107">For more information about how StorSimple cmdlets work with storage accounts, see the help topic for the New-AzureStorSimpleStorageAccountCredential cmdlet.</span></span>

## <span data-ttu-id="2eee2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eee2-108">EXAMPLES</span></span>

### <span data-ttu-id="2eee2-109">Przykład 1: modyfikowanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="2eee2-109">Example 1: Modify a credential</span></span>
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="2eee2-110">To polecenie powoduje zmianę poświadczeń konta magazynu o nazwie ContosoStorage01, aby nie wymagała już protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="2eee2-110">This command changes the storage account credential named ContosoStorage01 to no longer require SSL.</span></span>

## <span data-ttu-id="2eee2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eee2-111">PARAMETERS</span></span>

### <span data-ttu-id="2eee2-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="2eee2-112">-Profile</span></span>
<span data-ttu-id="2eee2-113">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2eee2-113">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="2eee2-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2eee2-114">-StorageAccountKey</span></span>
<span data-ttu-id="2eee2-115">Określa klucz dostępu konta magazynu w postaci zwykłego tekstu.</span><span class="sxs-lookup"><span data-stu-id="2eee2-115">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eee2-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2eee2-116">-StorageAccountName</span></span>
<span data-ttu-id="2eee2-117">Określa nazwę istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2eee2-117">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="2eee2-118">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="2eee2-118">-UseSSL</span></span>
<span data-ttu-id="2eee2-119">Wskazuje, czy przy użyciu nowego poświadczenia konta magazynu ma być używane połączenie SSL.</span><span class="sxs-lookup"><span data-stu-id="2eee2-119">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

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

### <span data-ttu-id="2eee2-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="2eee2-120">-WaitForComplete</span></span>
<span data-ttu-id="2eee2-121">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="2eee2-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="2eee2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eee2-122">CommonParameters</span></span>
<span data-ttu-id="2eee2-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eee2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eee2-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eee2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eee2-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eee2-125">INPUTS</span></span>

### <span data-ttu-id="2eee2-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2eee2-126">None</span></span>

## <span data-ttu-id="2eee2-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eee2-127">OUTPUTS</span></span>

### <span data-ttu-id="2eee2-128">StorageAccountCredentialResponse, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="2eee2-128">StorageAccountCredentialResponse, TaskResponse</span></span>
<span data-ttu-id="2eee2-129">To polecenie cmdlet zwraca obiekt **StorageAccountCredentialResponse** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="2eee2-129">This cmdlet returns a **StorageAccountCredentialResponse** object, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="2eee2-130">Jeśli nie określisz tego parametru, polecenie cmdlet zwróci obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="2eee2-130">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="2eee2-131">**StorageAccountCredentialResponse** zawiera następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="2eee2-131">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="2eee2-132">Nr **chmury** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-132">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="2eee2-133">**Nazwa_hosta** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-133">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="2eee2-134">**InstanceId** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-134">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="2eee2-135">**IsDefault** ( **wartość logiczna** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-135">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="2eee2-136">**Lokalizacja** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-136">**Location** ( **String** )</span></span>
- <span data-ttu-id="2eee2-137">**Login** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-137">**Login** ( **String** )</span></span>
- <span data-ttu-id="2eee2-138">**Name** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-138">**Name** ( **String** )</span></span>
- <span data-ttu-id="2eee2-139">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-139">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="2eee2-140">**Hasło** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-140">**Password** ( **String** )</span></span>
- <span data-ttu-id="2eee2-141">**PasswordEncryptionCertThumbprint** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-141">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="2eee2-142">**UseSSL** ( **wartość logiczna** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-142">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="2eee2-143">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="2eee2-143">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="2eee2-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eee2-144">NOTES</span></span>

## <span data-ttu-id="2eee2-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eee2-145">RELATED LINKS</span></span>

[<span data-ttu-id="2eee2-146">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2eee2-146">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="2eee2-147">Nowe — AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2eee2-147">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="2eee2-148">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2eee2-148">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)


