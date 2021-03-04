---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993203"
---
# <span data-ttu-id="330c0-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="330c0-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="330c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="330c0-102">SYNOPSIS</span></span>
<span data-ttu-id="330c0-103">Tworzy konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="330c0-103">Creates a Storage account.</span></span>

## <span data-ttu-id="330c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="330c0-104">SYNTAX</span></span>

### <span data-ttu-id="330c0-105">AzureActiveDirectoryDomainServicesForFile (domyślne)</span><span class="sxs-lookup"><span data-stu-id="330c0-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="330c0-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="330c0-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="330c0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="330c0-107">DESCRIPTION</span></span>
<span data-ttu-id="330c0-108">Polecenie **cmdlet New-AzStorageAccount** tworzy konto usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="330c0-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="330c0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="330c0-109">EXAMPLES</span></span>

### <span data-ttu-id="330c0-110">Przykład 1. Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="330c0-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="330c0-111">To polecenie tworzy konto magazynu dla nazwy grupy zasobów MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="330c0-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="330c0-112">Przykład 2. Tworzenie konta magazynu obiektów blob przy użyciu obiektów BlobStorage Kind i hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="330c0-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="330c0-113">To polecenie tworzy konto magazynu obiektów blob, które z obiektami BlobStorage Kind i hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="330c0-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="330c0-114">Przykład 3. Tworzenie konta magazynu przy użyciu urządzenia Kind StorageV2 oraz generowanie i przypisywanie tożsamości dla usługi Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="330c0-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="330c0-115">To polecenie tworzy konto magazynu z magazynem typu V2.</span><span class="sxs-lookup"><span data-stu-id="330c0-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="330c0-116">Generuje ona również i przypisuje tożsamość, za pomocą których można zarządzać kluczami kont za pośrednictwem usługi Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="330c0-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="330c0-117">Przykład 4. Tworzenie konta magazynu za pomocą zestawu NetworkRuleSet z JSON</span><span class="sxs-lookup"><span data-stu-id="330c0-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="330c0-118">To polecenie tworzy konto magazynu, które ma właściwość NetworkRuleSet z JSON</span><span class="sxs-lookup"><span data-stu-id="330c0-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="330c0-119">Przykład 5. Tworzenie konta magazynu z włączoną hierarchiczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="330c0-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="330c0-120">To polecenie tworzy konto magazynu z włączoną hierarchiczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="330c0-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="330c0-121">Przykład 6. Tworzenie konta magazynu przy użyciu usługi Azure Files AAD DS Authentication i włączanie dużego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="330c0-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="330c0-122">To polecenie umożliwia utworzenie konta magazynu z uwierzytelnianiem AAD DS plików platformy Azure i włączenie dużego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="330c0-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="330c0-123">Przykład 7. Utworzenie konta magazynu z włączym uwierzytelnianiem usługi domenowej Active Directory w plikach.</span><span class="sxs-lookup"><span data-stu-id="330c0-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="330c0-124">To polecenie powoduje utworzenie konta magazynu z możliwością uwierzytelniania usługi domenowej Active Directory z plikiami.</span><span class="sxs-lookup"><span data-stu-id="330c0-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="330c0-125">Przykład 8. Tworzenie konta magazynu przy użyciu klucza szyfrowania z zakresu konta i wymaganego szyfrowania infrastruktury przy użyciu usługi kolejki i usługi tabel.</span><span class="sxs-lookup"><span data-stu-id="330c0-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="330c0-126">To polecenie tworzy konto magazynu z kluczem szyfrowania w zakresie konta i usługą tabel i wymagać szyfrowania infrastruktury, więc kolejka i tabela będą używać tego samego klucza szyfrowania z usługą obiektów blob i plików, a usługa zastosuje pomocniczą warstwę szyfrowania z kluczami zarządzanymi platformy dla danych w spoczynku.</span><span class="sxs-lookup"><span data-stu-id="330c0-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="330c0-127">Następnie uzyskaj właściwości konta magazynu i wyświetl typ klucza szyfrowania usługi kolejki i tabeli oraz wartość RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="330c0-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="330c0-128">Przykład 9. Tworzenie konta MinimumTlsVersion i AllowBlobPublicAccess oraz wyłączanie dostępu do klucza udostępnionego</span><span class="sxs-lookup"><span data-stu-id="330c0-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="330c0-129">Polecenie utwórz konto z wartością MinimumTlsVersion, AllowBlobPublicAccess i wyłącz dostęp kluczu udostępnionego do konta, a następnie pokaż 3 właściwości utworzonego konta.</span><span class="sxs-lookup"><span data-stu-id="330c0-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="330c0-130">Przykład 10. Tworzenie konta magazynu przy użyciu ustawienia RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="330c0-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="330c0-131">To polecenie tworzy konto magazynu z ustawieniem RoutingPreference: PublishMicrosoftEndpoint i PublishInternetEndpoint jako prawda oraz RoutingChoice jako MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="330c0-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="330c0-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="330c0-132">PARAMETERS</span></span>

