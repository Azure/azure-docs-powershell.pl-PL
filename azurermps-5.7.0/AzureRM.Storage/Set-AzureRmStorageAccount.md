---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542136"
---
# <span data-ttu-id="c6aaa-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6aaa-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="c6aaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="c6aaa-103">Modyfikuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6aaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6aaa-104">SYNTAX</span></span>

### <span data-ttu-id="c6aaa-105">StorageEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c6aaa-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6aaa-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c6aaa-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6aaa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c6aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="c6aaa-108">Polecenie cmdlet **Set-AzureRmStorageAccount** modyfikuje konto usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="c6aaa-109">Za pomocą tego polecenia cmdlet można zmodyfikować typ konta, zaktualizować domenę klienta lub ustawić Tagi na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="c6aaa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6aaa-110">EXAMPLES</span></span>

### <span data-ttu-id="c6aaa-111">Przykład 1: Ustawianie typu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6aaa-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="c6aaa-112">To polecenie ustawia typ konta magazynu na Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="c6aaa-113">Przykład 2: Ustawianie domeny niestandardowej dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6aaa-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="c6aaa-114">To polecenie ustawia niestandardową domenę dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="c6aaa-115">Przykład 3: Włączanie szyfrowania obiektów blob i usług plików</span><span class="sxs-lookup"><span data-stu-id="c6aaa-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="c6aaa-116">To polecenie umożliwia włączenie szyfrowania obiektu BLOB i pliku dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="c6aaa-117">Przykład 4: Ustawianie wartości warstwy dostępu</span><span class="sxs-lookup"><span data-stu-id="c6aaa-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="c6aaa-118">Polecenie ustawia wartość w warstwie dostępu jako schłodzić.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c6aaa-119">Przykład 4: Ustawianie niestandardowej domeny i tagów</span><span class="sxs-lookup"><span data-stu-id="c6aaa-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="c6aaa-120">Polecenie ustawia wartość w warstwie dostępu jako schłodzić.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c6aaa-121">Przykład 5: Włączanie szyfrowania w usługach BLOB za pomocą magazynu typu</span><span class="sxs-lookup"><span data-stu-id="c6aaa-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="c6aaa-122">To polecenie umożliwia włączenie szyfrowania obiektu BLOB przy użyciu nowego utworzonego magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="c6aaa-123">Przykład 6: wyłączenie szyfrowania w usługach plików za pomocą zestawu źródeł klucza "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="c6aaa-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="c6aaa-124">To polecenie wyłącza szyfrowanie usług plików za pomocą zestawu źródeł klucza "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="c6aaa-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="c6aaa-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6aaa-125">PARAMETERS</span></span>

### <span data-ttu-id="c6aaa-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c6aaa-126">-AccessTier</span></span>
<span data-ttu-id="c6aaa-127">Określa warstwę dostępu konta magazynu, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="c6aaa-128">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="c6aaa-129">Zmiana warstwy dostępu może spowodować dodatkowe opłaty.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="c6aaa-130">Aby uzyskać więcej informacji, zobacz Usługa Azure Blob Storage: warstwy magazynowania dla urządzeń typu hot i chłodn https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="c6aaa-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c6aaa-131">Jeśli typ konta magazynu to magazyn, nie określaj tego parametru.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="c6aaa-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c6aaa-132">-AssignIdentity</span></span>
<span data-ttu-id="c6aaa-133">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c6aaa-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c6aaa-134">-CustomDomainName</span></span>
<span data-ttu-id="c6aaa-135">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-135">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="c6aaa-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="c6aaa-136">-DisableEncryptionService</span></span>
<span data-ttu-id="c6aaa-137">Wskazuje, czy to polecenie cmdlet wyłącza szyfrowanie usługi magazynu w usłudze magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="c6aaa-138">Usługa Azure BLOB i usługi Azure File Services są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="c6aaa-139">-EnableEncryptionService</span></span>
<span data-ttu-id="c6aaa-140">Wskazuje, czy to polecenie cmdlet umożliwia szyfrowanie usługi magazynu w usłudze magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="c6aaa-141">Usługa Azure BLOB i usługi Azure File Services są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c6aaa-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c6aaa-143">Wskazuje, czy konto magazynu umożliwia tylko ruch https.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="c6aaa-144">-Force</span><span class="sxs-lookup"><span data-stu-id="c6aaa-144">-Force</span></span>
<span data-ttu-id="c6aaa-145">Zmiana warstwy dostępu może spowodować dodatkowe opłaty.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="c6aaa-146">Aby uzyskać więcej informacji, zobacz Usługa Azure Blob Storage: warstwy magazynowania dla urządzeń typu hot i chłodn https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="c6aaa-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c6aaa-147">Jeśli typ konta magazynu to magazyn, nie określaj tego parametru.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="c6aaa-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6aaa-148">-InformationAction</span></span>
<span data-ttu-id="c6aaa-149">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6aaa-150">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c6aaa-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6aaa-151">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c6aaa-151">Continue</span></span>
- <span data-ttu-id="c6aaa-152">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c6aaa-152">Ignore</span></span>
- <span data-ttu-id="c6aaa-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="c6aaa-153">Inquire</span></span>
- <span data-ttu-id="c6aaa-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6aaa-154">SilentlyContinue</span></span>
- <span data-ttu-id="c6aaa-155">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c6aaa-155">Stop</span></span>
- <span data-ttu-id="c6aaa-156">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c6aaa-156">Suspend</span></span>

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

