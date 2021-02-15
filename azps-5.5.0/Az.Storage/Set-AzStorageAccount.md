---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183171"
---
# <span data-ttu-id="3d6eb-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d6eb-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="3d6eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6eb-103">Modyfikuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="3d6eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d6eb-104">SYNTAX</span></span>

### <span data-ttu-id="3d6eb-105">StorageEncryption (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d6eb-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6eb-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3d6eb-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6eb-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="3d6eb-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d6eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d6eb-108">DESCRIPTION</span></span>
<span data-ttu-id="3d6eb-109">Polecenie **cmdlet Set-AzStorageAccount** modyfikuje konto usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="3d6eb-110">To polecenie cmdlet umożliwia modyfikowanie typu konta, aktualizowanie domeny klienta lub ustawianie tagów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="3d6eb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d6eb-111">EXAMPLES</span></span>

### <span data-ttu-id="3d6eb-112">Przykład 1. Ustawianie typu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3d6eb-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="3d6eb-113">To polecenie ustawia typ konta magazynu na Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="3d6eb-114">Przykład 2. Ustawianie domeny niestandardowej dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3d6eb-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="3d6eb-115">To polecenie ustawia domenę niestandardową dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="3d6eb-116">Przykład 3. Ustawianie wartości warstwy dostępu</span><span class="sxs-lookup"><span data-stu-id="3d6eb-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="3d6eb-117">To polecenie ustawia wartość warstwy programu Access na cool.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="3d6eb-118">Przykład 4. Ustawianie niestandardowej domeny i tagów</span><span class="sxs-lookup"><span data-stu-id="3d6eb-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="3d6eb-119">To polecenie ustawia niestandardową domenę i tagi dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="3d6eb-120">Przykład 5. Ustawianie źródła klucza szyfrowania na wartość Keyvault</span><span class="sxs-lookup"><span data-stu-id="3d6eb-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="3d6eb-121">To polecenie set Encryption KeySource with a new created Keyvault.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="3d6eb-122">Przykład 6. Ustawianie źródła klucza szyfrowania na wartość "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="3d6eb-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="3d6eb-123">To polecenie ustawiło źródło klucza szyfrowania na "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="3d6eb-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="3d6eb-124">Przykład 7. Ustawianie właściwości NetworkRuleSet konta magazynu przy użyciu JSON</span><span class="sxs-lookup"><span data-stu-id="3d6eb-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="3d6eb-125">To polecenie ustawia właściwość NetworkRuleSet konta magazynu z JSON</span><span class="sxs-lookup"><span data-stu-id="3d6eb-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="3d6eb-126">Przykład 8. Uzyskiwanie właściwości NetworkRuleSet z konta magazynu i ustawianie jej na inne konto magazynu</span><span class="sxs-lookup"><span data-stu-id="3d6eb-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="3d6eb-127">To pierwsze polecenie pobiera właściwość NetworkRuleSet z konta magazynu, a drugie do innego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3d6eb-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="3d6eb-128">Przykład 9. Uaktualnianie konta magazynu przy użyciu rodzaju "Magazyn" lub "BlobStorage" do konta magazynu typu "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="3d6eb-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="3d6eb-129">Polecenie uaktualnij konto magazynu za pomocą rodzaju "Magazyn" lub "BlobStorage" do konta magazynu typu "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="3d6eb-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="3d6eb-130">Przykład 10. Aktualizowanie konta magazynu przez włączenie uwierzytelniania usług Azure Files AAD DS.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="3d6eb-131">Polecenie aktualizuj konto magazynu przez włączenie uwierzytelniania usług Azure Files AAD DS.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="3d6eb-132">Przykład 11. Aktualizowanie konta magazynu przez włączenie uwierzytelniania usługi domenowej Active Directory w plikach, a następnie wyświetlanie ustawienia uwierzytelniania opartego na tożsamości plików</span><span class="sxs-lookup"><span data-stu-id="3d6eb-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="3d6eb-133">Polecenie aktualizuje konto magazynu przez włączenie uwierzytelniania usługi domenowej Active Directory w usłudze Azure Files, a następnie wyświetla ustawienie uwierzytelniania opartego na tożsamości plików</span><span class="sxs-lookup"><span data-stu-id="3d6eb-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="3d6eb-134">Przykład 12. Ustawianie wartości MinimumTlsVersion i AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="3d6eb-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="3d6eb-135">Polecenie ustawia wartości MinimumTlsVersion i AllowBlobPublicAccess, a następnie wyświetla 2 właściwości konta.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

### <span data-ttu-id="3d6eb-136">Przykład 13. Aktualizowanie konta magazynu przy użyciu ustawienia RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="3d6eb-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="3d6eb-137">To polecenie aktualizuje konto magazynu przy użyciu ustawienia RoutingPreference: PublishMicrosoftEndpoint jako false, PublishInternetEndpoint jako prawda i RoutingChoice jako MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="3d6eb-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d6eb-138">PARAMETERS</span></span>

