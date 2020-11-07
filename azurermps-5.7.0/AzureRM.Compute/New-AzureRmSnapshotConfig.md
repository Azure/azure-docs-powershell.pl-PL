---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: ee3dd849a8f3877ac19ce86a7257d28fc18575c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717225"
---
# <span data-ttu-id="d2b07-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d2b07-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="d2b07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2b07-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b07-103">Umożliwia utworzenie obiektu migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="d2b07-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2b07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2b07-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2b07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2b07-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b07-106">Polecenie cmdlet **New-AzureRmSnapshotConfig** tworzy obiekt o konfigurowalnej migawce.</span><span class="sxs-lookup"><span data-stu-id="d2b07-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="d2b07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2b07-107">EXAMPLES</span></span>

### <span data-ttu-id="d2b07-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2b07-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="d2b07-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2b07-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d2b07-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="d2b07-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d2b07-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="d2b07-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="d2b07-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d2b07-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d2b07-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2b07-113">PARAMETERS</span></span>

### <span data-ttu-id="d2b07-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="d2b07-114">-CreateOption</span></span>
<span data-ttu-id="d2b07-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="d2b07-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d2b07-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="d2b07-117">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="d2b07-117">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d2b07-118">-DiskSizeGB</span></span>
<span data-ttu-id="d2b07-119">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="d2b07-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="d2b07-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="d2b07-121">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="d2b07-121">Enable encryption settings.</span></span>

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

### <span data-ttu-id="d2b07-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="d2b07-122">-ImageReference</span></span>
<span data-ttu-id="d2b07-123">Określa odwołanie do obrazu w migawce.</span><span class="sxs-lookup"><span data-stu-id="d2b07-123">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d2b07-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="d2b07-125">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="d2b07-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d2b07-126">-Location</span></span>
<span data-ttu-id="d2b07-127">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="d2b07-127">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="d2b07-128">-OsType</span></span>
<span data-ttu-id="d2b07-129">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="d2b07-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d2b07-130">-SkuName</span></span>
<span data-ttu-id="d2b07-131">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2b07-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d2b07-132">-SourceResourceId</span></span>
<span data-ttu-id="d2b07-133">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="d2b07-133">Specifies the source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="d2b07-134">-SourceUri</span></span>
<span data-ttu-id="d2b07-135">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="d2b07-135">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d2b07-136">-StorageAccountId</span></span>
<span data-ttu-id="d2b07-137">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2b07-137">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2b07-138">-Tag</span></span>
<span data-ttu-id="d2b07-139">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="d2b07-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2b07-140">-Confirm</span></span>
<span data-ttu-id="d2b07-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2b07-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2b07-142">-WhatIf</span></span>
<span data-ttu-id="d2b07-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2b07-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2b07-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2b07-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b07-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b07-145">CommonParameters</span></span>
<span data-ttu-id="d2b07-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b07-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b07-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b07-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b07-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2b07-148">INPUTS</span></span>

### <span data-ttu-id="d2b07-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="d2b07-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="d2b07-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = obojętny, PublicKeyToken = b77a5c561934e089]] system. String system. Collections. Hashtable system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutralne, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. models. KeyVaultAndSecretReference. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="d2b07-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="d2b07-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2b07-151">OUTPUTS</span></span>

### <span data-ttu-id="d2b07-152">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="d2b07-152">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="d2b07-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2b07-153">NOTES</span></span>

## <span data-ttu-id="d2b07-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2b07-154">RELATED LINKS</span></span>

