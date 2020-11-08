---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054483"
---
# <span data-ttu-id="45a2b-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="45a2b-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="45a2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="45a2b-103">Tworzy poświadczenia konta magazynu wewnętrznego.</span><span class="sxs-lookup"><span data-stu-id="45a2b-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="45a2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45a2b-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45a2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="45a2b-106">Polecenie cmdlet **New-AzureStorSimpleInlineStorageAccountCredential** tworzy obiekt wbudowanego poświadczenia konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="45a2b-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="45a2b-107">To polecenie cmdlet powoduje utworzenie fikcyjnego obiektu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="45a2b-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="45a2b-108">Polecenia cmdlet **New-AzureStorSimpleDeviceVolumeContainer** i bieżącego polecenia cmdlet można używać w tym samym poleceniu, korzystając z rurociągu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45a2b-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="45a2b-109">Bieżący obiekt poświadczenia konta magazynu jest tworzony w ramach tworzenia kontenera woluminów.</span><span class="sxs-lookup"><span data-stu-id="45a2b-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="45a2b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45a2b-110">EXAMPLES</span></span>

### <span data-ttu-id="45a2b-111">Przykład 1: Tworzenie poświadczenia konta magazynu w tekście</span><span class="sxs-lookup"><span data-stu-id="45a2b-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="45a2b-112">To polecenie powoduje utworzenie wbudowanego poświadczenia konta magazynu, a następnie przekazanie go do polecenia cmdlet **New-AzureStorSimpleDeviceVolumeContainer** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="45a2b-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="45a2b-113">Ten kontener używa fikcyjnego poświadczenia do tworzenia kontenera woluminów.</span><span class="sxs-lookup"><span data-stu-id="45a2b-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="45a2b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45a2b-114">PARAMETERS</span></span>

### <span data-ttu-id="45a2b-115">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="45a2b-115">-Endpoint</span></span>
<span data-ttu-id="45a2b-116">Określa punkt końcowy usługi Azure Storage dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="45a2b-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="45a2b-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="45a2b-117">-Profile</span></span>
<span data-ttu-id="45a2b-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a2b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45a2b-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="45a2b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45a2b-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="45a2b-120">-StorageAccountKey</span></span>
<span data-ttu-id="45a2b-121">Określa klucz konta magazynu w postaci zwykłego tekstu.</span><span class="sxs-lookup"><span data-stu-id="45a2b-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="45a2b-122">Klucz jest przenoszony w formacie zaszyfrowanym.</span><span class="sxs-lookup"><span data-stu-id="45a2b-122">The key is transferred in encrypted format.</span></span>

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

### <span data-ttu-id="45a2b-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="45a2b-123">-StorageAccountName</span></span>
<span data-ttu-id="45a2b-124">Określa nazwę istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="45a2b-124">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="45a2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a2b-125">CommonParameters</span></span>
<span data-ttu-id="45a2b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a2b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a2b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a2b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45a2b-128">INPUTS</span></span>

### <span data-ttu-id="45a2b-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="45a2b-129">None</span></span>

## <span data-ttu-id="45a2b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45a2b-130">OUTPUTS</span></span>

### <span data-ttu-id="45a2b-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="45a2b-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="45a2b-132">To polecenie cmdlet zwraca obiekt **cloudtype** , który zawiera następujące pola:</span><span class="sxs-lookup"><span data-stu-id="45a2b-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="45a2b-133">**Nazwa_hosta**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-133">**Hostname**.</span></span>
<span data-ttu-id="45a2b-134">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-134">**String**.</span></span> 
- <span data-ttu-id="45a2b-135">**Identyfikator InstanceId**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-135">**InstanceId**.</span></span>
<span data-ttu-id="45a2b-136">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-136">**String**.</span></span> 
- <span data-ttu-id="45a2b-137">**Wartość domyślna**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-137">**IsDefault**.</span></span>
<span data-ttu-id="45a2b-138">**Wartość logiczna**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-138">**Boolean**.</span></span> 
- <span data-ttu-id="45a2b-139">**Lokalizację**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-139">**Location**.</span></span>
<span data-ttu-id="45a2b-140">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-140">**String**.</span></span> 
- <span data-ttu-id="45a2b-141">**Login (logowanie** ).</span><span class="sxs-lookup"><span data-stu-id="45a2b-141">**Login**.</span></span>
<span data-ttu-id="45a2b-142">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-142">**String**.</span></span> 
- <span data-ttu-id="45a2b-143">**Name (nazwa** ).</span><span class="sxs-lookup"><span data-stu-id="45a2b-143">**Name**.</span></span>
<span data-ttu-id="45a2b-144">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-144">**String**.</span></span> 
- <span data-ttu-id="45a2b-145">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-145">**OperationInProgress**.</span></span>
<span data-ttu-id="45a2b-146">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="45a2b-147">**Password (hasło** ).</span><span class="sxs-lookup"><span data-stu-id="45a2b-147">**Password**.</span></span>
<span data-ttu-id="45a2b-148">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-148">**String**.</span></span> 
- <span data-ttu-id="45a2b-149">**PasswordEncryptionCertThumbprint**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="45a2b-150">**String**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-150">**String**.</span></span> 
- <span data-ttu-id="45a2b-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-151">**UseSSL**.</span></span>
<span data-ttu-id="45a2b-152">**Wartość logiczna**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-152">**Boolean**.</span></span> 
- <span data-ttu-id="45a2b-153">**VolumeCount**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-153">**VolumeCount**.</span></span>
<span data-ttu-id="45a2b-154">**Liczba całkowita**.</span><span class="sxs-lookup"><span data-stu-id="45a2b-154">**Integer**.</span></span>

## <span data-ttu-id="45a2b-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45a2b-155">NOTES</span></span>

## <span data-ttu-id="45a2b-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45a2b-156">RELATED LINKS</span></span>

[<span data-ttu-id="45a2b-157">Nowe — AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="45a2b-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="45a2b-158">Nowe — AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="45a2b-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


