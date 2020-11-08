---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225214"
---
# <span data-ttu-id="f480f-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f480f-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="f480f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f480f-102">SYNOPSIS</span></span>
<span data-ttu-id="f480f-103">Tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="f480f-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="f480f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f480f-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f480f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f480f-105">DESCRIPTION</span></span>
<span data-ttu-id="f480f-106">Polecenie cmdlet **New-AzDiskConfig** tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="f480f-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="f480f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f480f-107">EXAMPLES</span></span>

### <span data-ttu-id="f480f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f480f-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="f480f-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f480f-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="f480f-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f480f-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="f480f-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="f480f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="f480f-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f480f-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f480f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f480f-113">Example 2</span></span>
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

<span data-ttu-id="f480f-114">Pierwsze polecenie tworzy obiekt dysku lokalnego do przekazania.</span><span class="sxs-lookup"><span data-stu-id="f480f-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="f480f-115">Drugie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f480f-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="f480f-116">Trzecie polecenie pobiera adres URL dla dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="f480f-117">Czwarte polecenie uzyskuje stan dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="f480f-118">Jeśli dysk jest w stanie "ReadyToUpload", użytkownik może przekazać dysk z przestrzeni dyskowej BLOB do adresu URL dysków SAS dysku przy użyciu AzCopy.</span><span class="sxs-lookup"><span data-stu-id="f480f-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="f480f-119">Podczas przekazywania stan dysku zmieni się na "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="f480f-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="f480f-120">Ostatnie polecenie odwołuje dostęp do dysku w adresie URL SAS.</span><span class="sxs-lookup"><span data-stu-id="f480f-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="f480f-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f480f-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="f480f-122">Tworzenie dysku z wersji obrazu galerii udostępnionej.</span><span class="sxs-lookup"><span data-stu-id="f480f-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="f480f-123">Identyfikator to identyfikator wersji obrazu galerii udostępnionej.</span><span class="sxs-lookup"><span data-stu-id="f480f-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="f480f-124">Numer LUN jest potrzebny tylko wtedy, gdy źródłem jest dysk danych.</span><span class="sxs-lookup"><span data-stu-id="f480f-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="f480f-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f480f-125">PARAMETERS</span></span>

### <span data-ttu-id="f480f-126">-Opcja</span><span class="sxs-lookup"><span data-stu-id="f480f-126">-CreateOption</span></span>
<span data-ttu-id="f480f-127">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="f480f-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="f480f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f480f-128">-DefaultProfile</span></span>
<span data-ttu-id="f480f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f480f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f480f-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="f480f-130">-DiskAccessId</span></span>
<span data-ttu-id="f480f-131">Pobiera lub ustawia identyfikator ARM zasobu DiskAccess na potrzeby używania prywatnych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="f480f-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="f480f-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f480f-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="f480f-133">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="f480f-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="f480f-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="f480f-135">Określa identyfikator zasobu zestawu ustawień szyfrowania dysku, który ma być używany do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="f480f-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="f480f-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="f480f-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="f480f-137">Łączna liczba IOPS, które będą dozwolone na wszystkich maszynach wirtualnych instalujących dysk udostępniony jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="f480f-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="f480f-138">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="f480f-138">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f480f-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="f480f-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="f480f-140">Liczba IOPS dozwolonych dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="f480f-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="f480f-141">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="f480f-141">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f480f-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="f480f-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="f480f-143">"opis": "całkowita przepływność (MB/s), która będzie dozwolona na wszystkich maszynach wirtualnych instalująca dysk udostępniony jako tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="f480f-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="f480f-144">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="f480f-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f480f-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="f480f-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="f480f-146">Przepustowość dozwolona dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="f480f-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="f480f-147">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="f480f-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f480f-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f480f-148">-DiskSizeGB</span></span>
<span data-ttu-id="f480f-149">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="f480f-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="f480f-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f480f-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f480f-151">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f480f-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="f480f-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="f480f-152">-EncryptionType</span></span>
<span data-ttu-id="f480f-153">Typ klucza służący do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="f480f-154">Dostępne wartości: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="f480f-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="f480f-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f480f-155">-GalleryImageReference</span></span>
<span data-ttu-id="f480f-156">Obiekt GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="f480f-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="f480f-157">Wymagane w przypadku tworzenia z obrazu z galerii.</span><span class="sxs-lookup"><span data-stu-id="f480f-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="f480f-158">Identyfikator będzie identyfikatorem ARM dla udostępnionej wersji obrazu w ramach korekty, z której ma zostać utworzony dysk.</span><span class="sxs-lookup"><span data-stu-id="f480f-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="f480f-159">Jeśli źródłem kopii jest jedna z dysków danych w obrazie galerii, wymagana jest jednostka LUN. Jeśli wartość null, dysk systemu operacyjnego obrazu zostanie skopiowany.</span><span class="sxs-lookup"><span data-stu-id="f480f-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="f480f-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="f480f-160">-HyperVGeneration</span></span>
<span data-ttu-id="f480f-161">Generowanie funkcji hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f480f-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="f480f-162">Dotyczy tylko dysków z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="f480f-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="f480f-163">Dozwolone wartości to V1 i v2.</span><span class="sxs-lookup"><span data-stu-id="f480f-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="f480f-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="f480f-164">-ImageReference</span></span>
<span data-ttu-id="f480f-165">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="f480f-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f480f-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="f480f-167">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="f480f-168">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f480f-168">-Location</span></span>
<span data-ttu-id="f480f-169">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="f480f-169">Specifies a location.</span></span>

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

