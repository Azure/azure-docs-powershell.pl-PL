---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717473"
---
# <span data-ttu-id="26719-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="26719-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="26719-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26719-102">SYNOPSIS</span></span>
<span data-ttu-id="26719-103">Tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="26719-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26719-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26719-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26719-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26719-105">DESCRIPTION</span></span>
<span data-ttu-id="26719-106">Polecenie cmdlet **New-AzureRmDiskConfig** tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="26719-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="26719-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26719-107">EXAMPLES</span></span>

### <span data-ttu-id="26719-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26719-108">Example 1</span></span>
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

<span data-ttu-id="26719-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="26719-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="26719-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="26719-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="26719-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="26719-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="26719-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="26719-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="26719-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26719-113">PARAMETERS</span></span>

### <span data-ttu-id="26719-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="26719-114">-CreateOption</span></span>
<span data-ttu-id="26719-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="26719-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="26719-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26719-116">-DefaultProfile</span></span>
<span data-ttu-id="26719-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26719-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26719-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="26719-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="26719-119">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="26719-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="26719-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="26719-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="26719-121">Liczba IOPS dozwolonych dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="26719-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="26719-122">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="26719-122">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26719-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="26719-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="26719-124">Przepustowość dozwolona dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="26719-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="26719-125">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="26719-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26719-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="26719-126">-DiskSizeGB</span></span>
<span data-ttu-id="26719-127">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="26719-127">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26719-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="26719-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="26719-129">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="26719-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="26719-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="26719-130">-ImageReference</span></span>
<span data-ttu-id="26719-131">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="26719-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="26719-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="26719-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="26719-133">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="26719-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="26719-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="26719-134">-Location</span></span>
<span data-ttu-id="26719-135">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="26719-135">Specifies a location.</span></span>

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

### <span data-ttu-id="26719-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="26719-136">-OsType</span></span>
<span data-ttu-id="26719-137">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="26719-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="26719-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="26719-138">-SkuName</span></span>
<span data-ttu-id="26719-139">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="26719-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="26719-140">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="26719-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="26719-141">UltraSSD_LRS można użyć tylko z wartością pustą dla parametru usługi.</span><span class="sxs-lookup"><span data-stu-id="26719-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26719-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="26719-142">-SourceResourceId</span></span>
<span data-ttu-id="26719-143">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="26719-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="26719-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="26719-144">-SourceUri</span></span>
<span data-ttu-id="26719-145">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="26719-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="26719-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="26719-146">-StorageAccountId</span></span>
<span data-ttu-id="26719-147">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="26719-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="26719-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="26719-148">-Tag</span></span>
<span data-ttu-id="26719-149">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="26719-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26719-150">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="26719-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26719-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="26719-151">-Zone</span></span>
<span data-ttu-id="26719-152">Określa listę stref logicznych dla dysku.</span><span class="sxs-lookup"><span data-stu-id="26719-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="26719-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26719-153">-Confirm</span></span>
<span data-ttu-id="26719-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26719-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26719-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26719-155">-WhatIf</span></span>
<span data-ttu-id="26719-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26719-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26719-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26719-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26719-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26719-158">CommonParameters</span></span>
<span data-ttu-id="26719-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26719-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26719-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26719-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26719-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26719-161">INPUTS</span></span>

### <span data-ttu-id="26719-162">System. String</span><span class="sxs-lookup"><span data-stu-id="26719-162">System.String</span></span>

### <span data-ttu-id="26719-163">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="26719-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26719-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="26719-164">System.Int32</span></span>

### <span data-ttu-id="26719-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="26719-165">System.String[]</span></span>

### <span data-ttu-id="26719-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26719-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26719-167">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="26719-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="26719-168">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26719-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="26719-169">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="26719-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="26719-170">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="26719-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="26719-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26719-171">OUTPUTS</span></span>

### <span data-ttu-id="26719-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="26719-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="26719-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26719-173">NOTES</span></span>

## <span data-ttu-id="26719-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26719-174">RELATED LINKS</span></span>
