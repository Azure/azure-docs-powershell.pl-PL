---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224745"
---
# <span data-ttu-id="88af7-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88af7-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="88af7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88af7-102">SYNOPSIS</span></span>
<span data-ttu-id="88af7-103">Modyfikuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="88af7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88af7-104">SYNTAX</span></span>

### <span data-ttu-id="88af7-105">StorageEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="88af7-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88af7-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="88af7-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88af7-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="88af7-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88af7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="88af7-108">DESCRIPTION</span></span>
<span data-ttu-id="88af7-109">Polecenie cmdlet **Set-AzStorageAccount** modyfikuje konto usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="88af7-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="88af7-110">Za pomocą tego polecenia cmdlet można zmodyfikować typ konta, zaktualizować domenę klienta lub ustawić Tagi na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="88af7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88af7-111">EXAMPLES</span></span>

### <span data-ttu-id="88af7-112">Przykład 1: Ustawianie typu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="88af7-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="88af7-113">To polecenie ustawia typ konta magazynu na Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="88af7-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="88af7-114">Przykład 2: Ustawianie domeny niestandardowej dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="88af7-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="88af7-115">To polecenie ustawia niestandardową domenę dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="88af7-116">Przykład 3: Ustawianie wartości warstwy dostępu</span><span class="sxs-lookup"><span data-stu-id="88af7-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="88af7-117">Polecenie ustawia wartość w warstwie dostępu jako schłodzić.</span><span class="sxs-lookup"><span data-stu-id="88af7-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="88af7-118">Przykład 4: Ustawianie niestandardowej domeny i tagów</span><span class="sxs-lookup"><span data-stu-id="88af7-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="88af7-119">Polecenie ustawia niestandardową domenę i Tagi dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="88af7-120">Przykład 5: Ustawianie źródła klucza szyfrowania dla magazynu klucza</span><span class="sxs-lookup"><span data-stu-id="88af7-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="88af7-121">To polecenie ustawia źródło klucza szyfrowania z nowym utworzonym magazynem.</span><span class="sxs-lookup"><span data-stu-id="88af7-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="88af7-122">Przykład 6: Ustawianie źródła klucza szyfrowania na "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="88af7-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="88af7-123">To polecenie ustawia źródło klucza szyfrowania na "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="88af7-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="88af7-124">Przykład 7: Ustawianie właściwości NetworkRuleSet konta magazynu przy użyciu notacji JSON</span><span class="sxs-lookup"><span data-stu-id="88af7-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="88af7-125">To polecenie ustawia właściwość NetworkRuleSet konta magazynu przy użyciu notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="88af7-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="88af7-126">Przykład 8: pobieranie właściwości NetworkRuleSet z konta magazynu i ustawienie jej na inne konto magazynu</span><span class="sxs-lookup"><span data-stu-id="88af7-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="88af7-127">To pierwsze polecenie pobiera właściwość NetworkRuleSet z konta magazynu, a drugie polecenie ustawia je na inne konto magazynu</span><span class="sxs-lookup"><span data-stu-id="88af7-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="88af7-128">Przykład 9: uaktualnienie konta magazynu z rodzajem "magazyn" lub "BlobStorage" na "StorageV2" rodzajem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="88af7-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="88af7-129">Polecenie Uaktualnij konto magazynu, używając typu "Storage" lub "BlobStorage" do "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="88af7-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="88af7-130">Przykład 10: aktualizowanie konta magazynu przez włączenie uwierzytelniania usług domenowych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="88af7-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="88af7-131">Polecenie umożliwia zaktualizowanie konta magazynu przez włączenie uwierzytelniania usług domenowych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="88af7-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="88af7-132">Przykład 11: aktualizowanie konta magazynu przez włączenie uwierzytelniania usługi domeny Active Directory, a następnie wyświetlenie ustawienia uwierzytelniania opartego na tożsamości pliku</span><span class="sxs-lookup"><span data-stu-id="88af7-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="88af7-133">Polecenie aktualizuje konto magazynu przez włączenie uwierzytelniania usługi Domain File Active Directory na platformie Azure, a następnie wyświetlenie ustawienia uwierzytelniania opartego na tożsamości pliku.</span><span class="sxs-lookup"><span data-stu-id="88af7-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="88af7-134">Przykład 12: Set MinimumTlsVersion i AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="88af7-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="88af7-135">Polecenie ustawia MinimumTlsVersion i AllowBlobPublicAccess, a następnie Pokaż 2 właściwości konta</span><span class="sxs-lookup"><span data-stu-id="88af7-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="88af7-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88af7-136">PARAMETERS</span></span>

