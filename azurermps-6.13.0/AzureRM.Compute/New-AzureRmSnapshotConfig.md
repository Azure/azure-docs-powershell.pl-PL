---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 2050536a39c8ebcd5a1269709d25af100cc251b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717472"
---
# <span data-ttu-id="7823d-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7823d-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="7823d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7823d-102">SYNOPSIS</span></span>
<span data-ttu-id="7823d-103">Umożliwia utworzenie obiektu migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="7823d-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7823d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7823d-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7823d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7823d-105">DESCRIPTION</span></span>
<span data-ttu-id="7823d-106">Polecenie cmdlet **New-AzureRmSnapshotConfig** tworzy obiekt o konfigurowalnej migawce.</span><span class="sxs-lookup"><span data-stu-id="7823d-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="7823d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7823d-107">EXAMPLES</span></span>

### <span data-ttu-id="7823d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7823d-108">Example 1</span></span>
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

<span data-ttu-id="7823d-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7823d-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="7823d-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="7823d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="7823d-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="7823d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="7823d-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7823d-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7823d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7823d-113">PARAMETERS</span></span>

### <span data-ttu-id="7823d-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="7823d-114">-CreateOption</span></span>
<span data-ttu-id="7823d-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="7823d-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="7823d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7823d-116">-DefaultProfile</span></span>
<span data-ttu-id="7823d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7823d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7823d-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7823d-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="7823d-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="7823d-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="7823d-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7823d-120">-DiskSizeGB</span></span>
<span data-ttu-id="7823d-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="7823d-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7823d-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="7823d-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="7823d-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="7823d-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="7823d-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="7823d-124">-ImageReference</span></span>
<span data-ttu-id="7823d-125">Określa odwołanie do obrazu w migawce.</span><span class="sxs-lookup"><span data-stu-id="7823d-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="7823d-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7823d-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="7823d-127">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="7823d-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="7823d-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7823d-128">-Location</span></span>
<span data-ttu-id="7823d-129">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="7823d-129">Specifies a location.</span></span>

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

### <span data-ttu-id="7823d-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="7823d-130">-OsType</span></span>
<span data-ttu-id="7823d-131">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="7823d-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="7823d-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7823d-132">-SkuName</span></span>
<span data-ttu-id="7823d-133">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7823d-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="7823d-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7823d-134">-SourceResourceId</span></span>
<span data-ttu-id="7823d-135">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="7823d-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="7823d-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7823d-136">-SourceUri</span></span>
<span data-ttu-id="7823d-137">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="7823d-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="7823d-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7823d-138">-StorageAccountId</span></span>
<span data-ttu-id="7823d-139">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7823d-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="7823d-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="7823d-140">-Tag</span></span>
<span data-ttu-id="7823d-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7823d-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7823d-142">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7823d-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7823d-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7823d-143">-Confirm</span></span>
<span data-ttu-id="7823d-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7823d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7823d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7823d-145">-WhatIf</span></span>
<span data-ttu-id="7823d-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7823d-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7823d-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7823d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7823d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7823d-148">CommonParameters</span></span>
<span data-ttu-id="7823d-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7823d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7823d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7823d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7823d-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7823d-151">INPUTS</span></span>

### <span data-ttu-id="7823d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7823d-152">System.String</span></span>

### <span data-ttu-id="7823d-153">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="7823d-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7823d-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7823d-154">System.Int32</span></span>

### <span data-ttu-id="7823d-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7823d-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7823d-156">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="7823d-156">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="7823d-157">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7823d-157">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7823d-158">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="7823d-158">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="7823d-159">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="7823d-159">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="7823d-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7823d-160">OUTPUTS</span></span>

### <span data-ttu-id="7823d-161">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="7823d-161">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="7823d-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7823d-162">NOTES</span></span>

## <span data-ttu-id="7823d-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7823d-163">RELATED LINKS</span></span>