### <span data-ttu-id="c6aaa-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6aaa-157">-InformationVariable</span></span>
<span data-ttu-id="c6aaa-158">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-158">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6aaa-159">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="c6aaa-159">-KeyName</span></span>
<span data-ttu-id="c6aaa-160">Dysk źródłowy klucza szyfrowania konta magazynu # NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="c6aaa-160">Storage Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c6aaa-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="c6aaa-162">Określa, czy należy ustawić źródło klucza szyfrowania konta magazynu na Microsoft. lub nie.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span>
<span data-ttu-id="c6aaa-163">Jeśli określisz wartość KeyName, wersja klucza i KeyvaultUri, Źródło klucza szyfrowania konta magazynu zostanie również ustawione na Microsoft. Pogoda dla magazynu danych ten parametr jest ustawiony lub nie.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c6aaa-164">-KeyVaultUri</span></span>
<span data-ttu-id="c6aaa-165">KeyVaultUria klucza źródłowego klucza szyfrowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6aaa-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-166">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="c6aaa-166">-KeyVersion</span></span>
<span data-ttu-id="c6aaa-167">Wersja klucza magazynu klucza szyfrowania konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6aaa-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-168">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6aaa-168">-Name</span></span>
<span data-ttu-id="c6aaa-169">Określa nazwę konta magazynu, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="c6aaa-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6aaa-170">-ResourceGroupName</span></span>
<span data-ttu-id="c6aaa-171">Określa nazwę grupy zasobów, w której należy zmodyfikować konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-171">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="c6aaa-172">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c6aaa-172">-SkuName</span></span>
<span data-ttu-id="c6aaa-173">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-173">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="c6aaa-174">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c6aaa-174">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6aaa-175">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-175">Standard_LRS.</span></span>
<span data-ttu-id="c6aaa-176">Magazyn lokalny-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-176">Locally-redundant storage.</span></span>
- <span data-ttu-id="c6aaa-177">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-177">Standard_ZRS.</span></span>
<span data-ttu-id="c6aaa-178">Miejsce do magazynowania nadmiarowych stref.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-178">Zone-redundant storage.</span></span>
- <span data-ttu-id="c6aaa-179">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-179">Standard_GRS.</span></span>
<span data-ttu-id="c6aaa-180">Magazyn Geograficznie nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-180">Geo-redundant storage.</span></span>
- <span data-ttu-id="c6aaa-181">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-181">Standard_RAGRS.</span></span>
<span data-ttu-id="c6aaa-182">Dostęp do odczytu geograficznie zapasowego miejsca.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-182">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="c6aaa-183">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-183">Premium_LRS.</span></span>
<span data-ttu-id="c6aaa-184">Premium miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-184">Premium locally-redundant storage.</span></span>

<span data-ttu-id="c6aaa-185">Nie można zmieniać typów Standard_ZRS i Premium_LRS na inne typy kont.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-185">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="c6aaa-186">Nie można zmienić innych typów kont na Standard_ZRS lub Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-186">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-187">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="c6aaa-187">-StorageEncryption</span></span>
<span data-ttu-id="c6aaa-188">Czy chcesz ustawić źródło klucza szyfrowania konta magazynu na Microsoft. Storage, czy nie.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-188">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6aaa-189">-Tag</span></span>
<span data-ttu-id="c6aaa-190">Jeśli określisz wartość BlobStorage dla parametru *Kind* polecenia cmdlet New-AzureRmStorageAccount, musisz określić wartość parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c6aaa-190">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="c6aaa-191">Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c6aaa-191">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c6aaa-192">-UseSubDomain</span></span>
<span data-ttu-id="c6aaa-193">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-193">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-194">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6aaa-194">-Confirm</span></span>
<span data-ttu-id="c6aaa-195">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6aaa-196">-WhatIf</span></span>
<span data-ttu-id="c6aaa-197">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6aaa-198">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-198">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6aaa-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6aaa-199">CommonParameters</span></span>
<span data-ttu-id="c6aaa-200">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6aaa-201">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6aaa-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6aaa-202">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6aaa-202">INPUTS</span></span>

### <span data-ttu-id="c6aaa-203">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c6aaa-203">None</span></span>
<span data-ttu-id="c6aaa-204">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c6aaa-204">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6aaa-205">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6aaa-205">OUTPUTS</span></span>

## <span data-ttu-id="c6aaa-206">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6aaa-206">NOTES</span></span>

## <span data-ttu-id="c6aaa-207">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6aaa-207">RELATED LINKS</span></span>

[<span data-ttu-id="c6aaa-208">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6aaa-208">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="c6aaa-209">Nowe — AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6aaa-209">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="c6aaa-210">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6aaa-210">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
