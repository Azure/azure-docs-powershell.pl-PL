---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052112"
---
# <span data-ttu-id="1ea94-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ea94-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="1ea94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ea94-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea94-103">Tworzy konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ea94-103">Creates a Storage account.</span></span>

## <span data-ttu-id="1ea94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ea94-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ea94-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ea94-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea94-106">Polecenie cmdlet **New-AzStorageAccount** umożliwia utworzenie konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1ea94-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="1ea94-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ea94-107">EXAMPLES</span></span>

### <span data-ttu-id="1ea94-108">Przykład 1. Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1ea94-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="1ea94-109">To polecenie tworzy konto magazynu dla nazwy grupy zasobów moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ea94-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="1ea94-110">Przykład 2: Tworzenie konta magazynu obiektów BLOB przy użyciu BlobStorage i AccessTier na gorąco</span><span class="sxs-lookup"><span data-stu-id="1ea94-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="1ea94-111">To polecenie tworzy konto magazynu obiektów blob z BlobStorage i gorącą AccessTier</span><span class="sxs-lookup"><span data-stu-id="1ea94-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="1ea94-112">Przykład 3: Tworzenie konta magazynu za pomocą StorageV2, a następnie Wygeneruj i przypisz tożsamość do magazynu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea94-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="1ea94-113">To polecenie tworzy konto magazynu o rodzaju StorageV2.</span><span class="sxs-lookup"><span data-stu-id="1ea94-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="1ea94-114">Generuje także i przypisuje tożsamość, która może być używana do zarządzania kluczami kont za pośrednictwem usługi Azure Keys.</span><span class="sxs-lookup"><span data-stu-id="1ea94-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="1ea94-115">Przykład 4: Tworzenie konta magazynu przy użyciu NetworkRuleSet z notacji JSON</span><span class="sxs-lookup"><span data-stu-id="1ea94-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="1ea94-116">To polecenie tworzy konto magazynu z właściwością NetworkRuleSet w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="1ea94-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="1ea94-117">Przykład 5: Tworzenie konta magazynu z włączoną hierarchiczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="1ea94-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="1ea94-118">To polecenie tworzy konto magazynu z włączoną hierarchiczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="1ea94-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="1ea94-119">Przykład 6: Tworzenie konta magazynu za pomocą uwierzytelniania usług domenowych w usłudze Azure w usłudze Microsoft Files i włączanie dużego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="1ea94-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="1ea94-120">To polecenie tworzy konto magazynu z uwierzytelnianiem usługi Azure Files w usłudze Azure i umożliwia włączenie dużego udziału plików..</span><span class="sxs-lookup"><span data-stu-id="1ea94-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="1ea94-121">Przykład 8: Tworzenie konta magazynu za pomocą usługi kolejkowania i tabeli Użyj klucza szyfrowania z zakresem kont.</span><span class="sxs-lookup"><span data-stu-id="1ea94-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="1ea94-122">To polecenie tworzy konto magazynu z usługą kolejkowania i tabel, korzystając z klucza szyfrowania z zakresem kont, a więc kolejki i tabele będą używać tego samego klucza szyfrowania z obiektem BLOB i usługą plików.</span><span class="sxs-lookup"><span data-stu-id="1ea94-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="1ea94-123">Następnie uzyskasz właściwości konta magazynu i wyświetlenie klucza szyfrowania dla kolejki i usługi Table.</span><span class="sxs-lookup"><span data-stu-id="1ea94-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="1ea94-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ea94-124">PARAMETERS</span></span>

