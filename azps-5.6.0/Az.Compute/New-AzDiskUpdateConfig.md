---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957585"
---
# <span data-ttu-id="ae702-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ae702-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="ae702-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae702-102">SYNOPSIS</span></span>
<span data-ttu-id="ae702-103">Tworzy konfigurowalny obiekt aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="ae702-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae702-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae702-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae702-105">DESCRIPTION</span></span>
<span data-ttu-id="ae702-106">Polecenie **cmdlet New-AzCmUpdateConfig** tworzy konfigurowalny obiekt aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="ae702-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae702-107">EXAMPLES</span></span>

### <span data-ttu-id="ae702-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae702-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="ae702-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10 GB Premium_LRS typie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ae702-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ae702-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="ae702-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ae702-111">Drugie i trzecie polecenia ustawiają ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ae702-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk nazwą "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="ae702-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ae702-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ae702-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ae702-114">To polecenie aktualizuje istniejący dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów001" do rozmiaru dysku 10 GB.</span><span class="sxs-lookup"><span data-stu-id="ae702-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ae702-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae702-115">PARAMETERS</span></span>

### <span data-ttu-id="ae702-116">- PodsycanieBłędów</span><span class="sxs-lookup"><span data-stu-id="ae702-116">-BurstingEnabled</span></span>
<span data-ttu-id="ae702-117">Umożliwia seria danych wykraczających poza aprowizowany element docelowy wydajności dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="ae702-118">Rozsyłanie jest domyślnie wyłączone.</span><span class="sxs-lookup"><span data-stu-id="ae702-118">Bursting is disabled by default.</span></span> <span data-ttu-id="ae702-119">Nie dotyczy dysków Ultra.</span><span class="sxs-lookup"><span data-stu-id="ae702-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="ae702-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae702-120">-DefaultProfile</span></span>
<span data-ttu-id="ae702-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae702-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae702-122">- DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="ae702-122">-DiskAccessId</span></span>
<span data-ttu-id="ae702-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="ae702-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="ae702-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ae702-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="ae702-125">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ae702-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ae702-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ae702-127">Określa identyfikator zasobu dla szyfrowania dysku ustawionego do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="ae702-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="ae702-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="ae702-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="ae702-129">Całkowita liczba usług IOPS, które będą dozwolone dla wszystkich maszyn wirtualnych, chowają dysk udostępniony jako ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="ae702-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="ae702-130">Jedna operacja może przenosić od 4k do 256 tys. bajtów.</span><span class="sxs-lookup"><span data-stu-id="ae702-130">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae702-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="ae702-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="ae702-132">Liczba dozwolonych w programie IOPS dla tego dysku; można ustawić tylko dla dysków UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="ae702-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ae702-133">Jedna operacja może przenosić od 4k do 256 tys. bajtów.</span><span class="sxs-lookup"><span data-stu-id="ae702-133">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="ae702-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ae702-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="ae702-135">Całkowita przepływność (MBps), która będzie dozwolona dla wszystkich maszyn wirtualnych, a także na dysku udostępnionym jako ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="ae702-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="ae702-136">Program MBps oznacza miliony bajtów na sekundę — w tym przypadku MB używa notacji ISO, czyli potęg o pojemności 10.</span><span class="sxs-lookup"><span data-stu-id="ae702-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae702-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="ae702-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="ae702-138">Przepustowość dozwolona dla tego dysku; można ustawić tylko dla dysków UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="ae702-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ae702-139">Program MBps oznacza miliony bajtów na sekundę — w tym przypadku MB używa notacji ISO, czyli potęg o pojemności 10.</span><span class="sxs-lookup"><span data-stu-id="ae702-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="ae702-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ae702-140">-DiskSizeGB</span></span>
<span data-ttu-id="ae702-141">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="ae702-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ae702-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ae702-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ae702-143">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="ae702-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ae702-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="ae702-144">-EncryptionType</span></span>
<span data-ttu-id="ae702-145">Typ klucza używanego do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="ae702-146">Dostępne wartości to: 'EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="ae702-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="ae702-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ae702-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="ae702-148">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ae702-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="ae702-149">-MaxSharesCount</span></span>
<span data-ttu-id="ae702-150">Maksymalna liczba maszyn wirtualnych, które mogą dołączać do dysku w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="ae702-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="ae702-151">Wartość większa niż jedna wskazuje dysk, który może być jednocześnie montowany na wielu maszynych wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="ae702-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae702-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae702-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="ae702-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="ae702-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="ae702-154">- OsType</span><span class="sxs-lookup"><span data-stu-id="ae702-154">-OsType</span></span>
<span data-ttu-id="ae702-155">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="ae702-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ae702-156">-SKUName</span><span class="sxs-lookup"><span data-stu-id="ae702-156">-SkuName</span></span>
<span data-ttu-id="ae702-157">Określa nazwę sku konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ae702-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="ae702-158">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="ae702-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="ae702-159">UltraSSD_LRS można używać tylko z wartością pustą dla parametru CreateOption.</span><span class="sxs-lookup"><span data-stu-id="ae702-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="ae702-160">— Tag</span><span class="sxs-lookup"><span data-stu-id="ae702-160">-Tag</span></span>
<span data-ttu-id="ae702-161">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="ae702-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae702-162">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ae702-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae702-163">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="ae702-163">-Tier</span></span>
<span data-ttu-id="ae702-164">Warstwa wydajności dysku.</span><span class="sxs-lookup"><span data-stu-id="ae702-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="ae702-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae702-165">-Confirm</span></span>
<span data-ttu-id="ae702-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae702-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae702-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae702-167">-WhatIf</span></span>
<span data-ttu-id="ae702-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae702-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae702-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae702-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae702-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae702-170">CommonParameters</span></span>
<span data-ttu-id="ae702-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae702-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae702-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae702-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae702-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae702-173">INPUTS</span></span>

### <span data-ttu-id="ae702-174">System.String</span><span class="sxs-lookup"><span data-stu-id="ae702-174">System.String</span></span>

### <span data-ttu-id="ae702-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ae702-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ae702-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ae702-176">System.Int32</span></span>

### <span data-ttu-id="ae702-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae702-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ae702-178">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ae702-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ae702-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="ae702-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ae702-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="ae702-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ae702-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae702-181">OUTPUTS</span></span>

### <span data-ttu-id="ae702-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ae702-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="ae702-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae702-183">NOTES</span></span>

## <span data-ttu-id="ae702-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae702-184">RELATED LINKS</span></span>
