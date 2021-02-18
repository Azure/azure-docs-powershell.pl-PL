---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 12ebf45a0428b170f40edce6129d76dd7fcbd601
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181642"
---
# <span data-ttu-id="6945b-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6945b-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="6945b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6945b-102">SYNOPSIS</span></span>
<span data-ttu-id="6945b-103">Tworzy konfigurowalny obiekt dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="6945b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6945b-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6945b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6945b-105">DESCRIPTION</span></span>
<span data-ttu-id="6945b-106">Polecenie **cmdlet New-AzConfig** tworzy konfigurowalny obiekt dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="6945b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6945b-107">EXAMPLES</span></span>

### <span data-ttu-id="6945b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6945b-108">Example 1</span></span>
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

<span data-ttu-id="6945b-109">Pierwsze polecenie tworzy lokalny pusty obiekt dysku o rozmiarze 5 GB w Standard_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6945b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="6945b-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6945b-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="6945b-111">Drugie i trzecie polecenia ustawiają ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="6945b-112">Ostatnie polecenie pobiera obiekt dysku i tworzy dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="6945b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6945b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6945b-113">Example 2</span></span>
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

<span data-ttu-id="6945b-114">Pierwsze polecenie tworzy obiekt dysku lokalnego dla polecenia Przekaż.</span><span class="sxs-lookup"><span data-stu-id="6945b-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="6945b-115">Drugie polecenie pobiera obiekt dysku i tworzy dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="6945b-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="6945b-116">Trzecie polecenie pobiera adres URL SAS dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="6945b-117">Czwarte polecenie pobiera stan dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="6945b-118">Jeśli stan dysku to "ReadyToUpload", użytkownik może przekazać dysk z magazynu obiektów blob do adresu URL SAS dysku przy użyciu narzędzia AzCopy.</span><span class="sxs-lookup"><span data-stu-id="6945b-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="6945b-119">Podczas przekazywania stan dysku zmienia się na "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="6945b-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="6945b-120">Ostatnie polecenie odwołuje dostęp do dysku adresu URL SAS.</span><span class="sxs-lookup"><span data-stu-id="6945b-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="6945b-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6945b-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="6945b-122">Utwórz dysk z udostępnionej wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="6945b-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="6945b-123">Identyfikator to identyfikator wersji obrazu udostępnionej galerii.</span><span class="sxs-lookup"><span data-stu-id="6945b-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="6945b-124">Jest ona potrzebna tylko wtedy, gdy źródłem jest dysk danych.</span><span class="sxs-lookup"><span data-stu-id="6945b-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="6945b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6945b-125">PARAMETERS</span></span>

