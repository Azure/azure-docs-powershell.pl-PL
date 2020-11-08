---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BDCD6FD8-F4D5-4897-BF91-C78773DD3546
online version: ''
schema: 2.0.0
ms.openlocfilehash: f414f480328d508f0178d2536d144dceda3baab6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054479"
---
# <span data-ttu-id="00b4f-101">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="00b4f-101">New-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="00b4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="00b4f-103">Dodaje poświadczenia usługi Azure Storage Access.</span><span class="sxs-lookup"><span data-stu-id="00b4f-103">Adds an Azure storage access credential.</span></span>

## <span data-ttu-id="00b4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00b4f-104">SYNTAX</span></span>

```
New-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 -UseSSL <Boolean> [-Endpoint <String>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00b4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="00b4f-106">Polecenie cmdlet **New-AzureStorSimpleStorageAccountCredential** umożliwia dodanie poświadczenia usługi Azure Storage Access do Menedżera StorSimple, który będzie używany przez StorSimple OneSDK polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b4f-106">The **New-AzureStorSimpleStorageAccountCredential** cmdlet adds an Azure storage access credential to StorSimple manager for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="00b4f-107">Większość poleceń cmdlet programu StorSimple OneSDK działa z jednostkami, które są ostatecznie powiązane z określonym kontem magazynu, takimi jak woluminy, kontenery woluminów, kopie zapasowe i zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="00b4f-107">Most of the StorSimple OneSDK cmdlets deal with entities that are eventually tied to a specific storage account, such as volumes, volume containers, backups, and backup policies.</span></span>
<span data-ttu-id="00b4f-108">W przypadku kilku poleceń cmdlet należy podać poświadczenia używanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-108">For some cmdlets, you must provide the credentials of the storage account in use.</span></span>
<span data-ttu-id="00b4f-109">Poświadczenie konta magazynu to obiekt programu Access utworzony w OneSDK, który wskazuje istniejące konto usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="00b4f-109">A storage account credential is an access object created in OneSDK that points to an existing Azure storage account.</span></span>
<span data-ttu-id="00b4f-110">Wprowadź nazwę i klucz dostępu istniejącego konta magazynu, aby utworzyć poświadczenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-110">You provide the name and access key of an existing storage account to create a storage account credential.</span></span>
<span data-ttu-id="00b4f-111">Następnie możesz używać tego obiektu poświadczeń z innymi poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b4f-111">You can then use that credential object with other cmdlets.</span></span>

<span data-ttu-id="00b4f-112">To polecenie cmdlet używa klucza rejestracji dostarczanego podczas wybierania zasobu przy użyciu polecenia cmdlet **SELECT-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="00b4f-112">This cmdlet uses the registration key that you provide when you select the resource by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>
<span data-ttu-id="00b4f-113">Upewnij się, że wartość jest poprawie, aby uniknąć błędów szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="00b4f-113">Be sure that value is correct to avoid encryption failure.</span></span>
<span data-ttu-id="00b4f-114">Aby zmodyfikować klucz rejestracji na prawidłową wartość, użyj **opcji Select-AzureStorSimpleResource**.</span><span class="sxs-lookup"><span data-stu-id="00b4f-114">To modify the registration key to a correct value, use **Select-AzureStorSimpleResource**.</span></span>

## <span data-ttu-id="00b4f-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00b4f-115">EXAMPLES</span></span>

### <span data-ttu-id="00b4f-116">Przykład 1. Tworzenie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="00b4f-116">Example 1: Create a credential</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount07" -StorageAccountKey "L/eVcHtvqKjPWm5SaAJXtDlc0d69yVs0ICoZ2XIV1x0r9TqUyQyLUNS8lHvTvRmzdvQhJelav3fYyX7wyAu/SA==" -UseSSL $False -WaitForComplete
VERBOSE: ClientRequestId: f363cda4-54aa-4ee8-a3fa-00651ac86ffb_PS
VERBOSE: Found storage account with name : ContosoAccount07
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 716ce6df-62b3-4d48-8e0e-b0c94eec6934_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 19aa4ef7-2789-4817-980c-19e33d257650_PS

JobId        : 84f74c25-b742-452c-973c-43c7446e9f49
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 72bcdf37-bf06-4dac-adc9-31bb8d06475a_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : b9986714-cef4-4c3f-a719-7acfc9559320
IsDefault                        : False
Location                         : West Europe
Login                            : ContosoAccount07
Name                             : ContosoAccount07
OperationInProgress              : None

Password                         : G1sBQ6/qAN1gyRGRZVarpi7o6ToJl61sGugfeJ75yx7cwyaGLQHjrSEEwhxThbDJkxso2emAOarTe920Uufy
                                   0AmJ9NpBI5hNyIFfwS4Ff+z2WmfKOzApyeofW5Zy7GPufehe/2ondq0XG4pGt3qxHFXNVUuiaPSU6TVWEKSh
                                   hWDaksSXYMGij3DJdZDW1MA49e6Q7OY+rFujbYvi9P2OjVj8T+FbiMtMB5NnQEqE+t3k74RqPIDKU+d3h9x4
                                   rYbAksGPfMvSa0fUipwYJ+Y5/NABA6j/MfB2pNDJbvqDoa1JCX6SKiwL81wmTh78/KnDY5ST3Said5DzKEbR
                                   iYMQZg==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="00b4f-117">To polecenie powoduje utworzenie poświadczenia dostępu do magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-117">This command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="00b4f-118">To polecenie określa parametr *WaitForComplete* , a więc polecenie cmdlet czeka na zakończenie zadania w celu zwrócenia kontroli konsoli.</span><span class="sxs-lookup"><span data-stu-id="00b4f-118">This command specifies the *WaitForComplete* parameter, and, so, the cmdlet waits until the task finishes to return control to the console.</span></span>

### <span data-ttu-id="00b4f-119">Przykład 2: Tworzenie poświadczenia i badanie tego stanu zadania</span><span class="sxs-lookup"><span data-stu-id="00b4f-119">Example 2: Create a credential and query that status of the task</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount08" -Key "6BlMpSVrCQVQy3iOpkxiyY8uk/e3PiHIhadxV4qpPlKInr/eRFrGcWKDrfNC1IHj6oh0If/h3rALdZ0zuaf9cQ==" -UseSSL $True
PS C:\> Get-AzureStorSimpleTask -InstanceId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: 6104a834-ea57-4687-8e0b-1d97dc1c038b_PS
VERBOSE: Found storage account with name : ContosoAccount08
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 1f686fa4-5afc-43c3-87b6-f2da7bf9e65f_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 8acb3770-bd72-43e6-9622-481002ad40b0_PS
53816d8d-a8b5-4c1d-a177-e59007608d6d
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
53816d8d-a8b5-4c1d-a177-e59007608d6d for tracking the task's status
```

