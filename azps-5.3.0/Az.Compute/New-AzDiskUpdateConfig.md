---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504084"
---
# <span data-ttu-id="ca6f6-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ca6f6-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="ca6f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6f6-103">Tworzy obiekt konfigurowalnej aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="ca6f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca6f6-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca6f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ca6f6-106">Polecenie cmdlet **New-AzDiskUpdateConfig** tworzy konfigurowalny obiekt aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="ca6f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca6f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ca6f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca6f6-108">Example 1</span></span>
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

<span data-ttu-id="ca6f6-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ca6f6-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ca6f6-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ca6f6-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ca6f6-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ca6f6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ca6f6-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ca6f6-114">To polecenie aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ca6f6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca6f6-115">PARAMETERS</span></span>

### <span data-ttu-id="ca6f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6f6-116">-DefaultProfile</span></span>
<span data-ttu-id="ca6f6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca6f6-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="ca6f6-118">-DiskAccessId</span></span>
<span data-ttu-id="ca6f6-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="ca6f6-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="ca6f6-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ca6f6-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="ca6f6-121">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ca6f6-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ca6f6-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ca6f6-123">Określa identyfikator zasobu zestawu ustawień szyfrowania dysku, który ma być używany do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="ca6f6-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca6f6-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="ca6f6-125">Łączna liczba IOPS, które będą dozwolone na wszystkich maszynach wirtualnych instalujących dysk udostępniony jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="ca6f6-126">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-126">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="ca6f6-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="ca6f6-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="ca6f6-128">Liczba IOPS dozwolonych dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ca6f6-129">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="ca6f6-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca6f6-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="ca6f6-131">Łączna przepływność (MB/s), które będą dozwolone na wszystkich maszynach wirtualnych instalujących dysk udostępniony jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="ca6f6-132">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="ca6f6-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="ca6f6-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="ca6f6-134">Przepustowość dozwolona dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ca6f6-135">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="ca6f6-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ca6f6-136">-DiskSizeGB</span></span>
<span data-ttu-id="ca6f6-137">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ca6f6-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ca6f6-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ca6f6-139">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ca6f6-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="ca6f6-140">-EncryptionType</span></span>
<span data-ttu-id="ca6f6-141">Typ klucza służący do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="ca6f6-142">Dostępne wartości: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="ca6f6-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="ca6f6-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ca6f6-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="ca6f6-144">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ca6f6-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="ca6f6-145">-MaxSharesCount</span></span>
<span data-ttu-id="ca6f6-146">Maksymalna liczba maszyn wirtualnych, które można dołączyć do dysku w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="ca6f6-147">Wartość większa niż jedna wskazuje, że dysk może być instalowany jednocześnie z wieloma maszynami wirtualnymi w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="ca6f6-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca6f6-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="ca6f6-149">{{Fill NetworkAccessPolicy Description}}</span><span class="sxs-lookup"><span data-stu-id="ca6f6-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="ca6f6-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="ca6f6-150">-OsType</span></span>
<span data-ttu-id="ca6f6-151">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ca6f6-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ca6f6-152">-SkuName</span></span>
<span data-ttu-id="ca6f6-153">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="ca6f6-154">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="ca6f6-155">UltraSSD_LRS można użyć tylko z wartością pustą dla parametru usługi.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="ca6f6-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca6f6-156">-Tag</span></span>
<span data-ttu-id="ca6f6-157">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca6f6-158">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ca6f6-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ca6f6-159">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="ca6f6-159">-Tier</span></span>
<span data-ttu-id="ca6f6-160">Warstwa wydajności dysku.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="ca6f6-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca6f6-161">-Confirm</span></span>
<span data-ttu-id="ca6f6-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca6f6-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca6f6-163">-WhatIf</span></span>
<span data-ttu-id="ca6f6-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca6f6-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca6f6-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6f6-166">CommonParameters</span></span>
<span data-ttu-id="ca6f6-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6f6-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca6f6-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6f6-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca6f6-169">INPUTS</span></span>

### <span data-ttu-id="ca6f6-170">System. String</span><span class="sxs-lookup"><span data-stu-id="ca6f6-170">System.String</span></span>

### <span data-ttu-id="ca6f6-171">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="ca6f6-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ca6f6-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ca6f6-172">System.Int32</span></span>

### <span data-ttu-id="ca6f6-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca6f6-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ca6f6-174">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca6f6-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ca6f6-175">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="ca6f6-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ca6f6-176">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="ca6f6-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ca6f6-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca6f6-177">OUTPUTS</span></span>

### <span data-ttu-id="ca6f6-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ca6f6-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="ca6f6-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca6f6-179">NOTES</span></span>

## <span data-ttu-id="ca6f6-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca6f6-180">RELATED LINKS</span></span>
