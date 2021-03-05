---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: a5876f705749d1391540bffdf537899e29b9560d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981169"
---
# <span data-ttu-id="95a6e-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="95a6e-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="95a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="95a6e-103">Dodaje dysk danych do obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="95a6e-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="95a6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95a6e-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95a6e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="95a6e-105">DESCRIPTION</span></span>
<span data-ttu-id="95a6e-106">Polecenie **cmdlet Add-AzImageDataData Można** dodać do obiektu obrazu dysk danych.</span><span class="sxs-lookup"><span data-stu-id="95a6e-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="95a6e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95a6e-107">EXAMPLES</span></span>

### <span data-ttu-id="95a6e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95a6e-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="95a6e-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w $imageConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="95a6e-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="95a6e-110">Następne trzy polecenia przypiszą ścieżki dysku systemu operacyjnego i dwie dyskietki danych do zmiennych $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="95a6e-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="95a6e-111">Ta metoda ma na celu tylko czytelność następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="95a6e-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="95a6e-112">Następne trzy polecenia dodają dysk systemu operacyjnego i dwa dysk danych dla obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="95a6e-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="95a6e-113">Dane URI każdego dysku są przechowywane w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="95a6e-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="95a6e-114">Końcowe polecenie tworzy obraz o nazwie Nazwa_obrazu01 w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="95a6e-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="95a6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95a6e-115">PARAMETERS</span></span>

### <span data-ttu-id="95a6e-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="95a6e-116">-BlobUri</span></span>
<span data-ttu-id="95a6e-117">Określa link (jako URI) obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="95a6e-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a6e-118">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="95a6e-118">-Caching</span></span>
<span data-ttu-id="95a6e-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="95a6e-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a6e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a6e-120">-DefaultProfile</span></span>
<span data-ttu-id="95a6e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95a6e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95a6e-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="95a6e-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="95a6e-123">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="95a6e-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="95a6e-124">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="95a6e-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="95a6e-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="95a6e-125">-DiskSizeGB</span></span>
<span data-ttu-id="95a6e-126">Określa rozmiar dysku w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="95a6e-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="95a6e-127">— Obraz</span><span class="sxs-lookup"><span data-stu-id="95a6e-127">-Image</span></span>
<span data-ttu-id="95a6e-128">Określa obiekt obrazu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="95a6e-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95a6e-129">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="95a6e-129">-Lun</span></span>
<span data-ttu-id="95a6e-130">Określa numer jednostki logicznej (OWĄ).</span><span class="sxs-lookup"><span data-stu-id="95a6e-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a6e-131">-Managed Jednakid</span><span class="sxs-lookup"><span data-stu-id="95a6e-131">-ManagedDiskId</span></span>
<span data-ttu-id="95a6e-132">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="95a6e-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="95a6e-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="95a6e-133">-SnapshotId</span></span>
<span data-ttu-id="95a6e-134">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="95a6e-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="95a6e-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="95a6e-135">-StorageAccountType</span></span>
<span data-ttu-id="95a6e-136">Typ konta magazynu dysku obrazu danych</span><span class="sxs-lookup"><span data-stu-id="95a6e-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="95a6e-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95a6e-137">-Confirm</span></span>
<span data-ttu-id="95a6e-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95a6e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a6e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a6e-139">-WhatIf</span></span>
<span data-ttu-id="95a6e-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a6e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95a6e-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95a6e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a6e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a6e-142">CommonParameters</span></span>
<span data-ttu-id="95a6e-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a6e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a6e-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95a6e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a6e-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95a6e-145">INPUTS</span></span>

### <span data-ttu-id="95a6e-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="95a6e-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="95a6e-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="95a6e-147">System.Int32</span></span>

### <span data-ttu-id="95a6e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="95a6e-148">System.String</span></span>

### <span data-ttu-id="95a6e-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="95a6e-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="95a6e-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95a6e-150">OUTPUTS</span></span>

### <span data-ttu-id="95a6e-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="95a6e-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="95a6e-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95a6e-152">NOTES</span></span>

## <span data-ttu-id="95a6e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95a6e-153">RELATED LINKS</span></span>
