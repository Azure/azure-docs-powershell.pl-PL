---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 2989a5be6ef6eee137f296ab1379931070082fe9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894993"
---
# <span data-ttu-id="794e2-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="794e2-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="794e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="794e2-102">SYNOPSIS</span></span>
<span data-ttu-id="794e2-103">Umożliwia utworzenie obiektu migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="794e2-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="794e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="794e2-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="794e2-105">DESCRIPTION</span></span>
<span data-ttu-id="794e2-106">Polecenie cmdlet **New-AzSnapshotConfig** tworzy obiekt o konfigurowalnej migawce.</span><span class="sxs-lookup"><span data-stu-id="794e2-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="794e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="794e2-107">EXAMPLES</span></span>

### <span data-ttu-id="794e2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="794e2-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="794e2-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="794e2-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="794e2-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="794e2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="794e2-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="794e2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="794e2-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="794e2-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="794e2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="794e2-113">PARAMETERS</span></span>

### <span data-ttu-id="794e2-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="794e2-114">-CreateOption</span></span>
<span data-ttu-id="794e2-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="794e2-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="794e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794e2-116">-DefaultProfile</span></span>
<span data-ttu-id="794e2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="794e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="794e2-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="794e2-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="794e2-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="794e2-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="794e2-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="794e2-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="794e2-121">Określa identyfikator zasobu zestawu ustawień szyfrowania dysku, który ma być używany do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="794e2-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="794e2-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="794e2-122">-DiskSizeGB</span></span>
<span data-ttu-id="794e2-123">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="794e2-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="794e2-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="794e2-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="794e2-125">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="794e2-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="794e2-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="794e2-126">-EncryptionType</span></span>
<span data-ttu-id="794e2-127">Typ klucza służący do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="794e2-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="794e2-128">Dostępne wartości: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="794e2-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="794e2-129">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="794e2-129">-HyperVGeneration</span></span>
<span data-ttu-id="794e2-130">Generowanie funkcji hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="794e2-130">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="794e2-131">Dotyczy tylko dysków z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="794e2-131">Applicable to OS disks only.</span></span>  <span data-ttu-id="794e2-132">Dozwolone wartości to V1 i v2.</span><span class="sxs-lookup"><span data-stu-id="794e2-132">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="794e2-133">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="794e2-133">-ImageReference</span></span>
<span data-ttu-id="794e2-134">Określa odwołanie do obrazu w migawce.</span><span class="sxs-lookup"><span data-stu-id="794e2-134">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="794e2-135">-Przyrostowy</span><span class="sxs-lookup"><span data-stu-id="794e2-135">-Incremental</span></span>
<span data-ttu-id="794e2-136">Określa migawkę przyrostową.</span><span class="sxs-lookup"><span data-stu-id="794e2-136">Specifies an incremental snapshot.</span></span> <span data-ttu-id="794e2-137">Przyrostowe migawki na tym samym dysku zajmują mniej miejsca niż pełne migawki i można je powiększyć.</span><span class="sxs-lookup"><span data-stu-id="794e2-137">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794e2-138">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="794e2-138">-KeyEncryptionKey</span></span>
<span data-ttu-id="794e2-139">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="794e2-139">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="794e2-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="794e2-140">-Location</span></span>
<span data-ttu-id="794e2-141">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="794e2-141">Specifies a location.</span></span>

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

### <span data-ttu-id="794e2-142">-OsType</span><span class="sxs-lookup"><span data-stu-id="794e2-142">-OsType</span></span>
<span data-ttu-id="794e2-143">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="794e2-143">Specifies the OS type.</span></span>

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

### <span data-ttu-id="794e2-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="794e2-144">-SkuName</span></span>
<span data-ttu-id="794e2-145">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="794e2-145">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="794e2-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="794e2-146">-SourceResourceId</span></span>
<span data-ttu-id="794e2-147">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="794e2-147">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="794e2-148">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="794e2-148">-SourceUri</span></span>
<span data-ttu-id="794e2-149">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="794e2-149">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="794e2-150">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="794e2-150">-StorageAccountId</span></span>
<span data-ttu-id="794e2-151">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="794e2-151">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="794e2-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="794e2-152">-Tag</span></span>
<span data-ttu-id="794e2-153">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="794e2-153">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="794e2-154">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="794e2-154">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="794e2-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="794e2-155">-Confirm</span></span>
<span data-ttu-id="794e2-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="794e2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="794e2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794e2-157">-WhatIf</span></span>
<span data-ttu-id="794e2-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="794e2-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="794e2-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="794e2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="794e2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794e2-160">CommonParameters</span></span>
<span data-ttu-id="794e2-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="794e2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794e2-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="794e2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794e2-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="794e2-163">INPUTS</span></span>

### <span data-ttu-id="794e2-164">System. String</span><span class="sxs-lookup"><span data-stu-id="794e2-164">System.String</span></span>

### <span data-ttu-id="794e2-165">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="794e2-165">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="794e2-166">System. Int32</span><span class="sxs-lookup"><span data-stu-id="794e2-166">System.Int32</span></span>

### <span data-ttu-id="794e2-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="794e2-167">System.Collections.Hashtable</span></span>

### <span data-ttu-id="794e2-168">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="794e2-168">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="794e2-169">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="794e2-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="794e2-170">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="794e2-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="794e2-171">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="794e2-171">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="794e2-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="794e2-172">OUTPUTS</span></span>

### <span data-ttu-id="794e2-173">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="794e2-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="794e2-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="794e2-174">NOTES</span></span>

## <span data-ttu-id="794e2-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="794e2-175">RELATED LINKS</span></span>