### <span data-ttu-id="1ea94-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="1ea94-125">-AccessTier</span></span>
<span data-ttu-id="1ea94-126">Określa warstwę dostępu konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea94-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1ea94-127">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="1ea94-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="1ea94-128">W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="1ea94-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="1ea94-129">Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="1ea94-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ea94-130">-AsJob</span></span>
<span data-ttu-id="1ea94-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1ea94-131">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1ea94-132">-AssignIdentity</span></span>
<span data-ttu-id="1ea94-133">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea94-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="1ea94-134">-CustomDomainName</span></span>
<span data-ttu-id="1ea94-135">Określa nazwę domeny niestandardowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ea94-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="1ea94-136">Wartość domyślna to Storage.</span><span class="sxs-lookup"><span data-stu-id="1ea94-136">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea94-137">-DefaultProfile</span></span>
<span data-ttu-id="1ea94-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea94-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="1ea94-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="1ea94-140">Włącz uwierzytelnianie usługi domenowe Active Directory Azure na platformie Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ea94-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="1ea94-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="1ea94-142">Wskazuje, czy konto magazynu umożliwia włączenie hierarchicznego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="1ea94-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="1ea94-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="1ea94-144">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="1ea94-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="1ea94-146">Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o wydajności większej niż 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="1ea94-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="1ea94-147">Po włączeniu konta nie można wyłączyć funkcji.</span><span class="sxs-lookup"><span data-stu-id="1ea94-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="1ea94-148">Obecnie obsługiwane tylko dla typów replikacji LRS i ZRS, dzięki czemu konwersje kont na konta z nadmiarowością geograficzną nie będą możliwe.</span><span class="sxs-lookup"><span data-stu-id="1ea94-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="1ea94-149">Więcej informacji https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="1ea94-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="1ea94-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="1ea94-151">Ustawianie klucza szyfrowania dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="1ea94-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="1ea94-152">Wartość domyślna to usługa.</span><span class="sxs-lookup"><span data-stu-id="1ea94-152">The default value is Service.</span></span>
<span data-ttu-id="1ea94-153">— Konto: Kolejka zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresem kont.</span><span class="sxs-lookup"><span data-stu-id="1ea94-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="1ea94-154">-Service: kolejka będzie zawsze szyfrowana za pomocą kluczy Service-Managed.</span><span class="sxs-lookup"><span data-stu-id="1ea94-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="1ea94-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="1ea94-156">Ustawianie klucza szyfrowania dla tabeli.</span><span class="sxs-lookup"><span data-stu-id="1ea94-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="1ea94-157">Wartość domyślna to usługa.</span><span class="sxs-lookup"><span data-stu-id="1ea94-157">The default value is Service.</span></span>
- <span data-ttu-id="1ea94-158">Konto: tabela zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresem kont.</span><span class="sxs-lookup"><span data-stu-id="1ea94-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="1ea94-159">Usługa: tabela zawsze będzie szyfrowana przy użyciu kluczy Service-Managed.</span><span class="sxs-lookup"><span data-stu-id="1ea94-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-160">-Kind</span><span class="sxs-lookup"><span data-stu-id="1ea94-160">-Kind</span></span>
<span data-ttu-id="1ea94-161">Określa rodzaj konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea94-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1ea94-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1ea94-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ea94-163">Chowan.</span><span class="sxs-lookup"><span data-stu-id="1ea94-163">Storage.</span></span> <span data-ttu-id="1ea94-164">Ogólne konto magazynu, które obsługuje przechowywanie obiektów blob, tabel, kolejek, plików i dysków.</span><span class="sxs-lookup"><span data-stu-id="1ea94-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="1ea94-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="1ea94-165">StorageV2.</span></span> <span data-ttu-id="1ea94-166">Konto magazynu ogólnego celu w wersji 2 (GPv2), które obsługuje obiekty blob, tabele, kolejki, pliki i dyski, z zaawansowanymi funkcjami, takimi jak warstwy danych.</span><span class="sxs-lookup"><span data-stu-id="1ea94-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="1ea94-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="1ea94-167">BlobStorage.</span></span> <span data-ttu-id="1ea94-168">Konto magazynu obiektów BLOB obsługujące tylko przechowywanie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1ea94-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="1ea94-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="1ea94-169">BlockBlobStorage.</span></span> <span data-ttu-id="1ea94-170">Blokuj konto magazynu obiektów blob, które obsługuje tylko przechowywanie bloków bloków BLOB.</span><span class="sxs-lookup"><span data-stu-id="1ea94-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="1ea94-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="1ea94-171">FileStorage.</span></span> <span data-ttu-id="1ea94-172">Konto magazynu plików obsługujące tylko przechowywanie plików.</span><span class="sxs-lookup"><span data-stu-id="1ea94-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="1ea94-173">Wartość domyślna to StorageV2.</span><span class="sxs-lookup"><span data-stu-id="1ea94-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-174">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1ea94-174">-Location</span></span>
<span data-ttu-id="1ea94-175">Określa lokalizację konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="1ea94-175">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-176">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ea94-176">-Name</span></span>
<span data-ttu-id="1ea94-177">Określa nazwę konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="1ea94-177">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ea94-178">-NetworkRuleSet</span></span>
<span data-ttu-id="1ea94-179">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do ustawiania wartości właściwości sieci, takich jak usługi, które mogą pomijać reguły, oraz sposobu obsługi żądań niezgodnych z żadną określoną regułą.</span><span class="sxs-lookup"><span data-stu-id="1ea94-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea94-180">-ResourceGroupName</span></span>
<span data-ttu-id="1ea94-181">Określa nazwę grupy zasobów, w której ma zostać dodane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ea94-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1ea94-182">-SkuName</span></span>
<span data-ttu-id="1ea94-183">Określa nazwę SKU konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea94-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1ea94-184">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1ea94-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ea94-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-185">Standard_LRS.</span></span> <span data-ttu-id="1ea94-186">Magazyn lokalny-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="1ea94-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="1ea94-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-187">Standard_ZRS.</span></span> <span data-ttu-id="1ea94-188">Miejsce do magazynowania nadmiarowych stref.</span><span class="sxs-lookup"><span data-stu-id="1ea94-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="1ea94-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-189">Standard_GRS.</span></span> <span data-ttu-id="1ea94-190">Magazyn Geograficznie nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="1ea94-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="1ea94-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-191">Standard_RAGRS.</span></span> <span data-ttu-id="1ea94-192">Dostęp do odczytu geograficznie zapasowego miejsca.</span><span class="sxs-lookup"><span data-stu-id="1ea94-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="1ea94-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-193">Premium_LRS.</span></span> <span data-ttu-id="1ea94-194">Premium miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1ea94-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="1ea94-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="1ea94-195">Premium_ZRS.</span></span> <span data-ttu-id="1ea94-196">Strefa Premium-nadmiarowe miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1ea94-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="1ea94-197">Standard_GZRS-nadmiarowe miejsce w strefie geograficznej.</span><span class="sxs-lookup"><span data-stu-id="1ea94-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="1ea94-198">Standard_RAGZRS — dostęp do odczytu Geograficznie nadmiarowy obszar magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ea94-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-199">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ea94-199">-Tag</span></span>
<span data-ttu-id="1ea94-200">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="1ea94-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="1ea94-201">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1ea94-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="1ea94-202">-UseSubDomain</span></span>
<span data-ttu-id="1ea94-203">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="1ea94-203">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea94-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea94-204">CommonParameters</span></span>
<span data-ttu-id="1ea94-205">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea94-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea94-206">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ea94-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea94-207">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ea94-207">INPUTS</span></span>

### <span data-ttu-id="1ea94-208">System. String</span><span class="sxs-lookup"><span data-stu-id="1ea94-208">System.String</span></span>

## <span data-ttu-id="1ea94-209">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ea94-209">OUTPUTS</span></span>

### <span data-ttu-id="1ea94-210">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ea94-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1ea94-211">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ea94-211">NOTES</span></span>

## <span data-ttu-id="1ea94-212">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ea94-212">RELATED LINKS</span></span>

[<span data-ttu-id="1ea94-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ea94-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="1ea94-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ea94-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="1ea94-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ea94-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