### <span data-ttu-id="3d6eb-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="3d6eb-139">-AccessTier</span></span>
<span data-ttu-id="3d6eb-140">Określa warstwę dostępu konta magazynu, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="3d6eb-141">Dopuszczalne wartości dla tego parametru to: Hot (Hot) i Cool (Cool).</span><span class="sxs-lookup"><span data-stu-id="3d6eb-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="3d6eb-142">Zmiana warstwy dostępu może spowodować naliszczenie dodatkowych opłat.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="3d6eb-143">Aby uzyskać więcej informacji, zobacz Magazyn obiektów blob platformy Azure: warstwy magazynów o większej i [najciekawszej wersji.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="3d6eb-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="3d6eb-144">Jeśli konto magazynu ma typ StorageV2 lub BlobStorage, możesz określić parametr *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="3d6eb-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="3d6eb-145">Jeśli dla konta magazynu jest typ jako magazyn, nie należy określać *parametru AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="3d6eb-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="3d6eb-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="3d6eb-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="3d6eb-147">Określa identyfikator zabezpieczeń (SID) dla magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="3d6eb-148">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="3d6eb-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="3d6eb-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="3d6eb-150">Określa identyfikator GUID domeny.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-150">Specifies the domain GUID.</span></span> <span data-ttu-id="3d6eb-151">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="3d6eb-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="3d6eb-153">Określa domenę podstawową, dla których autorytatywny jest serwer DNS usługi AD.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="3d6eb-154">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="3d6eb-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="3d6eb-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="3d6eb-156">Określa identyfikator zabezpieczeń (SID).</span><span class="sxs-lookup"><span data-stu-id="3d6eb-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="3d6eb-157">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="3d6eb-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="3d6eb-159">Określa las usługi Active Directory do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="3d6eb-160">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="3d6eb-161">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="3d6eb-162">Określa nazwę domeny NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="3d6eb-163">Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="3d6eb-164">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="3d6eb-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="3d6eb-165">Zezwalaj na dostęp publiczny do wszystkich obiektów blob lub kontenerów na koncie magazynu lub nie zezwalaj na ten dostęp.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="3d6eb-166">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3d6eb-166">-AsJob</span></span>
<span data-ttu-id="3d6eb-167">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3d6eb-167">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d6eb-168">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3d6eb-168">-AssignIdentity</span></span>
<span data-ttu-id="3d6eb-169">Wygeneruj i przypisz nowe konto magazynu Identity do tego konta magazynu do używania z usługami zarządzania kluczami, na przykład Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-169">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3d6eb-170">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-170">-CustomDomainName</span></span>
<span data-ttu-id="3d6eb-171">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-171">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="3d6eb-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6eb-172">-DefaultProfile</span></span>
<span data-ttu-id="3d6eb-173">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d6eb-174">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="3d6eb-174">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="3d6eb-175">Włącz uwierzytelnianie usługi domenowej Active Directory plików Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-176">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="3d6eb-176">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="3d6eb-177">Włącz uwierzytelnianie usługi domenowej Active Directory plików Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-177">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="3d6eb-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="3d6eb-179">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="3d6eb-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="3d6eb-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="3d6eb-181">Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o pojemności większej niż 5 tib.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="3d6eb-182">Po włączeniu konta nie można wyłączyć tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="3d6eb-183">Obecnie obsługiwane są tylko typy replikacji LRS i ZRS, przez co konwersja kont na geograficznie nadmiarowe konta nie będzie możliwa.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="3d6eb-184">Dowiedz się więcej w https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="3d6eb-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="3d6eb-185">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3d6eb-185">-Force</span></span>
<span data-ttu-id="3d6eb-186">Wymusza na wymusze wpisienie zmiany na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-186">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="3d6eb-187">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-187">-KeyName</span></span>
<span data-ttu-id="3d6eb-188">Jeśli używasz szyfrowania -KeyvaultEncryption w celu włączenia szyfrowania przy użyciu magazynu kluczy, określ właściwość Keyname (Nazwa klucza) za pomocą tej opcji.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-188">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-189">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3d6eb-189">-KeyvaultEncryption</span></span>
<span data-ttu-id="3d6eb-190">Wskazuje, czy podczas korzystania z szyfrowania usługi magazynowania należy używać funkcji Microsoft KeyVault do kluczy szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-190">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="3d6eb-191">Jeśli wszystkie wartości to KeyName, KeyVersion i KeyVaultUri, wartość KeySource zostanie ustawiona na Microsoft.Keyvault niezależnie od tego, czy ten parametr jest ustawiony.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-191">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-192">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3d6eb-192">-KeyVaultUri</span></span>
<span data-ttu-id="3d6eb-193">Podczas korzystania z szyfrowania magazynu kluczy przez określenie parametru -KeyvaultEncryption użyj tej opcji, aby określić URI do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-194">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="3d6eb-194">-KeyVersion</span></span>
<span data-ttu-id="3d6eb-195">Podczas korzystania z szyfrowania magazynu kluczy przez określenie parametru -KeyvaultEncryption użyj tej opcji, aby określić dla wersji klucza wartość URI.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-195">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-196">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3d6eb-196">-MinimumTlsVersion</span></span>
<span data-ttu-id="3d6eb-197">Minimalna wersja TLS, która jest dozwolona w żądaniach przechowywania.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-197">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="3d6eb-198">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3d6eb-198">-Name</span></span>
<span data-ttu-id="3d6eb-199">Określa nazwę konta magazynu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-199">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="3d6eb-200">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d6eb-200">-NetworkRuleSet</span></span>
<span data-ttu-id="3d6eb-201">Zestaw NetworkRuleSet służy do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do określania wartości właściwości sieciowych, takich jak usługi mogące pomijać reguły i sposób obsługi żądań, które nie są zgodne z żadnymi zdefiniowanymi regułami.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-201">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="3d6eb-202">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d6eb-202">-PublishInternetEndpoint</span></span>
<span data-ttu-id="3d6eb-203">Wskazuje, czy punkty końcowe magazynu routingu internetowego mają zostać opublikowane.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-203">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="3d6eb-204">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d6eb-204">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="3d6eb-205">Wskazuje, czy punkty końcowe magazynu routingu firmy Microsoft mają zostać opublikowane.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-205">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="3d6eb-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-206">-ResourceGroupName</span></span>
<span data-ttu-id="3d6eb-207">Określa nazwę grupy zasobów, w której ma być modyfikowane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-207">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="3d6eb-208">- RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="3d6eb-208">-RoutingChoice</span></span>
<span data-ttu-id="3d6eb-209">Wybór routingu określa rodzaj routingu sieciowego wybierany przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-209">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="3d6eb-210">Możliwe wartości: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="3d6eb-210">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="3d6eb-211">-SKUName</span><span class="sxs-lookup"><span data-stu-id="3d6eb-211">-SkuName</span></span>
<span data-ttu-id="3d6eb-212">Określa nazwę sku konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-212">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="3d6eb-213">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3d6eb-213">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d6eb-214">Standard_LRS — magazyn nadmiarowy lokalnie.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-214">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="3d6eb-215">Standard_ZRS — nadmiarowa przestrzeń dyskowa bez stref.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-215">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="3d6eb-216">Standard_GRS — magazyn nadmiarowy geograficznie.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-216">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="3d6eb-217">Standard_RAGRS — odczyt danych o nadmiarowej przestrzeni dyskowej geograficznej.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-217">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="3d6eb-218">Premium_LRS — lokalnie nadmiarowa przestrzeń dyskowa Premium.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-218">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="3d6eb-219">Standard_GZRS — nadmiarowa geograficznie nadmiarowa przestrzeń dyskowa bez stref.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-219">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="3d6eb-220">Standard_RAGZRS — odczyt nadmiarowy geograficznie nadmiarowy magazyn strefy.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-220">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="3d6eb-221">Typów kont Standard_ZRS i Premium_LRS nie można zmienić na inne typy kont.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-221">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="3d6eb-222">Nie możesz zmienić innych typów kont na Standard_ZRS lub Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-222">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-223">- StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="3d6eb-223">-StorageEncryption</span></span>
<span data-ttu-id="3d6eb-224">Wskazuje, czy chcesz skonfigurować szyfrowanie konta magazynu do używania kluczy zarządzanych przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-224">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-225">— Tag</span><span class="sxs-lookup"><span data-stu-id="3d6eb-225">-Tag</span></span>
<span data-ttu-id="3d6eb-226">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi na serwerze.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-226">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="3d6eb-227">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3d6eb-227">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-228">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="3d6eb-228">-UpgradeToStorageV2</span></span>
<span data-ttu-id="3d6eb-229">Uaktualnij typ konta magazynu z magazynu lub usługi BlobStorage do storageV2.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-229">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="3d6eb-230">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="3d6eb-230">-UseSubDomain</span></span>
<span data-ttu-id="3d6eb-231">Wskazuje, czy należy włączyć pośrednie sprawdzanie poprawności CName.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-231">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="3d6eb-232">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d6eb-232">-Confirm</span></span>
<span data-ttu-id="3d6eb-233">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-233">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-234">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6eb-234">-WhatIf</span></span>
<span data-ttu-id="3d6eb-235">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-235">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6eb-236">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-236">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6eb-237">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6eb-237">CommonParameters</span></span>
<span data-ttu-id="3d6eb-238">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6eb-238">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6eb-239">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6eb-239">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6eb-240">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d6eb-240">INPUTS</span></span>

### <span data-ttu-id="3d6eb-241">System.String</span><span class="sxs-lookup"><span data-stu-id="3d6eb-241">System.String</span></span>

### <span data-ttu-id="3d6eb-242">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d6eb-242">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d6eb-243">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d6eb-243">OUTPUTS</span></span>

### <span data-ttu-id="3d6eb-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d6eb-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3d6eb-245">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d6eb-245">NOTES</span></span>

## <span data-ttu-id="3d6eb-246">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d6eb-246">RELATED LINKS</span></span>

[<span data-ttu-id="3d6eb-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d6eb-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="3d6eb-248">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d6eb-248">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="3d6eb-249">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d6eb-249">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
