---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 70ee169903ca70b539e8eda2043ffcd0fd2928c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554203"
---
# <span data-ttu-id="b392a-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b392a-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="b392a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b392a-102">SYNOPSIS</span></span>
<span data-ttu-id="b392a-103">Tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="b392a-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b392a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b392a-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b392a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b392a-105">DESCRIPTION</span></span>
<span data-ttu-id="b392a-106">Polecenie cmdlet **New-AzureRmDiskConfig** tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="b392a-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="b392a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b392a-107">EXAMPLES</span></span>

### <span data-ttu-id="b392a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b392a-108">Example 1</span></span>
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

<span data-ttu-id="b392a-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b392a-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b392a-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="b392a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b392a-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="b392a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="b392a-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b392a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b392a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b392a-113">PARAMETERS</span></span>

### <span data-ttu-id="b392a-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="b392a-114">-CreateOption</span></span>
<span data-ttu-id="b392a-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="b392a-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b392a-116">-DefaultProfile</span></span>
<span data-ttu-id="b392a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b392a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b392a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b392a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="b392a-119">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="b392a-119">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b392a-120">-DiskSizeGB</span></span>
<span data-ttu-id="b392a-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="b392a-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b392a-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b392a-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="b392a-123">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="b392a-124">-ImageReference</span></span>
<span data-ttu-id="b392a-125">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="b392a-125">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b392a-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="b392a-127">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="b392a-127">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b392a-128">-Location</span></span>
<span data-ttu-id="b392a-129">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="b392a-129">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="b392a-130">-OsType</span></span>
<span data-ttu-id="b392a-131">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="b392a-131">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b392a-132">-SkuName</span></span>
<span data-ttu-id="b392a-133">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b392a-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b392a-134">-SourceResourceId</span></span>
<span data-ttu-id="b392a-135">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="b392a-135">Specifies the  source resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b392a-136">-SourceUri</span></span>
<span data-ttu-id="b392a-137">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="b392a-137">Specifies the source Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b392a-138">-StorageAccountId</span></span>
<span data-ttu-id="b392a-139">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b392a-139">Specifies the storage account ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="b392a-140">-Tag</span></span>
<span data-ttu-id="b392a-141">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="b392a-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="b392a-142">-Zone</span></span>
<span data-ttu-id="b392a-143">Określa listę stref logicznych dla dysku.</span><span class="sxs-lookup"><span data-stu-id="b392a-143">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b392a-144">-Confirm</span></span>
<span data-ttu-id="b392a-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b392a-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b392a-146">-WhatIf</span></span>
<span data-ttu-id="b392a-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b392a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b392a-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b392a-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b392a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b392a-149">CommonParameters</span></span>
<span data-ttu-id="b392a-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b392a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b392a-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b392a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b392a-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b392a-152">INPUTS</span></span>

### <span data-ttu-id="b392a-153">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="b392a-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="b392a-154">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = obojętny, PublicKeyToken = b77a5c561934e089]] system. String system. Collections. Hashtable system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutralne, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. models. KeyVaultAndSecretReference. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="b392a-154">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b392a-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b392a-155">OUTPUTS</span></span>

### <span data-ttu-id="b392a-156">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="b392a-156">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="b392a-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b392a-157">NOTES</span></span>

## <span data-ttu-id="b392a-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b392a-158">RELATED LINKS</span></span>

