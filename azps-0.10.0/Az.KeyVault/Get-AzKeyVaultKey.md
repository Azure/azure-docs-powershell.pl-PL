---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891293"
---
# <span data-ttu-id="b02a3-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b02a3-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="b02a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b02a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b02a3-103">Pobiera klucze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b02a3-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="b02a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b02a3-104">SYNTAX</span></span>

### <span data-ttu-id="b02a3-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b02a3-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b02a3-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="b02a3-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b02a3-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="b02a3-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b02a3-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="b02a3-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b02a3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b02a3-109">DESCRIPTION</span></span>
<span data-ttu-id="b02a3-110">Polecenie cmdlet **Get-AzKeyVaultKey** pobiera klucze magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b02a3-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="b02a3-111">To polecenie cmdlet umożliwia pobieranie określonego pakietu **Microsoft. Azure. Commands. Key. MODELES** lub lista wszystkich obiektów **pakietu** kluczy w magazynie kluczy lub według wersji.</span><span class="sxs-lookup"><span data-stu-id="b02a3-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="b02a3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b02a3-112">EXAMPLES</span></span>

### <span data-ttu-id="b02a3-113">Przykład 1. pobieranie wszystkich kluczy w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="b02a3-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="b02a3-114">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b02a3-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="b02a3-115">Przykład 2: uzyskiwanie bieżącej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="b02a3-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="b02a3-116">To polecenie pobiera aktualną wersję klucza o nazwie ITPfx w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b02a3-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="b02a3-117">Przykład 3: pobieranie wszystkich wersji klucza</span><span class="sxs-lookup"><span data-stu-id="b02a3-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="b02a3-118">To polecenie pobiera wszystkie wersje klucza o nazwie ITPfx w kluczu vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="b02a3-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="b02a3-119">Przykład 4: uzyskiwanie określonej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="b02a3-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="b02a3-120">To polecenie pobiera określoną wersję klucza o nazwie ITPfx w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b02a3-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="b02a3-121">Po uruchomieniu tego polecenia możesz sprawdzić różne właściwości klucza, przechodząc do obiektu $Key.</span><span class="sxs-lookup"><span data-stu-id="b02a3-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="b02a3-122">Przykład 5: Uzyskaj wszystkie klucze, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b02a3-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="b02a3-123">To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b02a3-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="b02a3-124">Przykład 6: Pobiera klucze ITPfx, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b02a3-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="b02a3-125">To polecenie pobiera klucze ITPfx, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b02a3-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="b02a3-126">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="b02a3-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="b02a3-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b02a3-127">PARAMETERS</span></span>

### <span data-ttu-id="b02a3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02a3-128">-DefaultProfile</span></span>
<span data-ttu-id="b02a3-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b02a3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02a3-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="b02a3-130">-IncludeVersions</span></span>
<span data-ttu-id="b02a3-131">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza.</span><span class="sxs-lookup"><span data-stu-id="b02a3-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="b02a3-132">Bieżąca wersja klucza to pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="b02a3-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="b02a3-133">W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .</span><span class="sxs-lookup"><span data-stu-id="b02a3-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="b02a3-134">Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera bieżącą wersję klucza o określonej *nazwie*.</span><span class="sxs-lookup"><span data-stu-id="b02a3-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02a3-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b02a3-135">-InRemovedState</span></span>
<span data-ttu-id="b02a3-136">Określa, czy w wyniku mają być pokazywane uprzednio usunięte klucze.</span><span class="sxs-lookup"><span data-stu-id="b02a3-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02a3-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b02a3-137">-Name</span></span>
<span data-ttu-id="b02a3-138">Określa nazwę pakietu kluczy, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="b02a3-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02a3-139">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b02a3-139">-VaultName</span></span>
<span data-ttu-id="b02a3-140">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="b02a3-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="b02a3-141">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i wybrane środowisko.</span><span class="sxs-lookup"><span data-stu-id="b02a3-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="b02a3-142">-Version</span><span class="sxs-lookup"><span data-stu-id="b02a3-142">-Version</span></span>
<span data-ttu-id="b02a3-143">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="b02a3-143">Specifies the key version.</span></span>
<span data-ttu-id="b02a3-144">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="b02a3-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02a3-145">CommonParameters</span></span>
<span data-ttu-id="b02a3-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02a3-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02a3-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02a3-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b02a3-148">INPUTS</span></span>

### <span data-ttu-id="b02a3-149">Ciąg</span><span class="sxs-lookup"><span data-stu-id="b02a3-149">String</span></span>

## <span data-ttu-id="b02a3-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b02a3-150">OUTPUTS</span></span>

### <span data-ttu-id="b02a3-151">Lista<Microsoft. Azure. Commands.. modele. KeyIdentityItem>, Microsoft. Azure. Commands. platforming. models. DeletedKeyIdentityItem, lista<Microsoft. Azure. Commands. Modeling. modele.>, Microsoft. Azure. Commands. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="b02a3-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="b02a3-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b02a3-152">NOTES</span></span>

## <span data-ttu-id="b02a3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b02a3-153">RELATED LINKS</span></span>

[<span data-ttu-id="b02a3-154">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b02a3-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="b02a3-155">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b02a3-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="b02a3-156">Cofanie — AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b02a3-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="b02a3-157">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="b02a3-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

