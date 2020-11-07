---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: b2c922a1dcce683636d61b68c66ab8cfb82535c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544504"
---
# <span data-ttu-id="a0859-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a0859-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="a0859-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0859-102">SYNOPSIS</span></span>
<span data-ttu-id="a0859-103">Tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="a0859-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0859-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0859-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0859-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0859-105">DESCRIPTION</span></span>
<span data-ttu-id="a0859-106">Polecenie cmdlet **New-AzureRmDiskConfig** tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="a0859-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="a0859-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0859-107">EXAMPLES</span></span>

### <span data-ttu-id="a0859-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0859-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="a0859-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0859-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a0859-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a0859-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a0859-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="a0859-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="a0859-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a0859-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a0859-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0859-113">PARAMETERS</span></span>

### <span data-ttu-id="a0859-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="a0859-114">-CreateOption</span></span>
<span data-ttu-id="a0859-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="a0859-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a0859-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a0859-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="a0859-117">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="a0859-117">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="a0859-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a0859-118">-DiskSizeGB</span></span>
<span data-ttu-id="a0859-119">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="a0859-119">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a0859-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a0859-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a0859-121">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a0859-121">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a0859-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a0859-122">-ImageReference</span></span>
<span data-ttu-id="a0859-123">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="a0859-123">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="a0859-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a0859-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="a0859-125">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="a0859-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="a0859-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0859-126">-Location</span></span>
<span data-ttu-id="a0859-127">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="a0859-127">Specifies a location.</span></span>

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

### <span data-ttu-id="a0859-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="a0859-128">-OsType</span></span>
<span data-ttu-id="a0859-129">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="a0859-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a0859-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a0859-130">-SkuName</span></span>
<span data-ttu-id="a0859-131">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0859-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a0859-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a0859-132">-SourceResourceId</span></span>
<span data-ttu-id="a0859-133">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="a0859-133">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="a0859-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a0859-134">-SourceUri</span></span>
<span data-ttu-id="a0859-135">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="a0859-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a0859-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a0859-136">-StorageAccountId</span></span>
<span data-ttu-id="a0859-137">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0859-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a0859-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0859-138">-Tag</span></span>
<span data-ttu-id="a0859-139">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="a0859-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="a0859-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0859-140">-Confirm</span></span>
<span data-ttu-id="a0859-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0859-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0859-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0859-142">-WhatIf</span></span>
<span data-ttu-id="a0859-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0859-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0859-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0859-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0859-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0859-145">CommonParameters</span></span>
<span data-ttu-id="a0859-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0859-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0859-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0859-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0859-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0859-148">INPUTS</span></span>

### <span data-ttu-id="a0859-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="a0859-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="a0859-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = obojętny, PublicKeyToken = b77a5c561934e089]] system. String system. Collections. Hashtable system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutralne, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. models. KeyVaultAndSecretReference. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a0859-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a0859-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0859-151">OUTPUTS</span></span>

### <span data-ttu-id="a0859-152">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="a0859-152">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="a0859-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0859-153">NOTES</span></span>

## <span data-ttu-id="a0859-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0859-154">RELATED LINKS</span></span>