### <span data-ttu-id="330c0-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="330c0-133">-AccessTier</span></span>
<span data-ttu-id="330c0-134">Określa warstwę dostępu dla konta magazynu, które tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="330c0-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="330c0-135">Dopuszczalne wartości dla tego parametru to: Hot (Hot) i Cool (Cool).</span><span class="sxs-lookup"><span data-stu-id="330c0-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="330c0-136">Jeśli dla parametru *Kind* określisz wartość parametru BlobStorage, musisz określić wartość *parametru AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="330c0-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="330c0-137">W przypadku określenia wartości parametru Storage (Magazyn) dla tego *parametru nie* należy określać *parametru AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="330c0-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="330c0-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="330c0-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="330c0-139">Określa identyfikator zabezpieczeń (SID) dla magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="330c0-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="330c0-140">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="330c0-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="330c0-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="330c0-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="330c0-142">Określa identyfikator GUID domeny.</span><span class="sxs-lookup"><span data-stu-id="330c0-142">Specifies the domain GUID.</span></span> <span data-ttu-id="330c0-143">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="330c0-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="330c0-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="330c0-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="330c0-145">Określa domenę podstawową, dla których autorytatywny jest serwer DNS usługi AD.</span><span class="sxs-lookup"><span data-stu-id="330c0-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="330c0-146">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="330c0-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="330c0-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="330c0-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="330c0-148">Określa identyfikator zabezpieczeń (SID).</span><span class="sxs-lookup"><span data-stu-id="330c0-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="330c0-149">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="330c0-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="330c0-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="330c0-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="330c0-151">Określa las usługi Active Directory do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="330c0-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="330c0-152">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="330c0-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="330c0-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="330c0-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="330c0-154">Określa nazwę domeny NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="330c0-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="330c0-155">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="330c0-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="330c0-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="330c0-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="330c0-157">Zezwalaj na dostęp publiczny do wszystkich obiektów blob lub kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="330c0-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="330c0-158">Domyślna interpretacja dotyczy tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="330c0-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="330c0-159">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="330c0-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="330c0-160">Wskazuje, czy konto magazynu zezwala na autoryzację żądań dostępu do konta za pośrednictwem klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="330c0-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="330c0-161">Jeśli wartość fałsz, wszystkie żądania, w tym podpisy dostępu udostępnionego, muszą mieć autoryzację w usłudze Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="330c0-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="330c0-162">Wartość domyślna to null, która jest równoważna wartością prawda.</span><span class="sxs-lookup"><span data-stu-id="330c0-162">The default value is null, which is equivalent to true.</span></span>

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

### <span data-ttu-id="330c0-163">— AsJob</span><span class="sxs-lookup"><span data-stu-id="330c0-163">-AsJob</span></span>
<span data-ttu-id="330c0-164">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="330c0-164">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="330c0-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="330c0-165">-AssignIdentity</span></span>
<span data-ttu-id="330c0-166">Wygeneruj i przypisz nowe konto magazynu Tożsamości dla tego konta magazynu do używania z usługami zarządzania kluczami, na przykład Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="330c0-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="330c0-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="330c0-167">-CustomDomainName</span></span>
<span data-ttu-id="330c0-168">Określa nazwę domeny niestandardowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="330c0-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="330c0-169">Wartość domyślna to Magazyn.</span><span class="sxs-lookup"><span data-stu-id="330c0-169">The default value is Storage.</span></span>

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

