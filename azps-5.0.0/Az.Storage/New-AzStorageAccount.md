---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231659"
---
# <span data-ttu-id="d2dc0-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2dc0-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="d2dc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2dc0-103">Tworzy konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-103">Creates a Storage account.</span></span>

## <span data-ttu-id="d2dc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2dc0-104">SYNTAX</span></span>

### <span data-ttu-id="d2dc0-105">AzureActiveDirectoryDomainServicesForFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d2dc0-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2dc0-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d2dc0-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2dc0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d2dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="d2dc0-108">Polecenie cmdlet **New-AzStorageAccount** umożliwia utworzenie konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="d2dc0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2dc0-109">EXAMPLES</span></span>

### <span data-ttu-id="d2dc0-110">Przykład 1. Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d2dc0-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="d2dc0-111">To polecenie tworzy konto magazynu dla nazwy grupy zasobów moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="d2dc0-112">Przykład 2: Tworzenie konta magazynu obiektów BLOB przy użyciu BlobStorage i AccessTier na gorąco</span><span class="sxs-lookup"><span data-stu-id="d2dc0-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="d2dc0-113">To polecenie tworzy konto magazynu obiektów blob z BlobStorage i gorącą AccessTier</span><span class="sxs-lookup"><span data-stu-id="d2dc0-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="d2dc0-114">Przykład 3: Tworzenie konta magazynu za pomocą StorageV2, a następnie Wygeneruj i przypisz tożsamość do magazynu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="d2dc0-115">To polecenie tworzy konto magazynu o rodzaju StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="d2dc0-116">Generuje także i przypisuje tożsamość, która może być używana do zarządzania kluczami kont za pośrednictwem usługi Azure Keys.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="d2dc0-117">Przykład 4: Tworzenie konta magazynu przy użyciu NetworkRuleSet z notacji JSON</span><span class="sxs-lookup"><span data-stu-id="d2dc0-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="d2dc0-118">To polecenie tworzy konto magazynu z właściwością NetworkRuleSet w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="d2dc0-119">Przykład 5: Tworzenie konta magazynu z włączoną hierarchiczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="d2dc0-120">To polecenie tworzy konto magazynu z włączoną hierarchiczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="d2dc0-121">Przykład 6: Tworzenie konta magazynu za pomocą uwierzytelniania usług domenowych w usłudze Azure w usłudze Microsoft Files i włączanie dużego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="d2dc0-122">To polecenie tworzy konto magazynu z uwierzytelnianiem usługi Azure fileing przy użyciu uwierzytelniania usługi DS i umożliwia włączenie dużego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="d2dc0-123">Przykład 7: Tworzenie konta magazynu z uwierzytelnianiem usługi domenowe Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="d2dc0-124">To polecenie tworzy konto magazynu z plikami withenable uwierzytelnianie usługi Domain Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="d2dc0-125">Przykład 8: Tworzenie konta magazynu za pomocą usługi kolejkowania i tabeli Użyj klucza szyfrowania z zakresem kont i Wymagaj szyfrowania infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="d2dc0-126">To polecenie tworzy konto magazynu z usługą kolejkowania i tabel, korzystając z klucza szyfrowania z zakresem kont i wymaga szyfrowania infrastruktury, więc w kolejce i tabeli będzie używany ten sam klucz szyfrowania z użyciem obiektu BLOB i usługi plików, a usługa będzie stosować pomocniczą warstwę szyfrowania z kluczami zarządzanymi przez platformę dla danych w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="d2dc0-127">Następnie uzyskasz właściwości konta magazynu i wyświetlenie klucza szyfrowania usługi kolejkowania i tabel oraz wartości RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="d2dc0-128">Przykład 9: Tworzenie konta MinimumTlsVersion i AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="d2dc0-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="d2dc0-129">Polecenie Utwórz konto z MinimumTlsVersion i AllowBlobPublicAccess, a następnie Pokaż 2 właściwości utworzonego konta.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="d2dc0-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2dc0-130">PARAMETERS</span></span>