<span data-ttu-id="00b4f-120">Pierwsze polecenie tworzy poświadczenie dostępu do magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-120">The first command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="00b4f-121">Polecenie zwraca identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="00b4f-121">The command returns a task ID.</span></span>

<span data-ttu-id="00b4f-122">Drugie polecenie bada stan zadania przy użyciu polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="00b4f-122">The second command queries the status of the task by using the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="00b4f-123">Polecenie określa identyfikator zadania z pierwszego polecenia.</span><span class="sxs-lookup"><span data-stu-id="00b4f-123">The command specifies the task ID from the first command.</span></span>

### <span data-ttu-id="00b4f-124">Przykład 3: Tworzenie poświadczenia do użycia z innym poleceniem cmdlet</span><span class="sxs-lookup"><span data-stu-id="00b4f-124">Example 3: Create a credential to use with another cmdlet</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount09" | New-AzureStorSimpleDeviceVolumeContainer -Name "VC03" -DeviceName "Contoso63-AppVm" -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "<your encryption key>" -WaitForComplete
VERBOSE: ClientRequestId: b1d1e637-cd72-4a1e-95a8-4db1d0b921a7_PS
VERBOSE: ClientRequestId: 71f56ca0-1f0b-4655-9331-4849e096345a_PS
VERBOSE: ClientRequestId: fbdd5a96-c95f-4547-9bcd-376d05543348_PS
VERBOSE: Storage Access Credential with name ContosoAccount09 found! 
VERBOSE: ClientRequestId: b44e0363-9979-4e97-aeb1-d9eb4073a337_PS
VERBOSE: ClientRequestId: a6047943-b01e-44e4-a91d-5103aa80ce57_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: ac2dfd8b-922f-4e4d-8c8d-df1e2f87806c_PS


JobId        : 1cf2db5d-624f-46c4-97b9-c36451ba144e
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 9558414b-0883-4cf6-8a02-40efc7edd80d_PS
BandwidthRate                   : 256
EncryptionKey                   : g53NTgCF3SBVZzzk+9yUz5nZopvZpNr3th92ol7WRO7ZUKhodPm7WNjjHEKB0/V+JY6P68tdaF4JxF5jH58e/
                                  mCtTvnPNpOxykYFdY9GKGd9gnf+36sUPqiLFP+ONO5nN/N/zFmOeyuySsaa3gJsZG8eIiFc821yfe9m5QPbF
                                  bx/Qyu8qLl1R1LrKU7k+46IXfwQYSyclztydyuzvFUUic9kaJuR3944VLvrjvxJIbnLrYy7hsn+Gfq7ds9NFq
                                  AUILBH0+bk2uWgUlofAcE8fJ/rzDAHr8nFGWxOTJSrqAo0J3st8BN39+BcrY+zOWsMc/vKfc+Ss5PsGVGDT1r
                                  eQ==