### <span data-ttu-id="330c0-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330c0-170">-DefaultProfile</span></span>
<span data-ttu-id="330c0-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="330c0-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="330c0-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="330c0-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="330c0-173">Włącz uwierzytelnianie usługi domenowej Active Directory w plikach Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="330c0-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="330c0-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="330c0-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="330c0-175">Włącz uwierzytelnianie usługi domen usługi Azure Active Directory dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="330c0-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="330c0-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="330c0-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="330c0-177">Wskazuje, czy konto magazynu umożliwia korzystanie z hierarchicznej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="330c0-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="330c0-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="330c0-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="330c0-179">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="330c0-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="330c0-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="330c0-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="330c0-181">Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o pojemności większej niż 5 tib.</span><span class="sxs-lookup"><span data-stu-id="330c0-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="330c0-182">Po włączeniu konta nie można wyłączyć tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="330c0-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="330c0-183">Obecnie obsługiwane są tylko typy replikacji LRS i ZRS, przez co konwersja kont na geograficznie nadmiarowe konta nie będzie możliwa.</span><span class="sxs-lookup"><span data-stu-id="330c0-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="330c0-184">Dowiedz się więcej w https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="330c0-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="330c0-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="330c0-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="330c0-186">Ustaw typ klucza szyfrowania dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="330c0-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="330c0-187">Wartość domyślna to Service (Usługa).</span><span class="sxs-lookup"><span data-stu-id="330c0-187">The default value is Service.</span></span>
<span data-ttu-id="330c0-188">-Konto: Kolejka zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresu konta.</span><span class="sxs-lookup"><span data-stu-id="330c0-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="330c0-189">-Service: Kolejka zawsze będzie zaszyfrowana za pomocą Service-Managed kluczy.</span><span class="sxs-lookup"><span data-stu-id="330c0-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="330c0-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="330c0-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="330c0-191">Ustaw typ klucza szyfrowania dla tabeli.</span><span class="sxs-lookup"><span data-stu-id="330c0-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="330c0-192">Wartość domyślna to Service (Usługa).</span><span class="sxs-lookup"><span data-stu-id="330c0-192">The default value is Service.</span></span>
- <span data-ttu-id="330c0-193">Konto: Tabela zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresu konta.</span><span class="sxs-lookup"><span data-stu-id="330c0-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="330c0-194">Usługa: Tabela będzie zawsze zaszyfrowana przy Service-Managed kluczach.</span><span class="sxs-lookup"><span data-stu-id="330c0-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="330c0-195">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="330c0-195">-Kind</span></span>
<span data-ttu-id="330c0-196">Określa rodzaj konta magazynu, które tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="330c0-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="330c0-197">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="330c0-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="330c0-198">Miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="330c0-198">Storage.</span></span> <span data-ttu-id="330c0-199">Konto magazynu ogólnego przeznaczenia, które obsługuje magazyn obiektów blob, tabel, kolejek, plików i dysków.</span><span class="sxs-lookup"><span data-stu-id="330c0-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="330c0-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="330c0-200">StorageV2.</span></span> <span data-ttu-id="330c0-201">Konto magazynu ogólnego przeznaczenia w wersji 2 (GPv2), które obsługuje obiekty blob, tabele, kolejki, pliki i dyski, z zaawansowanymi funkcjami, takich jak warstwowanie danych.</span><span class="sxs-lookup"><span data-stu-id="330c0-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="330c0-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="330c0-202">BlobStorage.</span></span> <span data-ttu-id="330c0-203">Konto magazynu obiektów blob, które obsługuje tylko magazyn obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="330c0-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="330c0-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="330c0-204">BlockBlobStorage.</span></span> <span data-ttu-id="330c0-205">Blokuj konto magazynu obiektów blob, które obsługuje tylko magazyn obiektów blob blokowych.</span><span class="sxs-lookup"><span data-stu-id="330c0-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="330c0-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="330c0-206">FileStorage.</span></span> <span data-ttu-id="330c0-207">Konto magazynu plików, które obsługuje tylko przechowywanie plików.</span><span class="sxs-lookup"><span data-stu-id="330c0-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="330c0-208">Wartość domyślna to StorageV2.</span><span class="sxs-lookup"><span data-stu-id="330c0-208">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="330c0-209">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="330c0-209">-Location</span></span>
<span data-ttu-id="330c0-210">Określa lokalizację konta magazynu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="330c0-210">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="330c0-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="330c0-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="330c0-212">Minimalna wersja TLS, która jest dozwolona w żądaniach przechowywania.</span><span class="sxs-lookup"><span data-stu-id="330c0-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="330c0-213">Domyślna interpretacja tej właściwości to TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="330c0-213">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="330c0-214">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="330c0-214">-Name</span></span>
<span data-ttu-id="330c0-215">Określa nazwę konta magazynu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="330c0-215">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="330c0-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="330c0-216">-NetworkRuleSet</span></span>
<span data-ttu-id="330c0-217">Zestaw NetworkRuleSet służy do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do określania wartości właściwości sieciowych, takich jak usługi mogące pomijać reguły i sposób obsługi żądań, które nie są zgodne z żadnymi zdefiniowanymi regułami.</span><span class="sxs-lookup"><span data-stu-id="330c0-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="330c0-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="330c0-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="330c0-219">Wskazuje, czy punkty końcowe magazynu routingu internetowego mają zostać opublikowane.</span><span class="sxs-lookup"><span data-stu-id="330c0-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="330c0-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="330c0-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="330c0-221">Wskazuje, czy punkty końcowe magazynu routingu firmy Microsoft mają zostać opublikowane.</span><span class="sxs-lookup"><span data-stu-id="330c0-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="330c0-222">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="330c0-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="330c0-223">Usługa zastosuje pomocniczą warstwę szyfrowania z kluczami zarządzanymi platformy dla danych w spoczynku.</span><span class="sxs-lookup"><span data-stu-id="330c0-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="330c0-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="330c0-224">-ResourceGroupName</span></span>
<span data-ttu-id="330c0-225">Określa nazwę grupy zasobów, w której chcesz dodać konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="330c0-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="330c0-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="330c0-226">-RoutingChoice</span></span>
<span data-ttu-id="330c0-227">Wybór routingu określa rodzaj routingu sieciowego wybierany przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="330c0-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="330c0-228">Możliwe wartości: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="330c0-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="330c0-229">-SKUName</span><span class="sxs-lookup"><span data-stu-id="330c0-229">-SkuName</span></span>
<span data-ttu-id="330c0-230">Określa nazwę sKU konta magazynu, które tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="330c0-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="330c0-231">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="330c0-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="330c0-232">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="330c0-232">Standard_LRS.</span></span> <span data-ttu-id="330c0-233">Lokalnie nadmiarowa przestrzeń dyskowa.</span><span class="sxs-lookup"><span data-stu-id="330c0-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="330c0-234">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="330c0-234">Standard_ZRS.</span></span> <span data-ttu-id="330c0-235">Nadmiarowa przestrzeń dyskowa bez stref.</span><span class="sxs-lookup"><span data-stu-id="330c0-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="330c0-236">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="330c0-236">Standard_GRS.</span></span> <span data-ttu-id="330c0-237">Magazyn geograficznie nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="330c0-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="330c0-238">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="330c0-238">Standard_RAGRS.</span></span> <span data-ttu-id="330c0-239">Odczytywanie nadmiarowej geoprzesyłki dostępu.</span><span class="sxs-lookup"><span data-stu-id="330c0-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="330c0-240">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="330c0-240">Premium_LRS.</span></span> <span data-ttu-id="330c0-241">Premium lokalnie nadmiarowa przestrzeń dyskowa.</span><span class="sxs-lookup"><span data-stu-id="330c0-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="330c0-242">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="330c0-242">Premium_ZRS.</span></span> <span data-ttu-id="330c0-243">Nadmiarowa przestrzeń dyskowa premium.</span><span class="sxs-lookup"><span data-stu-id="330c0-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="330c0-244">Standard_GZRS — nadmiarowa geograficznie nadmiarowa przestrzeń dyskowa bez stref.</span><span class="sxs-lookup"><span data-stu-id="330c0-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="330c0-245">Standard_RAGZRS — odczyt nadmiarowy geograficznie nadmiarowy magazyn strefy.</span><span class="sxs-lookup"><span data-stu-id="330c0-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="330c0-246">— Tag</span><span class="sxs-lookup"><span data-stu-id="330c0-246">-Tag</span></span>
<span data-ttu-id="330c0-247">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi na serwerze.</span><span class="sxs-lookup"><span data-stu-id="330c0-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="330c0-248">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="330c0-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="330c0-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="330c0-249">-UseSubDomain</span></span>
<span data-ttu-id="330c0-250">Wskazuje, czy należy włączyć pośrednie sprawdzanie poprawności CName.</span><span class="sxs-lookup"><span data-stu-id="330c0-250">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="330c0-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330c0-251">CommonParameters</span></span>
<span data-ttu-id="330c0-252">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="330c0-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330c0-253">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="330c0-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330c0-254">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="330c0-254">INPUTS</span></span>

### <span data-ttu-id="330c0-255">System.String</span><span class="sxs-lookup"><span data-stu-id="330c0-255">System.String</span></span>

## <span data-ttu-id="330c0-256">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="330c0-256">OUTPUTS</span></span>

### <span data-ttu-id="330c0-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="330c0-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="330c0-258">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="330c0-258">NOTES</span></span>

## <span data-ttu-id="330c0-259">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="330c0-259">RELATED LINKS</span></span>

[<span data-ttu-id="330c0-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="330c0-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="330c0-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="330c0-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="330c0-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="330c0-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
