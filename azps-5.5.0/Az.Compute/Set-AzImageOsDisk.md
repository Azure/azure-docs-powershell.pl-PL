---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238700"
---
# <span data-ttu-id="d97fc-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="d97fc-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="d97fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d97fc-102">SYNOPSIS</span></span>
<span data-ttu-id="d97fc-103">Ustawia właściwości dysku systemu operacyjnego obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="d97fc-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d97fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d97fc-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d97fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d97fc-105">DESCRIPTION</span></span>
<span data-ttu-id="d97fc-106">Polecenie **cmdlet Set-AzImageOs Można** ustawić właściwości dysku systemu operacyjnego w obiekcie obrazu.</span><span class="sxs-lookup"><span data-stu-id="d97fc-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d97fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d97fc-107">EXAMPLES</span></span>

### <span data-ttu-id="d97fc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d97fc-108">Example 1</span></span>
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

<span data-ttu-id="d97fc-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w $imageConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="d97fc-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="d97fc-110">Następne trzy polecenia przypiszą ścieżki dysku systemu operacyjnego i dwie dyskietki danych do zmiennych $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d97fc-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d97fc-111">Ta metoda ma na celu tylko czytelność następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="d97fc-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="d97fc-112">Następne trzy polecenia dodają dysk systemu operacyjnego i dwa dyski dla danych do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d97fc-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d97fc-113">Dane URI każdego dysku są przechowywane w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d97fc-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="d97fc-114">Końcowe polecenie tworzy obraz o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d97fc-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d97fc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d97fc-115">PARAMETERS</span></span>

### <span data-ttu-id="d97fc-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="d97fc-116">-BlobUri</span></span>
<span data-ttu-id="d97fc-117">Określa wartość Uri obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="d97fc-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="d97fc-118">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="d97fc-118">-Caching</span></span>
<span data-ttu-id="d97fc-119">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="d97fc-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97fc-120">-DefaultProfile</span></span>
<span data-ttu-id="d97fc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d97fc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d97fc-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d97fc-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d97fc-123">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="d97fc-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d97fc-124">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d97fc-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="d97fc-125">- DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d97fc-125">-DiskSizeGB</span></span>
<span data-ttu-id="d97fc-126">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="d97fc-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="d97fc-127">— Obraz</span><span class="sxs-lookup"><span data-stu-id="d97fc-127">-Image</span></span>
<span data-ttu-id="d97fc-128">Określa obiekt obrazu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="d97fc-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="d97fc-129">-Managed Jednakid</span><span class="sxs-lookup"><span data-stu-id="d97fc-129">-ManagedDiskId</span></span>
<span data-ttu-id="d97fc-130">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d97fc-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="d97fc-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="d97fc-131">-OsState</span></span>
<span data-ttu-id="d97fc-132">Określa stan systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d97fc-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97fc-133">- OsType</span><span class="sxs-lookup"><span data-stu-id="d97fc-133">-OsType</span></span>
<span data-ttu-id="d97fc-134">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d97fc-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="d97fc-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d97fc-135">-SnapshotId</span></span>
<span data-ttu-id="d97fc-136">Określa identyfikator migawki.</span><span class="sxs-lookup"><span data-stu-id="d97fc-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="d97fc-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d97fc-137">-StorageAccountType</span></span>
<span data-ttu-id="d97fc-138">Typ konta magazynu dysku obrazu systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="d97fc-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="d97fc-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d97fc-139">-Confirm</span></span>
<span data-ttu-id="d97fc-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d97fc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d97fc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d97fc-141">-WhatIf</span></span>
<span data-ttu-id="d97fc-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d97fc-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d97fc-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d97fc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d97fc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97fc-144">CommonParameters</span></span>
<span data-ttu-id="d97fc-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97fc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97fc-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d97fc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97fc-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d97fc-147">INPUTS</span></span>

### <span data-ttu-id="d97fc-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="d97fc-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="d97fc-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d97fc-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d97fc-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d97fc-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d97fc-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d97fc-151">System.String</span></span>

### <span data-ttu-id="d97fc-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d97fc-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d97fc-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d97fc-153">System.Int32</span></span>

## <span data-ttu-id="d97fc-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d97fc-154">OUTPUTS</span></span>

### <span data-ttu-id="d97fc-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="d97fc-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d97fc-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d97fc-156">NOTES</span></span>

## <span data-ttu-id="d97fc-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d97fc-157">RELATED LINKS</span></span>
