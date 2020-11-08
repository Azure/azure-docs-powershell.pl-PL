---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054486"
---
# <span data-ttu-id="0d186-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0d186-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="0d186-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d186-102">SYNOPSIS</span></span>
<span data-ttu-id="0d186-103">Tworzy kontener woluminu.</span><span class="sxs-lookup"><span data-stu-id="0d186-103">Creates a volume container.</span></span>

## <span data-ttu-id="0d186-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d186-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d186-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d186-105">DESCRIPTION</span></span>
<span data-ttu-id="0d186-106">Polecenie cmdlet **New-AzureStorSimpleDeviceVolumeContainer** tworzy kontener woluminu.</span><span class="sxs-lookup"><span data-stu-id="0d186-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="0d186-107">Musisz skojarzyć poświadczenia konta magazynu z nowym kontenerem woluminów.</span><span class="sxs-lookup"><span data-stu-id="0d186-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="0d186-108">Aby uzyskać poświadczenia konta magazynu, użyj polecenia cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="0d186-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="0d186-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d186-109">EXAMPLES</span></span>

### <span data-ttu-id="0d186-110">Przykład 1. Tworzenie kontenera</span><span class="sxs-lookup"><span data-stu-id="0d186-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="0d186-111">To polecenie pobiera poświadczenia konta magazynu dla konta o nazwie ContosoAccount przy użyciu polecenia cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="0d186-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="0d186-112">Polecenie przekazuje poświadczenia bieżącemu polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="0d186-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d186-113">To polecenie cmdlet używa poświadczenia z tego polecenia cmdlet, aby utworzyć kontener o nazwie Container08 na urządzeniu o nazwie Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="0d186-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="0d186-114">To polecenie uruchamia zadanie, a następnie zwraca obiekt **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="0d186-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="0d186-115">Aby wyświetlić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="0d186-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="0d186-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d186-116">PARAMETERS</span></span>

### <span data-ttu-id="0d186-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="0d186-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="0d186-118">Określa szybkość przepustowości w megabitach na sekundę (MB/s).</span><span class="sxs-lookup"><span data-stu-id="0d186-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d186-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0d186-119">-DeviceName</span></span>
<span data-ttu-id="0d186-120">Określa nazwę urządzenia StorSimple, na którym ma być utworzony kontener woluminu.</span><span class="sxs-lookup"><span data-stu-id="0d186-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

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

### <span data-ttu-id="0d186-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="0d186-121">-EncryptionEnabled</span></span>
<span data-ttu-id="0d186-122">Wskazuje, czy włączyć szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="0d186-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="0d186-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0d186-123">-EncryptionKey</span></span>
<span data-ttu-id="0d186-124">Określa klucz szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="0d186-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="0d186-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0d186-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="0d186-126">Określa poświadczenie jako obiekt **StorageAccountCredential** , który ma zostać skojarzony z nowym kontenerem woluminu.</span><span class="sxs-lookup"><span data-stu-id="0d186-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="0d186-127">Aby uzyskać obiekt **StorageAccountCredential** , użyj polecenia cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="0d186-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d186-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="0d186-128">-Profile</span></span>
<span data-ttu-id="0d186-129">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0d186-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0d186-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="0d186-130">-VolumeContainerName</span></span>
<span data-ttu-id="0d186-131">Określa nazwę kontenera woluminu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="0d186-131">Specifies the name of the volume container to create.</span></span>

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

### <span data-ttu-id="0d186-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0d186-132">-WaitForComplete</span></span>
<span data-ttu-id="0d186-133">Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="0d186-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0d186-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d186-134">CommonParameters</span></span>
<span data-ttu-id="0d186-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d186-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d186-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d186-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d186-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d186-137">INPUTS</span></span>

### <span data-ttu-id="0d186-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0d186-138">StorageAccountCredential</span></span>
<span data-ttu-id="0d186-139">To polecenie cmdlet akceptuje obiekt **PrimaryStorageAccountCredential** , który można skojarzyć z kontenerem woluminów.</span><span class="sxs-lookup"><span data-stu-id="0d186-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="0d186-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d186-140">OUTPUTS</span></span>

### <span data-ttu-id="0d186-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="0d186-141">TaskStatusInfo</span></span>
<span data-ttu-id="0d186-142">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="0d186-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="0d186-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d186-143">NOTES</span></span>

## <span data-ttu-id="0d186-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d186-144">RELATED LINKS</span></span>

[<span data-ttu-id="0d186-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0d186-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="0d186-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0d186-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="0d186-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0d186-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="0d186-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0d186-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


