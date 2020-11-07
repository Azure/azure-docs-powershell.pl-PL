---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 273a4388665e12cf58d1fe2d7e067648862bf4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710285"
---
# <span data-ttu-id="e4ee4-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e4ee4-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="e4ee4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ee4-103">Tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="e4ee4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4ee4-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4ee4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ee4-106">Polecenie cmdlet **New-AzDiskConfig** tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="e4ee4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ee4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4ee4-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e4ee4-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="e4ee4-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="e4ee4-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="e4ee4-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e4ee4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e4ee4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e4ee4-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e4ee4-114">Pierwsze polecenie tworzy obiekt dysku lokalnego do przekazania.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="e4ee4-115">Drugie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e4ee4-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="e4ee4-116">Trzecie polecenie pobiera adres URL dla dysku.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="e4ee4-117">Czwarte polecenie uzyskuje stan dysku.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="e4ee4-118">Jeśli dysk jest w stanie "ReadyToUpload", użytkownik może przekazać dysk z przestrzeni dyskowej BLOB do adresu URL dysków SAS dysku przy użyciu AzCopy.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="e4ee4-119">Podczas przekazywania stan dysku zmieni się na "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="e4ee4-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="e4ee4-120">Ostatnie polecenie odwołuje dostęp do dysku w adresie URL SAS.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="e4ee4-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4ee4-121">PARAMETERS</span></span>

### <span data-ttu-id="e4ee4-122">-Opcja</span><span class="sxs-lookup"><span data-stu-id="e4ee4-122">-CreateOption</span></span>
<span data-ttu-id="e4ee4-123">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e4ee4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ee4-124">-DefaultProfile</span></span>
<span data-ttu-id="e4ee4-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4ee4-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e4ee4-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="e4ee4-127">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="e4ee4-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4ee4-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="e4ee4-129">Liczba IOPS dozwolonych dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e4ee4-130">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="e4ee4-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4ee4-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="e4ee4-132">Przepustowość dozwolona dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e4ee4-133">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="e4ee4-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e4ee4-134">-DiskSizeGB</span></span>
<span data-ttu-id="e4ee4-135">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e4ee4-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e4ee4-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e4ee4-137">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e4ee4-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="e4ee4-138">-HyperVGeneration</span></span>
<span data-ttu-id="e4ee4-139">Generowanie funkcji hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="e4ee4-140">Dotyczy tylko dysków z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="e4ee4-141">Dozwolone wartości to V1 i v2.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="e4ee4-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e4ee4-142">-ImageReference</span></span>
<span data-ttu-id="e4ee4-143">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="e4ee4-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e4ee4-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="e4ee4-145">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="e4ee4-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4ee4-146">-Location</span></span>
<span data-ttu-id="e4ee4-147">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-147">Specifies a location.</span></span>

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

### <span data-ttu-id="e4ee4-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="e4ee4-148">-OsType</span></span>
<span data-ttu-id="e4ee4-149">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e4ee4-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4ee4-150">-SkuName</span></span>
<span data-ttu-id="e4ee4-151">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="e4ee4-152">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="e4ee4-153">UltraSSD_LRS można użyć tylko z wartością pustą dla parametru usługi.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="e4ee4-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e4ee4-154">-SourceResourceId</span></span>
<span data-ttu-id="e4ee4-155">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="e4ee4-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e4ee4-156">-SourceUri</span></span>
<span data-ttu-id="e4ee4-157">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e4ee4-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e4ee4-158">-StorageAccountId</span></span>
<span data-ttu-id="e4ee4-159">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e4ee4-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4ee4-160">-Tag</span></span>
<span data-ttu-id="e4ee4-161">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4ee4-162">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e4ee4-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4ee4-163">-Zone</span><span class="sxs-lookup"><span data-stu-id="e4ee4-163">-Zone</span></span>
<span data-ttu-id="e4ee4-164">Określa listę stref logicznych dla dysku.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-164">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="e4ee4-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4ee4-165">-Confirm</span></span>
<span data-ttu-id="e4ee4-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ee4-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ee4-167">-WhatIf</span></span>
<span data-ttu-id="e4ee4-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4ee4-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4ee4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ee4-170">CommonParameters</span></span>
<span data-ttu-id="e4ee4-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ee4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ee4-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ee4-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ee4-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4ee4-173">INPUTS</span></span>

### <span data-ttu-id="e4ee4-174">System. String</span><span class="sxs-lookup"><span data-stu-id="e4ee4-174">System.String</span></span>

### <span data-ttu-id="e4ee4-175">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="e4ee4-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e4ee4-176">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e4ee4-176">System.Int32</span></span>

### <span data-ttu-id="e4ee4-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="e4ee4-177">System.String[]</span></span>

### <span data-ttu-id="e4ee4-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4ee4-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4ee4-179">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="e4ee4-179">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="e4ee4-180">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4ee4-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4ee4-181">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="e4ee4-181">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e4ee4-182">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="e4ee4-182">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e4ee4-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4ee4-183">OUTPUTS</span></span>

### <span data-ttu-id="e4ee4-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="e4ee4-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e4ee4-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4ee4-185">NOTES</span></span>

## <span data-ttu-id="e4ee4-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4ee4-186">RELATED LINKS</span></span>