### <span data-ttu-id="f480f-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="f480f-170">-LogicalSectorSize</span></span>
<span data-ttu-id="f480f-171">Rozmiar sektora logicznego w bajtach dla Ultra dysków.</span><span class="sxs-lookup"><span data-stu-id="f480f-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="f480f-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="f480f-172">-MaxSharesCount</span></span>
<span data-ttu-id="f480f-173">Maksymalna liczba maszyn wirtualnych, które można dołączyć do dysku w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="f480f-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="f480f-174">Wartość większa niż jedna wskazuje, że dysk może być instalowany jednocześnie z wieloma maszynami wirtualnymi w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="f480f-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="f480f-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f480f-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="f480f-176">Zasady dostępu do sieci definiują zasady dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="f480f-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="f480f-177">Możliwe wartości to: "AllowAll", "AllowPrivate", "DenyAll".</span><span class="sxs-lookup"><span data-stu-id="f480f-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="f480f-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="f480f-178">-OsType</span></span>
<span data-ttu-id="f480f-179">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="f480f-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f480f-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f480f-180">-SkuName</span></span>
<span data-ttu-id="f480f-181">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f480f-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="f480f-182">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="f480f-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="f480f-183">UltraSSD_LRS można użyć tylko z wartością pustą dla parametru usługi.</span><span class="sxs-lookup"><span data-stu-id="f480f-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="f480f-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f480f-184">-SourceResourceId</span></span>
<span data-ttu-id="f480f-185">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="f480f-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="f480f-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f480f-186">-SourceUri</span></span>
<span data-ttu-id="f480f-187">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="f480f-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="f480f-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f480f-188">-StorageAccountId</span></span>
<span data-ttu-id="f480f-189">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f480f-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="f480f-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="f480f-190">-Tag</span></span>
<span data-ttu-id="f480f-191">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f480f-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f480f-192">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f480f-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f480f-193">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="f480f-193">-Tier</span></span>
<span data-ttu-id="f480f-194">Warstwa wydajności dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="f480f-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="f480f-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="f480f-196">Określa rozmiar zawartości przekazanie, łącznie z stopką dysku VHD, gdy opcja ta jest przekazywana.</span><span class="sxs-lookup"><span data-stu-id="f480f-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="f480f-197">Ta wartość powinna znajdować się w zakresie od 20972032 (20 MiB + 512 bajtów dla stopki VHD) i 35183298347520 bajtów (32 TiB + 512 bajtów dla stopki VHD).</span><span class="sxs-lookup"><span data-stu-id="f480f-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f480f-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="f480f-198">-Zone</span></span>
<span data-ttu-id="f480f-199">Określa listę stref logicznych dla dysku.</span><span class="sxs-lookup"><span data-stu-id="f480f-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="f480f-200">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f480f-200">-Confirm</span></span>
<span data-ttu-id="f480f-201">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f480f-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f480f-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f480f-202">-WhatIf</span></span>
<span data-ttu-id="f480f-203">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f480f-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f480f-204">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f480f-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f480f-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f480f-205">CommonParameters</span></span>
<span data-ttu-id="f480f-206">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f480f-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f480f-207">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f480f-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f480f-208">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f480f-208">INPUTS</span></span>

### <span data-ttu-id="f480f-209">System. String</span><span class="sxs-lookup"><span data-stu-id="f480f-209">System.String</span></span>

### <span data-ttu-id="f480f-210">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="f480f-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f480f-211">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f480f-211">System.Int32</span></span>

### <span data-ttu-id="f480f-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="f480f-212">System.String[]</span></span>

### <span data-ttu-id="f480f-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f480f-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f480f-214">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="f480f-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="f480f-215">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f480f-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f480f-216">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="f480f-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="f480f-217">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="f480f-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f480f-218">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f480f-218">OUTPUTS</span></span>

### <span data-ttu-id="f480f-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="f480f-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="f480f-220">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f480f-220">NOTES</span></span>

## <span data-ttu-id="f480f-221">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f480f-221">RELATED LINKS</span></span>