### <span data-ttu-id="6945b-126">- PodsycanieBłędów</span><span class="sxs-lookup"><span data-stu-id="6945b-126">-BurstingEnabled</span></span>
<span data-ttu-id="6945b-127">Umożliwia seria danych wykraczających poza aprowizowany element docelowy wydajności dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="6945b-128">Rozsyłanie jest domyślnie wyłączone.</span><span class="sxs-lookup"><span data-stu-id="6945b-128">Bursting is disabled by default.</span></span> <span data-ttu-id="6945b-129">Nie dotyczy dysków Ultra.</span><span class="sxs-lookup"><span data-stu-id="6945b-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="6945b-130">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="6945b-130">-CreateOption</span></span>
<span data-ttu-id="6945b-131">Określa, czy to polecenie cmdlet tworzy dysk na komputerze wirtualnym z platformy lub obrazu użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="6945b-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="6945b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6945b-132">-DefaultProfile</span></span>
<span data-ttu-id="6945b-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6945b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6945b-134">- DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="6945b-134">-DiskAccessId</span></span>
<span data-ttu-id="6945b-135">Pobiera lub ustawia ARM zasobu DiskAccess do używania prywatnych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="6945b-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="6945b-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6945b-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="6945b-137">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="6945b-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6945b-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6945b-139">Określa identyfikator zasobu dla szyfrowania dysku ustawionego do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="6945b-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="6945b-140">- DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="6945b-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="6945b-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="6945b-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="6945b-142">Jedna operacja może przenosić od 4k do 256 tys. bajtów.</span><span class="sxs-lookup"><span data-stu-id="6945b-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="6945b-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="6945b-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="6945b-144">Liczba dozwolonych w programie IOPS dla tego dysku; można ustawić tylko dla dysków UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="6945b-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="6945b-145">Jedna operacja może przenosić od 4k do 256 tys. bajtów.</span><span class="sxs-lookup"><span data-stu-id="6945b-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="6945b-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="6945b-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="6945b-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="6945b-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="6945b-148">Program MBps oznacza miliony bajtów na sekundę — w tym przypadku MB używa notacji ISO, czyli potęg o pojemności 10.</span><span class="sxs-lookup"><span data-stu-id="6945b-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="6945b-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="6945b-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="6945b-150">Przepustowość dozwolona dla tego dysku; można ustawić tylko dla dysków UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="6945b-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="6945b-151">Mb/s oznacza, że miliony bajtów na sekundę — w tym przypadku MB używa notacji ISO, czyli potęg o pojemności 10.</span><span class="sxs-lookup"><span data-stu-id="6945b-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="6945b-152">- DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6945b-152">-DiskSizeGB</span></span>
<span data-ttu-id="6945b-153">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="6945b-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6945b-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="6945b-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6945b-155">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6945b-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6945b-156">- EncryptionType</span><span class="sxs-lookup"><span data-stu-id="6945b-156">-EncryptionType</span></span>
<span data-ttu-id="6945b-157">Typ klucza używanego do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="6945b-158">Dostępne wartości to: 'EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="6945b-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="6945b-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="6945b-159">-GalleryImageReference</span></span>
<span data-ttu-id="6945b-160">Obiekt GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="6945b-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="6945b-161">Wymagane w przypadku tworzenia z obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="6945b-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="6945b-162">Identyfikator będzie identyfikatorem ARM wersji udostępnionego obrazu galleya, z której można utworzyć dysk.</span><span class="sxs-lookup"><span data-stu-id="6945b-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="6945b-163">Jeśli źródło kopii jest jednym z dysków danych na obrazie w galerii, potrzebne jest ; Jeśli wartość null, dysk systemu operacyjnego obrazu zostanie skopiowany.</span><span class="sxs-lookup"><span data-stu-id="6945b-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="6945b-164">-HyperV Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="6945b-164">-HyperVGeneration</span></span>
<span data-ttu-id="6945b-165">Generowanie hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6945b-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="6945b-166">Dotyczy tylko dyskietek systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="6945b-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="6945b-167">Dozwolone wartości to V1 i V2.</span><span class="sxs-lookup"><span data-stu-id="6945b-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="6945b-168">- ImageReference</span><span class="sxs-lookup"><span data-stu-id="6945b-168">-ImageReference</span></span>
<span data-ttu-id="6945b-169">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="6945b-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6945b-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="6945b-171">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="6945b-172">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6945b-172">-Location</span></span>
<span data-ttu-id="6945b-173">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="6945b-173">Specifies a location.</span></span>

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