InstanceId                      : 60c34706-ef0c-4c6f-ad90-7249f42648f7
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VC03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="00b4f-125">To polecenie tworzy poświadczenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-125">This command creates a storage account credential.</span></span>
<span data-ttu-id="00b4f-126">Następnie polecenie przekazuje to poświadczenie do polecenia cmdlet **New-AzureStorSimpleDeviceVolumeContainer** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="00b4f-126">The command then passes that credential to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="00b4f-127">To polecenie cmdlet tworzy nowy kontener woluminu przy użyciu poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="00b4f-127">That cmdlet creates a new volume container by using the credential.</span></span>

## <span data-ttu-id="00b4f-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00b4f-128">PARAMETERS</span></span>

### <span data-ttu-id="00b4f-129">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="00b4f-129">-Endpoint</span></span>
<span data-ttu-id="00b4f-130">Określa punkt końcowy usługi Azure Storage dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-130">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="00b4f-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="00b4f-131">-Profile</span></span>
<span data-ttu-id="00b4f-132">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00b4f-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="00b4f-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="00b4f-133">-StorageAccountKey</span></span>
<span data-ttu-id="00b4f-134">Określa klucz dostępu konta magazynu w postaci zwykłego tekstu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-134">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b4f-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="00b4f-135">-StorageAccountName</span></span>
<span data-ttu-id="00b4f-136">Określa nazwę istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="00b4f-136">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="00b4f-137">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="00b4f-137">-UseSSL</span></span>
<span data-ttu-id="00b4f-138">Wskazuje, czy przy użyciu nowego poświadczenia konta magazynu ma być używane połączenie SSL.</span><span class="sxs-lookup"><span data-stu-id="00b4f-138">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

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

### <span data-ttu-id="00b4f-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="00b4f-139">-WaitForComplete</span></span>
<span data-ttu-id="00b4f-140">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="00b4f-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="00b4f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b4f-141">CommonParameters</span></span>
<span data-ttu-id="00b4f-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b4f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b4f-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b4f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b4f-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00b4f-144">INPUTS</span></span>

### <span data-ttu-id="00b4f-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="00b4f-145">None</span></span>

## <span data-ttu-id="00b4f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00b4f-146">OUTPUTS</span></span>

### <span data-ttu-id="00b4f-147">Interfejs IEnumerable \<StorageAccountCredentialResponse\> , TaskResponse</span><span class="sxs-lookup"><span data-stu-id="00b4f-147">IEnumerable\<StorageAccountCredentialResponse\>, TaskResponse</span></span>
<span data-ttu-id="00b4f-148">To polecenie cmdlet zwraca listę obiektów **StorageAccountCredentialResponse** , jeśli określono parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="00b4f-148">This cmdlet returns a list of **StorageAccountCredentialResponse** objects, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="00b4f-149">Jeśli nie określisz tego parametru, polecenie cmdlet zwróci obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="00b4f-149">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="00b4f-150">**StorageAccountCredentialResponse** zawiera następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="00b4f-150">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="00b4f-151">Nr **chmury** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-151">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="00b4f-152">**Nazwa_hosta** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-152">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="00b4f-153">**InstanceId** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-153">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="00b4f-154">**IsDefault** ( **wartość logiczna** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-154">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="00b4f-155">**Lokalizacja** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-155">**Location** ( **String** )</span></span>
- <span data-ttu-id="00b4f-156">**Login** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-156">**Login** ( **String** )</span></span>
- <span data-ttu-id="00b4f-157">**Name** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-157">**Name** ( **String** )</span></span>
- <span data-ttu-id="00b4f-158">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-158">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="00b4f-159">**Hasło** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-159">**Password** ( **String** )</span></span>
- <span data-ttu-id="00b4f-160">**PasswordEncryptionCertThumbprint** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-160">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="00b4f-161">**UseSSL** ( **wartość logiczna** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-161">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="00b4f-162">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="00b4f-162">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="00b4f-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00b4f-163">NOTES</span></span>

## <span data-ttu-id="00b4f-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00b4f-164">RELATED LINKS</span></span>

[<span data-ttu-id="00b4f-165">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="00b4f-165">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="00b4f-166">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="00b4f-166">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="00b4f-167">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="00b4f-167">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="00b4f-168">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="00b4f-168">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="00b4f-169">Nowe — AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="00b4f-169">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


