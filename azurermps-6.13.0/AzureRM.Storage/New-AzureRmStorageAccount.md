---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 2ceb395805607809593054880415dccac7e1e28c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547315"
---
# <span data-ttu-id="2d7a2-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d7a2-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="2d7a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7a2-103">Tworzy konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d7a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d7a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d7a2-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7a2-106">Polecenie cmdlet **New-AzureRmStorageAccount** umożliwia utworzenie konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="2d7a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d7a2-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7a2-108">Przykład 1. Tworzenie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="2d7a2-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="2d7a2-109">To polecenie tworzy konto magazynu dla nazwy grupy zasobów moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="2d7a2-110">Przykład 2: Tworzenie konta magazynu obiektów BLOB przy użyciu BlobStorage i AccessTier na gorąco</span><span class="sxs-lookup"><span data-stu-id="2d7a2-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="2d7a2-111">To polecenie tworzy konto magazynu obiektów blob z BlobStorage i gorącą AccessTier</span><span class="sxs-lookup"><span data-stu-id="2d7a2-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="2d7a2-112">Przykład 3: Tworzenie konta magazynu za pomocą StorageV2, a następnie Wygeneruj i przypisz tożsamość do magazynu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="2d7a2-113">To polecenie tworzy konto magazynu o rodzaju StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="2d7a2-114">Generuje także i przypisuje tożsamość, która może być używana do zarządzania kluczami kont za pośrednictwem usługi Azure Keys.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="2d7a2-115">Przykład 4: Tworzenie konta magazynu przy użyciu NetworkRuleSet z notacji JSON</span><span class="sxs-lookup"><span data-stu-id="2d7a2-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="2d7a2-116">To polecenie tworzy konto magazynu z właściwością NetworkRuleSet w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="2d7a2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d7a2-117">PARAMETERS</span></span>

### <span data-ttu-id="2d7a2-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="2d7a2-118">-AccessTier</span></span>
<span data-ttu-id="2d7a2-119">Określa warstwę dostępu konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2d7a2-120">Dopuszczalne wartości tego parametru to: gorące i chłodzone.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="2d7a2-121">W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="2d7a2-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="2d7a2-122">Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="2d7a2-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="2d7a2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d7a2-123">-AsJob</span></span>
<span data-ttu-id="2d7a2-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2d7a2-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d7a2-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2d7a2-125">-AssignIdentity</span></span>
<span data-ttu-id="2d7a2-126">Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2d7a2-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2d7a2-127">-CustomDomainName</span></span>
<span data-ttu-id="2d7a2-128">Określa nazwę domeny niestandardowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="2d7a2-129">Wartość domyślna to Storage.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-129">The default value is Storage.</span></span>

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

### <span data-ttu-id="2d7a2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7a2-130">-DefaultProfile</span></span>
<span data-ttu-id="2d7a2-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d7a2-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="2d7a2-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="2d7a2-133">Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="2d7a2-134">-Kind</span><span class="sxs-lookup"><span data-stu-id="2d7a2-134">-Kind</span></span>
<span data-ttu-id="2d7a2-135">Określa rodzaj konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2d7a2-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2d7a2-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d7a2-137">Chowan.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-137">Storage.</span></span> <span data-ttu-id="2d7a2-138">Ogólne konto magazynu, które obsługuje przechowywanie obiektów blob, tabel, kolejek, plików i dysków.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="2d7a2-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-139">StorageV2.</span></span> <span data-ttu-id="2d7a2-140">Konto magazynu ogólnego celu w wersji 2 (GPv2), które obsługuje obiekty blob, tabele, kolejki, pliki i dyski, z zaawansowanymi funkcjami, takimi jak warstwy danych.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="2d7a2-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-141">BlobStorage.</span></span> <span data-ttu-id="2d7a2-142">Konto magazynu obiektów BLOB obsługujące tylko przechowywanie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="2d7a2-143">Wartość domyślna to Storage.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7a2-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2d7a2-144">-Location</span></span>
<span data-ttu-id="2d7a2-145">Określa lokalizację konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-145">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="2d7a2-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d7a2-146">-Name</span></span>
<span data-ttu-id="2d7a2-147">Określa nazwę konta magazynu, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-147">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="2d7a2-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d7a2-148">-NetworkRuleSet</span></span>
<span data-ttu-id="2d7a2-149">NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do ustawiania wartości właściwości sieci, takich jak usługi, które mogą pomijać reguły, oraz sposobu obsługi żądań niezgodnych z żadną określoną regułą.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="2d7a2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7a2-150">-ResourceGroupName</span></span>
<span data-ttu-id="2d7a2-151">Określa nazwę grupy zasobów, w której ma zostać dodane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="2d7a2-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2d7a2-152">-SkuName</span></span>
<span data-ttu-id="2d7a2-153">Określa nazwę SKU konta magazynu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2d7a2-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2d7a2-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d7a2-155">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-155">Standard_LRS.</span></span> <span data-ttu-id="2d7a2-156">Magazyn lokalny-nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="2d7a2-157">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-157">Standard_ZRS.</span></span> <span data-ttu-id="2d7a2-158">Miejsce do magazynowania nadmiarowych stref.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="2d7a2-159">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-159">Standard_GRS.</span></span> <span data-ttu-id="2d7a2-160">Magazyn Geograficznie nadmiarowy.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="2d7a2-161">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-161">Standard_RAGRS.</span></span> <span data-ttu-id="2d7a2-162">Dostęp do odczytu geograficznie zapasowego miejsca.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="2d7a2-163">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-163">Premium_LRS.</span></span> <span data-ttu-id="2d7a2-164">Premium miejsce do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-164">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7a2-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d7a2-165">-Tag</span></span>
<span data-ttu-id="2d7a2-166">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="2d7a2-167">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="2d7a2-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2d7a2-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="2d7a2-168">-UseSubDomain</span></span>
<span data-ttu-id="2d7a2-169">Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-169">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="2d7a2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7a2-170">CommonParameters</span></span>
<span data-ttu-id="2d7a2-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7a2-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7a2-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7a2-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d7a2-173">INPUTS</span></span>

### <span data-ttu-id="2d7a2-174">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7a2-174">System.String</span></span>

### <span data-ttu-id="2d7a2-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d7a2-175">System.Boolean</span></span>

## <span data-ttu-id="2d7a2-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d7a2-176">OUTPUTS</span></span>

### <span data-ttu-id="2d7a2-177">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d7a2-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="2d7a2-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d7a2-178">NOTES</span></span>

## <span data-ttu-id="2d7a2-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d7a2-179">RELATED LINKS</span></span>

[<span data-ttu-id="2d7a2-180">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d7a2-180">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="2d7a2-181">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d7a2-181">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="2d7a2-182">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d7a2-182">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
