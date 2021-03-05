---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 8407cb1f8968d1e7d9e469b4ca3ccd1cb49742a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007105"
---
# <span data-ttu-id="85480-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="85480-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="85480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85480-102">SYNOPSIS</span></span>
<span data-ttu-id="85480-103">Tworzy konfigurowalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="85480-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85480-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85480-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="85480-105">DESCRIPTION</span></span>
<span data-ttu-id="85480-106">Polecenie **cmdlet New-AzSnapshotConfig** tworzy konfigurowalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="85480-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85480-107">EXAMPLES</span></span>

### <span data-ttu-id="85480-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85480-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="85480-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5 GB Standard_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="85480-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="85480-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="85480-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="85480-111">Drugie i trzecie polecenie ustawia ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="85480-112">Ostatnie polecenie pobiera obiekt migawki i tworzy migawkę o nazwie "Migawka01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="85480-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="85480-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="85480-113">Example 2</span></span>

<span data-ttu-id="85480-114">Tworzy konfigurowalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="85480-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="85480-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="85480-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85480-116">PARAMETERS</span></span>

### <span data-ttu-id="85480-117">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="85480-117">-CreateOption</span></span>
<span data-ttu-id="85480-118">Określa, czy to polecenie cmdlet tworzy dysk na komputerze wirtualnym z platformy lub obrazu użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="85480-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="85480-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85480-119">-DefaultProfile</span></span>
<span data-ttu-id="85480-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85480-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85480-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="85480-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="85480-122">Określa obiekt klucza szyfrowania dysku w migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="85480-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="85480-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="85480-124">Określa identyfikator zasobu dla szyfrowania dysku ustawionego do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="85480-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="85480-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="85480-125">-DiskSizeGB</span></span>
<span data-ttu-id="85480-126">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="85480-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="85480-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="85480-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="85480-128">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="85480-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="85480-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="85480-129">-EncryptionType</span></span>
<span data-ttu-id="85480-130">Typ klucza używanego do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="85480-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="85480-131">Dostępne wartości to: 'EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="85480-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="85480-132">- DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="85480-132">-DiskAccessId</span></span>
<span data-ttu-id="85480-133">Pobiera lub ustawia ARM zasobu DiskAccess na przykład w celu używania prywatnych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="85480-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="85480-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="85480-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="85480-135">Zasady dostępu do sieci definiują zasady dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="85480-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="85480-136">Możliwe wartości to: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="85480-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="85480-137">-HyperV Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="85480-137">-HyperVGeneration</span></span>
<span data-ttu-id="85480-138">Generowanie hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="85480-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="85480-139">Dotyczy tylko dyskietek systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="85480-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="85480-140">Dozwolone wartości to V1 i V2.</span><span class="sxs-lookup"><span data-stu-id="85480-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="85480-141">- ImageReference</span><span class="sxs-lookup"><span data-stu-id="85480-141">-ImageReference</span></span>
<span data-ttu-id="85480-142">Określa odwołanie do obrazu w migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="85480-143">— Przyrostowe</span><span class="sxs-lookup"><span data-stu-id="85480-143">-Incremental</span></span>
<span data-ttu-id="85480-144">Określa migawkę przyrostową.</span><span class="sxs-lookup"><span data-stu-id="85480-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="85480-145">Migawki przyrostowe na tym samym dysku zajmują mniej miejsca niż pełne migawki i mogą być rozpraszane.</span><span class="sxs-lookup"><span data-stu-id="85480-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="85480-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="85480-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="85480-147">Określa klucz szyfrowania klucza w migawki.</span><span class="sxs-lookup"><span data-stu-id="85480-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="85480-148">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="85480-148">-Location</span></span>
<span data-ttu-id="85480-149">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="85480-149">Specifies a location.</span></span>

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

### <span data-ttu-id="85480-150">- OsType</span><span class="sxs-lookup"><span data-stu-id="85480-150">-OsType</span></span>
<span data-ttu-id="85480-151">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="85480-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="85480-152">-SKUName</span><span class="sxs-lookup"><span data-stu-id="85480-152">-SkuName</span></span>
<span data-ttu-id="85480-153">Określa nazwę sku konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="85480-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="85480-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="85480-154">-SourceResourceId</span></span>
<span data-ttu-id="85480-155">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="85480-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="85480-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="85480-156">-SourceUri</span></span>
<span data-ttu-id="85480-157">Określa źródłowy Uri.</span><span class="sxs-lookup"><span data-stu-id="85480-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="85480-158">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="85480-158">-StorageAccountId</span></span>
<span data-ttu-id="85480-159">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="85480-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="85480-160">— Tag</span><span class="sxs-lookup"><span data-stu-id="85480-160">-Tag</span></span>
<span data-ttu-id="85480-161">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="85480-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85480-162">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="85480-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85480-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85480-163">-Confirm</span></span>
<span data-ttu-id="85480-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="85480-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85480-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85480-165">-WhatIf</span></span>
<span data-ttu-id="85480-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85480-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85480-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="85480-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85480-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85480-168">CommonParameters</span></span>
<span data-ttu-id="85480-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85480-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85480-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85480-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85480-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85480-171">INPUTS</span></span>

### <span data-ttu-id="85480-172">System.String</span><span class="sxs-lookup"><span data-stu-id="85480-172">System.String</span></span>

### <span data-ttu-id="85480-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="85480-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="85480-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="85480-174">System.Int32</span></span>

### <span data-ttu-id="85480-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="85480-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="85480-176">Microsoft.Azure.Management.Compute.Models.ImageFerence</span><span class="sxs-lookup"><span data-stu-id="85480-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="85480-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="85480-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="85480-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="85480-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="85480-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="85480-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="85480-180">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85480-180">OUTPUTS</span></span>

### <span data-ttu-id="85480-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="85480-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="85480-182">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85480-182">NOTES</span></span>

## <span data-ttu-id="85480-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85480-183">RELATED LINKS</span></span>
