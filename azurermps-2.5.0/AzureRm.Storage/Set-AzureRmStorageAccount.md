---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: a6f16c4ef9012f7aaf5216e0cfb24edf65ce9f4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898133"
---
# <span data-ttu-id="ec022-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec022-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="ec022-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec022-102">SYNOPSIS</span></span>
<span data-ttu-id="ec022-103">Modyfikuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec022-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec022-104">SYNTAX</span></span>

### <span data-ttu-id="ec022-105">StorageEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec022-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec022-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ec022-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec022-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ec022-107">DESCRIPTION</span></span>
<span data-ttu-id="ec022-108">Polecenie cmdlet **Set-AzureRmStorageAccount** modyfikuje konto usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ec022-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="ec022-109">Za pomocą tego polecenia cmdlet można zmodyfikować typ konta, zaktualizować domenę klienta lub ustawić Tagi na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="ec022-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec022-110">EXAMPLES</span></span>

### <span data-ttu-id="ec022-111">Przykład 1: Ustawianie typu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ec022-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="ec022-112">To polecenie ustawia typ konta magazynu na Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="ec022-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="ec022-113">Przykład 2: Ustawianie domeny niestandardowej dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ec022-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="ec022-114">To polecenie ustawia niestandardową domenę dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="ec022-115">Przykład 3: Ustawianie wartości warstwy dostępu</span><span class="sxs-lookup"><span data-stu-id="ec022-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="ec022-116">Polecenie ustawia wartość w warstwie dostępu jako schłodzić.</span><span class="sxs-lookup"><span data-stu-id="ec022-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="ec022-117">Przykład 4: Ustawianie niestandardowej domeny i tagów</span><span class="sxs-lookup"><span data-stu-id="ec022-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="ec022-118">Polecenie ustawia niestandardową domenę i Tagi dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="ec022-119">Przykład 5: Ustawianie źródła klucza szyfrowania dla magazynu klucza</span><span class="sxs-lookup"><span data-stu-id="ec022-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="ec022-120">To polecenie ustawia źródło klucza szyfrowania z nowym utworzonym magazynem.</span><span class="sxs-lookup"><span data-stu-id="ec022-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="ec022-121">Przykład 6: Ustawianie źródła klucza szyfrowania na "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="ec022-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="ec022-122">To polecenie ustawia źródło klucza szyfrowania na "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="ec022-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="ec022-123">Przykład 7: Ustawianie właściwości NetworkRuleSet konta magazynu przy użyciu notacji JSON</span><span class="sxs-lookup"><span data-stu-id="ec022-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="ec022-124">To polecenie ustawia właściwość NetworkRuleSet konta magazynu przy użyciu notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="ec022-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="ec022-125">Przykład 8: pobieranie właściwości NetworkRuleSet z konta magazynu i ustawienie jej na inne konto magazynu</span><span class="sxs-lookup"><span data-stu-id="ec022-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="ec022-126">To pierwsze polecenie pobiera właściwość NetworkRuleSet z konta magazynu, a drugie polecenie ustawia je na inne konto magazynu</span><span class="sxs-lookup"><span data-stu-id="ec022-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="ec022-127">Przykład 9: uaktualnienie konta magazynu z rodzajem "magazyn" lub "BlobStorage" na "StorageV2" rodzajem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ec022-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="ec022-128">Polecenie Uaktualnij konto magazynu, używając typu "Storage" lub "BlobStorage" do "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="ec022-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="ec022-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec022-129">PARAMETERS</span></span>