### <span data-ttu-id="d2dc0-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="d2dc0-131">-AccessTier</span></span>
<span data-ttu-id="d2dc0-132">Określa warstwę dostępu konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d2dc0-133">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="d2dc0-134">W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="d2dc0-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="d2dc0-135">Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="d2dc0-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="d2dc0-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="d2dc0-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="d2dc0-137">Określa identyfikator zabezpieczeń (SID) usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="d2dc0-138">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="d2dc0-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="d2dc0-140">Określa identyfikator GUID domeny.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-140">Specifies the domain GUID.</span></span> <span data-ttu-id="d2dc0-141">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="d2dc0-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="d2dc0-143">Określa podstawową domenę, dla której serwer DNS usługi AD jest autorytatywny.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="d2dc0-144">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="d2dc0-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="d2dc0-146">Określa identyfikator zabezpieczeń (SID).</span><span class="sxs-lookup"><span data-stu-id="d2dc0-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="d2dc0-147">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="d2dc0-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="d2dc0-149">Określa Las usługi Active Directory do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="d2dc0-150">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="d2dc0-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="d2dc0-152">Określa nazwę domeny NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="d2dc0-153">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="d2dc0-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="d2dc0-155">Zezwalaj na dostęp publiczny do wszystkich obiektów blob lub kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="d2dc0-156">Dla tej właściwości domyślna interpretacja to prawda.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="d2dc0-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2dc0-157">-AsJob</span></span>
<span data-ttu-id="d2dc0-158">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2dc0-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2dc0-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d2dc0-159">-AssignIdentity</span></span>
<span data-ttu-id="d2dc0-160">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d2dc0-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d2dc0-161">-CustomDomainName</span></span>
<span data-ttu-id="d2dc0-162">Określa nazwę domeny niestandardowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="d2dc0-163">Wartość domyślna to Storage.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="d2dc0-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2dc0-164">-DefaultProfile</span></span>
<span data-ttu-id="d2dc0-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2dc0-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d2dc0-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="d2dc0-167">Włącz uwierzytelnianie usługi domenowe Active Directory na platformie Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d2dc0-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="d2dc0-169">Włącz uwierzytelnianie usługi domenowe Active Directory Azure na platformie Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="d2dc0-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="d2dc0-171">Wskazuje, czy konto magazynu umożliwia włączenie hierarchicznego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="d2dc0-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="d2dc0-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="d2dc0-173">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="d2dc0-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="d2dc0-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="d2dc0-175">Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o wydajności większej niż 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="d2dc0-176">Po włączeniu konta nie można wyłączyć funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="d2dc0-177">Obecnie obsługiwane tylko dla typów replikacji LRS i ZRS, dzięki czemu konwersje kont na konta z nadmiarowością geograficzną nie będą możliwe.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="d2dc0-178">Więcej informacji https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="d2dc0-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="d2dc0-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="d2dc0-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="d2dc0-180">Ustawianie klucza szyfrowania dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="d2dc0-181">Wartość domyślna to usługa.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-181">The default value is Service.</span></span>
<span data-ttu-id="d2dc0-182">— Konto: Kolejka zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresem kont.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="d2dc0-183">-Service: kolejka będzie zawsze szyfrowana za pomocą kluczy Service-Managed.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="d2dc0-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="d2dc0-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="d2dc0-185">Ustawianie klucza szyfrowania dla tabeli.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="d2dc0-186">Wartość domyślna to usługa.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-186">The default value is Service.</span></span>
- <span data-ttu-id="d2dc0-187">Konto: tabela zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresem kont.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="d2dc0-188">Usługa: tabela zawsze będzie szyfrowana przy użyciu kluczy Service-Managed.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="d2dc0-189">-Kind</span><span class="sxs-lookup"><span data-stu-id="d2dc0-189">-Kind</span></span>
<span data-ttu-id="d2dc0-190">Określa rodzaj konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d2dc0-191">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2dc0-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2dc0-192">Chowan.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-192">Storage.</span></span> <span data-ttu-id="d2dc0-193">Ogólne konto magazynu, które obsługuje przechowywanie obiektów blob, tabel, kolejek, plików i dysków.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="d2dc0-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-194">StorageV2.</span></span> <span data-ttu-id="d2dc0-195">Konto magazynu ogólnego celu w wersji 2 (GPv2), które obsługuje obiekty blob, tabele, kolejki, pliki i dyski, z zaawansowanymi funkcjami, takimi jak warstwy danych.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="d2dc0-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-196">BlobStorage.</span></span> <span data-ttu-id="d2dc0-197">Konto magazynu obiektów BLOB obsługujące tylko przechowywanie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="d2dc0-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-198">BlockBlobStorage.</span></span> <span data-ttu-id="d2dc0-199">Blokuj konto magazynu obiektów blob, które obsługuje tylko przechowywanie bloków bloków BLOB.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="d2dc0-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-200">FileStorage.</span></span> <span data-ttu-id="d2dc0-201">Konto magazynu plików obsługujące tylko przechowywanie plików.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="d2dc0-202">Wartość domyślna to StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-202">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-203">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d2dc0-203">-Location</span></span>
<span data-ttu-id="d2dc0-204">Określa lokalizację konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="d2dc0-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d2dc0-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="d2dc0-206">Minimalna wersja protokołu TLS, która ma być dozwolona na żądaniach magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="d2dc0-207">Domyślna interpretacja to TLS 1,0 dla tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-207">The default interpretation is TLS 1.0 for this property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc0-208">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2dc0-208">-Name</span></span>
<span data-ttu-id="d2dc0-209">Określa nazwę konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="d2dc0-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2dc0-210">-NetworkRuleSet</span></span>
<span data-ttu-id="d2dc0-211">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do ustawiania wartości właściwości sieci, takich jak usługi, które mogą pomijać reguły, oraz sposobu obsługi żądań niezgodnych z żadną określoną regułą.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="d2dc0-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="d2dc0-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="d2dc0-213">Usługa zastosuje pomocniczą warstwę szyfrowania z kluczami zarządzanymi przez platformę dla danych w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="d2dc0-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2dc0-214">-ResourceGroupName</span></span>
<span data-ttu-id="d2dc0-215">Określa nazwę grupy zasobów, w której ma zostać dodane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="d2dc0-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d2dc0-216">-SkuName</span></span>
<span data-ttu-id="d2dc0-217">Określa nazwę SKU konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d2dc0-218">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2dc0-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2dc0-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-219">Standard_LRS.</span></span> <span data-ttu-id="d2dc0-220">Magazyn lokalny-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-221">Standard_ZRS.</span></span> <span data-ttu-id="d2dc0-222">Miejsce do magazynowania nadmiarowych stref.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-223">Standard_GRS.</span></span> <span data-ttu-id="d2dc0-224">Magazyn Geograficznie nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-225">Standard_RAGRS.</span></span> <span data-ttu-id="d2dc0-226">Dostęp do odczytu geograficznie zapasowego miejsca.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-227">Premium_LRS.</span></span> <span data-ttu-id="d2dc0-228">Premium miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-229">Premium_ZRS.</span></span> <span data-ttu-id="d2dc0-230">Strefa Premium-nadmiarowe miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-231">Standard_GZRS-nadmiarowe miejsce w strefie geograficznej.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="d2dc0-232">Standard_RAGZRS — dostęp do odczytu Geograficznie nadmiarowy obszar magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="d2dc0-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2dc0-233">-Tag</span></span>
<span data-ttu-id="d2dc0-234">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="d2dc0-235">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d2dc0-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d2dc0-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="d2dc0-236">-UseSubDomain</span></span>
<span data-ttu-id="d2dc0-237">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="d2dc0-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2dc0-238">CommonParameters</span></span>
<span data-ttu-id="d2dc0-239">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2dc0-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2dc0-240">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2dc0-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2dc0-241">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2dc0-241">INPUTS</span></span>

### <span data-ttu-id="d2dc0-242">System. String</span><span class="sxs-lookup"><span data-stu-id="d2dc0-242">System.String</span></span>

## <span data-ttu-id="d2dc0-243">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2dc0-243">OUTPUTS</span></span>

### <span data-ttu-id="d2dc0-244">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2dc0-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d2dc0-245">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2dc0-245">NOTES</span></span>

## <span data-ttu-id="d2dc0-246">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2dc0-246">RELATED LINKS</span></span>

[<span data-ttu-id="d2dc0-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2dc0-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="d2dc0-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2dc0-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="d2dc0-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2dc0-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