### <span data-ttu-id="6945b-174">-LogicalStoriaSize</span><span class="sxs-lookup"><span data-stu-id="6945b-174">-LogicalSectorSize</span></span>
<span data-ttu-id="6945b-175">Wielkość z sektora logicznego w bajtach na dyskach Ultra.</span><span class="sxs-lookup"><span data-stu-id="6945b-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="6945b-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="6945b-176">-MaxSharesCount</span></span>
<span data-ttu-id="6945b-177">Maksymalna liczba maszyn wirtualnych, które mogą dołączać do dysku w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="6945b-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="6945b-178">Wartość większa niż jedna wskazuje dysk, który może być jednocześnie montowany na wielu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6945b-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="6945b-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6945b-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="6945b-180">Zasady dostępu do sieci definiują zasady dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="6945b-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="6945b-181">Możliwe wartości to: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="6945b-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="6945b-182">- OsType</span><span class="sxs-lookup"><span data-stu-id="6945b-182">-OsType</span></span>
<span data-ttu-id="6945b-183">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="6945b-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6945b-184">-SKUName</span><span class="sxs-lookup"><span data-stu-id="6945b-184">-SkuName</span></span>
<span data-ttu-id="6945b-185">Określa nazwę sku konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6945b-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="6945b-186">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="6945b-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="6945b-187">UltraSSD_LRS można używać tylko z wartością pustą dla parametru CreateOption.</span><span class="sxs-lookup"><span data-stu-id="6945b-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="6945b-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6945b-188">-SourceResourceId</span></span>
<span data-ttu-id="6945b-189">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6945b-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="6945b-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="6945b-190">-SourceUri</span></span>
<span data-ttu-id="6945b-191">Określa źródłowy Uri.</span><span class="sxs-lookup"><span data-stu-id="6945b-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="6945b-192">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6945b-192">-StorageAccountId</span></span>
<span data-ttu-id="6945b-193">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6945b-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="6945b-194">— Tag</span><span class="sxs-lookup"><span data-stu-id="6945b-194">-Tag</span></span>
<span data-ttu-id="6945b-195">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="6945b-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6945b-196">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="6945b-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6945b-197">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="6945b-197">-Tier</span></span>
<span data-ttu-id="6945b-198">Warstwa wydajności dysku.</span><span class="sxs-lookup"><span data-stu-id="6945b-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="6945b-199">- UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6945b-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="6945b-200">Określa rozmiar zawartości przekazywania wraz ze stopkę VHD, gdy opcja CreateOption ma wartość Przekaż.</span><span class="sxs-lookup"><span data-stu-id="6945b-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="6945b-201">Ta wartość powinna być między 20972032 (20 bajtów mib + 512 bajtów dla stopki VHD) a 35183298347520 bajtów (32 tib + 512 bajtów dla stopki VHD).</span><span class="sxs-lookup"><span data-stu-id="6945b-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="6945b-202">— Strefa</span><span class="sxs-lookup"><span data-stu-id="6945b-202">-Zone</span></span>
<span data-ttu-id="6945b-203">Określa listę stref logicznych dla wartości Dysk.</span><span class="sxs-lookup"><span data-stu-id="6945b-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="6945b-204">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6945b-204">-Confirm</span></span>
<span data-ttu-id="6945b-205">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6945b-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6945b-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6945b-206">-WhatIf</span></span>
<span data-ttu-id="6945b-207">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6945b-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6945b-208">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6945b-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6945b-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6945b-209">CommonParameters</span></span>
<span data-ttu-id="6945b-210">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6945b-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6945b-211">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6945b-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6945b-212">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6945b-212">INPUTS</span></span>

### <span data-ttu-id="6945b-213">System.String</span><span class="sxs-lookup"><span data-stu-id="6945b-213">System.String</span></span>

### <span data-ttu-id="6945b-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6945b-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6945b-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6945b-215">System.Int32</span></span>

### <span data-ttu-id="6945b-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6945b-216">System.String[]</span></span>

### <span data-ttu-id="6945b-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6945b-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6945b-218">Microsoft.Azure.Management.Compute.Models.ImageFerence</span><span class="sxs-lookup"><span data-stu-id="6945b-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="6945b-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6945b-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6945b-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="6945b-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="6945b-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="6945b-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="6945b-222">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6945b-222">OUTPUTS</span></span>

### <span data-ttu-id="6945b-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="6945b-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="6945b-224">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6945b-224">NOTES</span></span>

## <span data-ttu-id="6945b-225">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6945b-225">RELATED LINKS</span></span>