### <span data-ttu-id="88af7-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="88af7-137">-AccessTier</span></span>
<span data-ttu-id="88af7-138">Określa warstwę dostępu konta magazynu, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88af7-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="88af7-139">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="88af7-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="88af7-140">Zmiana warstwy dostępu może spowodować dodatkowe opłaty.</span><span class="sxs-lookup"><span data-stu-id="88af7-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="88af7-141">Aby uzyskać więcej informacji, zobacz [usługa Azure Blob Storage: warstwy magazynowania dla urządzeń typu hot i chłodn](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="88af7-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="88af7-142">Jeśli konto magazynu ma charakter StorageV2 lub BlobStorage, możesz określić parametr *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="88af7-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="88af7-143">Jeśli konto magazynu ma jako miejsce do magazynowania, nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="88af7-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="88af7-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="88af7-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="88af7-145">Określa identyfikator zabezpieczeń (SID) usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="88af7-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="88af7-146">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="88af7-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="88af7-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="88af7-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="88af7-148">Określa identyfikator GUID domeny.</span><span class="sxs-lookup"><span data-stu-id="88af7-148">Specifies the domain GUID.</span></span> <span data-ttu-id="88af7-149">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="88af7-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="88af7-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="88af7-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="88af7-151">Określa podstawową domenę, dla której serwer DNS usługi AD jest autorytatywny.</span><span class="sxs-lookup"><span data-stu-id="88af7-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="88af7-152">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="88af7-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="88af7-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="88af7-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="88af7-154">Określa identyfikator zabezpieczeń (SID).</span><span class="sxs-lookup"><span data-stu-id="88af7-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="88af7-155">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="88af7-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="88af7-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="88af7-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="88af7-157">Określa Las usługi Active Directory do pobrania.</span><span class="sxs-lookup"><span data-stu-id="88af7-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="88af7-158">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="88af7-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="88af7-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="88af7-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="88af7-160">Określa nazwę domeny NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="88af7-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="88af7-161">Ten parametr musi być ustawiony, gdy dla parametru-EnableActiveDirectoryDomainServicesForFile jest ustawiona wartość true.</span><span class="sxs-lookup"><span data-stu-id="88af7-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="88af7-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="88af7-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="88af7-163">Zezwalanie na publiczny dostęp do wszystkich obiektów blob lub kontenerów na koncie magazynu lub niezezwalanie na nie.</span><span class="sxs-lookup"><span data-stu-id="88af7-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="88af7-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88af7-164">-AsJob</span></span>
<span data-ttu-id="88af7-165">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="88af7-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88af7-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="88af7-166">-AssignIdentity</span></span>
<span data-ttu-id="88af7-167">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88af7-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="88af7-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="88af7-168">-CustomDomainName</span></span>
<span data-ttu-id="88af7-169">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="88af7-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="88af7-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88af7-170">-DefaultProfile</span></span>
<span data-ttu-id="88af7-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88af7-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88af7-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="88af7-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="88af7-173">Włącz uwierzytelnianie usługi domenowe Active Directory na platformie Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="88af7-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="88af7-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="88af7-175">Włącz uwierzytelnianie usługi domenowe Active Directory na platformie Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="88af7-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="88af7-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="88af7-177">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="88af7-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="88af7-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="88af7-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="88af7-179">Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o wydajności większej niż 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="88af7-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="88af7-180">Po włączeniu konta nie można wyłączyć funkcji.</span><span class="sxs-lookup"><span data-stu-id="88af7-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="88af7-181">Obecnie obsługiwane tylko dla typów replikacji LRS i ZRS, dzięki czemu konwersje kont na konta z nadmiarowością geograficzną nie będą możliwe.</span><span class="sxs-lookup"><span data-stu-id="88af7-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="88af7-182">Więcej informacji https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="88af7-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="88af7-183">-Force</span><span class="sxs-lookup"><span data-stu-id="88af7-183">-Force</span></span>
<span data-ttu-id="88af7-184">Wymusza zapisanie zmiany na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="88af7-185">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="88af7-185">-KeyName</span></span>
<span data-ttu-id="88af7-186">Jeśli w przypadku korzystania z funkcji-KeyvaultEncryption w celu włączenia szyfrowania za pomocą magazynu kluczy Określ właściwość KeyName z tą opcją.</span><span class="sxs-lookup"><span data-stu-id="88af7-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="88af7-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="88af7-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="88af7-188">Wskazuje, czy chcesz używać usługi Microsoft Keys do obsługi kluczy szyfrowania podczas korzystania z szyfrowania usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="88af7-189">Jeśli dla wszystkich zestawów jest ustawiony parametr NazwaKlucza, wersja klucza i KeyVaultUri, dla źródła klucza zostanie ustawiona wartość Microsoft. DataSources, niezależnie od tego, czy ten parametr jest ustawiony.</span><span class="sxs-lookup"><span data-stu-id="88af7-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="88af7-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="88af7-190">-KeyVaultUri</span></span>
<span data-ttu-id="88af7-191">W przypadku korzystania z szyfrowania magazynu kluczy przez określenie parametru-KeyvaultEncryption Użyj tej opcji, aby określić identyfikator URI dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="88af7-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="88af7-192">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="88af7-192">-KeyVersion</span></span>
<span data-ttu-id="88af7-193">W przypadku korzystania z szyfrowania magazynu kluczy przez określenie parametru-KeyvaultEncryption Użyj tej opcji, aby określić identyfikator URI dla wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="88af7-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="88af7-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="88af7-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="88af7-195">Minimalna wersja protokołu TLS, która ma być dozwolona na żądaniach magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-195">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="88af7-196">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88af7-196">-Name</span></span>
<span data-ttu-id="88af7-197">Określa nazwę konta magazynu, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="88af7-197">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="88af7-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="88af7-198">-NetworkRuleSet</span></span>
<span data-ttu-id="88af7-199">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do ustawiania wartości właściwości sieci, takich jak usługi, które mogą pomijać reguły, oraz sposobu obsługi żądań niezgodnych z żadną określoną regułą.</span><span class="sxs-lookup"><span data-stu-id="88af7-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="88af7-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88af7-200">-ResourceGroupName</span></span>
<span data-ttu-id="88af7-201">Określa nazwę grupy zasobów, w której należy zmodyfikować konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="88af7-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="88af7-202">-SkuName</span></span>
<span data-ttu-id="88af7-203">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="88af7-204">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="88af7-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88af7-205">Standard_LRS-lokalne-nadmiarowe miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="88af7-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="88af7-206">Standard_ZRS-Zone-nadmiarowa pamięć.</span><span class="sxs-lookup"><span data-stu-id="88af7-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="88af7-207">Miejsce do magazynowania w Standard_GRS-Geo-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="88af7-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="88af7-208">Standard_RAGRS odczytu geograficznie zapasowego miejsca do odczytu.</span><span class="sxs-lookup"><span data-stu-id="88af7-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="88af7-209">Miejsce do magazynowania zapasowego Premium_LRS-Premium.</span><span class="sxs-lookup"><span data-stu-id="88af7-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="88af7-210">Standard_GZRS-nadmiarowe miejsce w strefie geograficznej.</span><span class="sxs-lookup"><span data-stu-id="88af7-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="88af7-211">Standard_RAGZRS — dostęp do odczytu Geograficznie nadmiarowy obszar magazynu.</span><span class="sxs-lookup"><span data-stu-id="88af7-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="88af7-212">Nie można zmieniać typów Standard_ZRS i Premium_LRS na inne typy kont.</span><span class="sxs-lookup"><span data-stu-id="88af7-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="88af7-213">Nie można zmienić innych typów kont na Standard_ZRS lub Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="88af7-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="88af7-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="88af7-214">-StorageEncryption</span></span>
<span data-ttu-id="88af7-215">Wskazuje, czy chcesz ustawić szyfrowanie konta magazynu w celu używania kluczy zarządzanych przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88af7-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="88af7-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="88af7-216">-Tag</span></span>
<span data-ttu-id="88af7-217">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="88af7-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="88af7-218">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="88af7-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="88af7-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="88af7-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="88af7-220">Uaktualnij rodzaj konta magazynu z magazynu lub BlobStorage do StorageV2.</span><span class="sxs-lookup"><span data-stu-id="88af7-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="88af7-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="88af7-221">-UseSubDomain</span></span>
<span data-ttu-id="88af7-222">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="88af7-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="88af7-223">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88af7-223">-Confirm</span></span>
<span data-ttu-id="88af7-224">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88af7-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88af7-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88af7-225">-WhatIf</span></span>
<span data-ttu-id="88af7-226">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88af7-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88af7-227">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88af7-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88af7-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88af7-228">CommonParameters</span></span>
<span data-ttu-id="88af7-229">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88af7-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88af7-230">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88af7-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88af7-231">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88af7-231">INPUTS</span></span>

### <span data-ttu-id="88af7-232">System. String</span><span class="sxs-lookup"><span data-stu-id="88af7-232">System.String</span></span>

### <span data-ttu-id="88af7-233">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88af7-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88af7-234">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88af7-234">OUTPUTS</span></span>

### <span data-ttu-id="88af7-235">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88af7-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="88af7-236">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88af7-236">NOTES</span></span>

## <span data-ttu-id="88af7-237">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88af7-237">RELATED LINKS</span></span>

[<span data-ttu-id="88af7-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88af7-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="88af7-239">Nowe — AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88af7-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="88af7-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88af7-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