### <span data-ttu-id="ec022-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ec022-130">-AccessTier</span></span>
<span data-ttu-id="ec022-131">Określa warstwę dostępu konta magazynu, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec022-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="ec022-132">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="ec022-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="ec022-133">Zmiana warstwy dostępu może spowodować dodatkowe opłaty.</span><span class="sxs-lookup"><span data-stu-id="ec022-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="ec022-134">Aby uzyskać więcej informacji, zobacz [usługa Azure Blob Storage: warstwy magazynowania dla urządzeń typu hot i chłodn](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="ec022-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="ec022-135">Jeśli konto magazynu ma charakter StorageV2 lub BlobStorage, możesz określić parametr *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="ec022-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="ec022-136">Jeśli konto magazynu ma jako miejsce do magazynowania, nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="ec022-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="ec022-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec022-137">-AsJob</span></span>
<span data-ttu-id="ec022-138">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ec022-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec022-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ec022-139">-AssignIdentity</span></span>
<span data-ttu-id="ec022-140">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ec022-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ec022-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ec022-141">-CustomDomainName</span></span>
<span data-ttu-id="ec022-142">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="ec022-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="ec022-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec022-143">-DefaultProfile</span></span>
<span data-ttu-id="ec022-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec022-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec022-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="ec022-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="ec022-146">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ec022-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec022-147">-Force</span><span class="sxs-lookup"><span data-stu-id="ec022-147">-Force</span></span>
<span data-ttu-id="ec022-148">Wymusza zapisanie zmiany na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="ec022-149">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="ec022-149">-KeyName</span></span>
<span data-ttu-id="ec022-150">Jeśli w przypadku korzystania z funkcji-KeyvaultEncryption w celu włączenia szyfrowania za pomocą magazynu kluczy Określ właściwość KeyName z tą opcją.</span><span class="sxs-lookup"><span data-stu-id="ec022-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="ec022-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ec022-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="ec022-152">Wskazuje, czy chcesz używać usługi Microsoft Keys do obsługi kluczy szyfrowania podczas korzystania z szyfrowania usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="ec022-153">Jeśli dla wszystkich zestawów jest ustawiony parametr NazwaKlucza, wersja klucza i KeyVaultUri, dla źródła klucza zostanie ustawiona wartość Microsoft. DataSources, niezależnie od tego, czy ten parametr jest ustawiony.</span><span class="sxs-lookup"><span data-stu-id="ec022-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="ec022-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ec022-154">-KeyVaultUri</span></span>
<span data-ttu-id="ec022-155">W przypadku korzystania z szyfrowania magazynu kluczy przez określenie parametru-KeyvaultEncryption Użyj tej opcji, aby określić identyfikator URI dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="ec022-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="ec022-156">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="ec022-156">-KeyVersion</span></span>
<span data-ttu-id="ec022-157">W przypadku korzystania z szyfrowania magazynu kluczy przez określenie parametru-KeyvaultEncryption Użyj tej opcji, aby określić identyfikator URI dla wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="ec022-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="ec022-158">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec022-158">-Name</span></span>
<span data-ttu-id="ec022-159">Określa nazwę konta magazynu, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="ec022-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="ec022-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec022-160">-NetworkRuleSet</span></span>
<span data-ttu-id="ec022-161">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do ustawiania wartości właściwości sieci, takich jak usługi, które mogą pomijać reguły, oraz sposobu obsługi żądań niezgodnych z żadną określoną regułą.</span><span class="sxs-lookup"><span data-stu-id="ec022-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="ec022-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec022-162">-ResourceGroupName</span></span>
<span data-ttu-id="ec022-163">Określa nazwę grupy zasobów, w której należy zmodyfikować konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="ec022-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ec022-164">-SkuName</span></span>
<span data-ttu-id="ec022-165">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec022-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="ec022-166">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ec022-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec022-167">Standard_LRS-lokalne-nadmiarowe miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="ec022-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="ec022-168">Standard_ZRS-Zone-nadmiarowa pamięć.</span><span class="sxs-lookup"><span data-stu-id="ec022-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="ec022-169">Miejsce do magazynowania w Standard_GRS-Geo-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="ec022-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="ec022-170">Standard_RAGRS odczytu geograficznie zapasowego miejsca do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ec022-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="ec022-171">Miejsce do magazynowania zapasowego Premium_LRS-Premium.</span><span class="sxs-lookup"><span data-stu-id="ec022-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="ec022-172">Nie można zmieniać typów Standard_ZRS i Premium_LRS na inne typy kont.</span><span class="sxs-lookup"><span data-stu-id="ec022-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="ec022-173">Nie można zmienić innych typów kont na Standard_ZRS lub Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="ec022-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec022-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="ec022-174">-StorageEncryption</span></span>
<span data-ttu-id="ec022-175">Wskazuje, czy chcesz ustawić szyfrowanie konta magazynu w celu używania kluczy zarządzanych przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec022-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="ec022-176">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec022-176">-Tag</span></span>
<span data-ttu-id="ec022-177">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="ec022-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ec022-178">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ec022-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ec022-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="ec022-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="ec022-180">Uaktualnij rodzaj konta magazynu z magazynu lub BlobStorage do StorageV2.</span><span class="sxs-lookup"><span data-stu-id="ec022-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="ec022-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="ec022-181">-UseSubDomain</span></span>
<span data-ttu-id="ec022-182">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="ec022-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="ec022-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec022-183">-Confirm</span></span>
<span data-ttu-id="ec022-184">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec022-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec022-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec022-185">-WhatIf</span></span>
<span data-ttu-id="ec022-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec022-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec022-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec022-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec022-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec022-188">CommonParameters</span></span>
<span data-ttu-id="ec022-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec022-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec022-190">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec022-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec022-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec022-191">INPUTS</span></span>

### <span data-ttu-id="ec022-192">System. String</span><span class="sxs-lookup"><span data-stu-id="ec022-192">System.String</span></span>

### <span data-ttu-id="ec022-193">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ec022-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ec022-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec022-194">System.Boolean</span></span>

## <span data-ttu-id="ec022-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec022-195">OUTPUTS</span></span>

### <span data-ttu-id="ec022-196">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec022-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ec022-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec022-197">NOTES</span></span>

## <span data-ttu-id="ec022-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec022-198">RELATED LINKS</span></span>

[<span data-ttu-id="ec022-199">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec022-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="ec022-200">Nowe — AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec022-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="ec022-201">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec022-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
