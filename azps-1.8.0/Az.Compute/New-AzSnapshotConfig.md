---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 293e894704509fe1b869ca23bd726c49f400de48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710275"
---
# <span data-ttu-id="dc099-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="dc099-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="dc099-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc099-102">SYNOPSIS</span></span>
<span data-ttu-id="dc099-103">Umożliwia utworzenie obiektu migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="dc099-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="dc099-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc099-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc099-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc099-105">DESCRIPTION</span></span>
<span data-ttu-id="dc099-106">Polecenie cmdlet **New-AzSnapshotConfig** tworzy obiekt o konfigurowalnej migawce.</span><span class="sxs-lookup"><span data-stu-id="dc099-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="dc099-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc099-107">EXAMPLES</span></span>

### <span data-ttu-id="dc099-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc099-108">Example 1</span></span>
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

<span data-ttu-id="dc099-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dc099-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="dc099-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="dc099-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="dc099-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="dc099-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="dc099-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="dc099-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dc099-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc099-113">PARAMETERS</span></span>

### <span data-ttu-id="dc099-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="dc099-114">-CreateOption</span></span>
<span data-ttu-id="dc099-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="dc099-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="dc099-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc099-116">-DefaultProfile</span></span>
<span data-ttu-id="dc099-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc099-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc099-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="dc099-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="dc099-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="dc099-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="dc099-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="dc099-120">-DiskSizeGB</span></span>
<span data-ttu-id="dc099-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="dc099-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="dc099-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="dc099-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="dc099-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="dc099-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="dc099-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="dc099-124">-HyperVGeneration</span></span>
<span data-ttu-id="dc099-125">Generowanie funkcji hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc099-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="dc099-126">Dotyczy tylko dysków z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="dc099-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="dc099-127">Dozwolone wartości to V1 i v2.</span><span class="sxs-lookup"><span data-stu-id="dc099-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="dc099-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="dc099-128">-ImageReference</span></span>
<span data-ttu-id="dc099-129">Określa odwołanie do obrazu w migawce.</span><span class="sxs-lookup"><span data-stu-id="dc099-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="dc099-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="dc099-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="dc099-131">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="dc099-131">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="dc099-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dc099-132">-Location</span></span>
<span data-ttu-id="dc099-133">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="dc099-133">Specifies a location.</span></span>

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

### <span data-ttu-id="dc099-134">-OsType</span><span class="sxs-lookup"><span data-stu-id="dc099-134">-OsType</span></span>
<span data-ttu-id="dc099-135">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="dc099-135">Specifies the OS type.</span></span>

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

### <span data-ttu-id="dc099-136">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dc099-136">-SkuName</span></span>
<span data-ttu-id="dc099-137">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dc099-137">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="dc099-138">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="dc099-138">-SourceResourceId</span></span>
<span data-ttu-id="dc099-139">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="dc099-139">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="dc099-140">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="dc099-140">-SourceUri</span></span>
<span data-ttu-id="dc099-141">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="dc099-141">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="dc099-142">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dc099-142">-StorageAccountId</span></span>
<span data-ttu-id="dc099-143">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dc099-143">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="dc099-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc099-144">-Tag</span></span>
<span data-ttu-id="dc099-145">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="dc099-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dc099-146">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="dc099-146">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dc099-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc099-147">-Confirm</span></span>
<span data-ttu-id="dc099-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc099-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc099-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc099-149">-WhatIf</span></span>
<span data-ttu-id="dc099-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc099-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc099-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc099-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc099-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc099-152">CommonParameters</span></span>
<span data-ttu-id="dc099-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc099-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc099-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc099-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc099-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc099-155">INPUTS</span></span>

### <span data-ttu-id="dc099-156">System. String</span><span class="sxs-lookup"><span data-stu-id="dc099-156">System.String</span></span>

### <span data-ttu-id="dc099-157">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="dc099-157">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dc099-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dc099-158">System.Int32</span></span>

### <span data-ttu-id="dc099-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc099-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dc099-160">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="dc099-160">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="dc099-161">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dc099-161">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dc099-162">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="dc099-162">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="dc099-163">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="dc099-163">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="dc099-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc099-164">OUTPUTS</span></span>

### <span data-ttu-id="dc099-165">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="dc099-165">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="dc099-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc099-166">NOTES</span></span>

## <span data-ttu-id="dc099-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc099-167">RELATED LINKS</span></span>
