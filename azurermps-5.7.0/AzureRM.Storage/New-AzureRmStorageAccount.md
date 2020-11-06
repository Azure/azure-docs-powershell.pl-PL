---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551475"
---
# <span data-ttu-id="cf4c0-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf4c0-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="cf4c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4c0-103">Tworzy konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf4c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf4c0-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf4c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="cf4c0-106">Polecenie cmdlet **New-AzureRmStorageAccount** umożliwia utworzenie konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="cf4c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf4c0-107">EXAMPLES</span></span>

### <span data-ttu-id="cf4c0-108">Przykład 1. Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cf4c0-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="cf4c0-109">To polecenie tworzy konto magazynu dla nazwy grupy zasobów moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="cf4c0-110">Przykład 2: Tworzenie konta magazynu obiektów BLOB używającego szyfrowania usługi magazynu</span><span class="sxs-lookup"><span data-stu-id="cf4c0-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="cf4c0-111">To polecenie tworzy konto magazynu obiektów BLOB korzystające z typu hot Access.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="cf4c0-112">Konto ma włączone szyfrowanie usługi magazynowania w usłudze BLOB.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="cf4c0-113">Przykład 3: Tworzenie konta magazynu, które umożliwia szyfrowanie usługi magazynu w przypadku obiektów blob i usług plików oraz wygenerowanie i przypisanie tożsamości dla magazynu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="cf4c0-114">To polecenie tworzy konto magazynu z włączonym szyfrowaniem usługi magazynu w przypadku obiektów blob i usług plików.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="cf4c0-115">Generuje także i przypisuje tożsamość, która może być używana do zarządzania kluczami kont za pośrednictwem usługi Azure Keys.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="cf4c0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf4c0-116">PARAMETERS</span></span>

### <span data-ttu-id="cf4c0-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="cf4c0-117">-AccessTier</span></span>
<span data-ttu-id="cf4c0-118">Określa warstwę dostępu konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="cf4c0-119">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="cf4c0-120">W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="cf4c0-121">Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cf4c0-122">-AssignIdentity</span></span>
<span data-ttu-id="cf4c0-123">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="cf4c0-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="cf4c0-124">-CustomDomainName</span></span>
<span data-ttu-id="cf4c0-125">Określa nazwę domeny niestandardowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="cf4c0-126">Wartość domyślna to Storage.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="cf4c0-127">-EnableEncryptionService</span></span>
<span data-ttu-id="cf4c0-128">Wskazuje, czy to polecenie cmdlet umożliwia szyfrowanie usługi magazynu w usłudze magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="cf4c0-129">Usługa Azure BLOB i usługi Azure File Services są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="cf4c0-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="cf4c0-131">Wskazuje, czy konto magazynu umożliwia tylko ruch https.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cf4c0-132">-InformationAction</span></span>
<span data-ttu-id="cf4c0-133">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cf4c0-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cf4c0-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf4c0-135">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="cf4c0-135">Continue</span></span>
- <span data-ttu-id="cf4c0-136">Ignorować</span><span class="sxs-lookup"><span data-stu-id="cf4c0-136">Ignore</span></span>
- <span data-ttu-id="cf4c0-137">Inquire</span><span class="sxs-lookup"><span data-stu-id="cf4c0-137">Inquire</span></span>
- <span data-ttu-id="cf4c0-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cf4c0-138">SilentlyContinue</span></span>
- <span data-ttu-id="cf4c0-139">Przestaw</span><span class="sxs-lookup"><span data-stu-id="cf4c0-139">Stop</span></span>
- <span data-ttu-id="cf4c0-140">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="cf4c0-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cf4c0-141">-InformationVariable</span></span>
<span data-ttu-id="cf4c0-142">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-143">-Kind</span><span class="sxs-lookup"><span data-stu-id="cf4c0-143">-Kind</span></span>
<span data-ttu-id="cf4c0-144">Określa rodzaj konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="cf4c0-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cf4c0-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf4c0-146">Chowan.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-146">Storage.</span></span>
<span data-ttu-id="cf4c0-147">Ogólne konto magazynu, które obsługuje przechowywanie obiektów blob, tabel, kolejek, plików i dysków.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="cf4c0-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-148">BlobStorage.</span></span>
<span data-ttu-id="cf4c0-149">Konto magazynu obiektów BLOB obsługujące tylko przechowywanie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="cf4c0-150">Wartość domyślna to Storage.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-151">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cf4c0-151">-Location</span></span>
<span data-ttu-id="cf4c0-152">Określa lokalizację konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-153">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf4c0-153">-Name</span></span>
<span data-ttu-id="cf4c0-154">Określa nazwę konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4c0-155">-ResourceGroupName</span></span>
<span data-ttu-id="cf4c0-156">Określa nazwę grupy zasobów, w której ma zostać dodane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-157">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cf4c0-157">-SkuName</span></span>
<span data-ttu-id="cf4c0-158">Określa nazwę SKU konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="cf4c0-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cf4c0-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf4c0-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-160">Standard_LRS.</span></span>
<span data-ttu-id="cf4c0-161">Magazyn lokalny-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="cf4c0-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-162">Standard_ZRS.</span></span>
<span data-ttu-id="cf4c0-163">Miejsce do magazynowania nadmiarowych stref.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="cf4c0-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-164">Standard_GRS.</span></span>
<span data-ttu-id="cf4c0-165">Magazyn Geograficznie nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="cf4c0-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-166">Standard_RAGRS.</span></span>
<span data-ttu-id="cf4c0-167">Dostęp do odczytu geograficznie zapasowego miejsca.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="cf4c0-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-168">Premium_LRS.</span></span>
<span data-ttu-id="cf4c0-169">Premium miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf4c0-170">-Tag</span></span>
<span data-ttu-id="cf4c0-171">W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="cf4c0-172">Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-173">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="cf4c0-173">-UseSubDomain</span></span>
<span data-ttu-id="cf4c0-174">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4c0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4c0-175">CommonParameters</span></span>
<span data-ttu-id="cf4c0-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4c0-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4c0-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf4c0-178">INPUTS</span></span>

### <span data-ttu-id="cf4c0-179">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cf4c0-179">None</span></span>
<span data-ttu-id="cf4c0-180">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf4c0-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf4c0-181">OUTPUTS</span></span>

## <span data-ttu-id="cf4c0-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf4c0-182">NOTES</span></span>

## <span data-ttu-id="cf4c0-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf4c0-183">RELATED LINKS</span></span>

[<span data-ttu-id="cf4c0-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf4c0-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="cf4c0-185">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf4c0-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="cf4c0-186">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf4c0-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
