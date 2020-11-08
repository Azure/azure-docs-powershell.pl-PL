---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231539"
---
# <span data-ttu-id="e42f2-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e42f2-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="e42f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e42f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e42f2-103">Utwórz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-103">Create a gallery image version.</span></span>

## <span data-ttu-id="e42f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e42f2-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e42f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e42f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e42f2-106">Utwórz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-106">Create a gallery image version.</span></span>

## <span data-ttu-id="e42f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e42f2-107">EXAMPLES</span></span>

### <span data-ttu-id="e42f2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e42f2-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="e42f2-109">Utwórz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-109">Create a gallery image version.</span></span>

### <span data-ttu-id="e42f2-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e42f2-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="e42f2-111">Tworzenie Zdjęcia z galerii za pomocą szyfrowania obrazu dysku.</span><span class="sxs-lookup"><span data-stu-id="e42f2-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="e42f2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e42f2-112">PARAMETERS</span></span>

### <span data-ttu-id="e42f2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e42f2-113">-AsJob</span></span>
<span data-ttu-id="e42f2-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e42f2-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="e42f2-115">-DataDiskImage</span></span>
<span data-ttu-id="e42f2-116">Obrazy na dyskach danych.</span><span class="sxs-lookup"><span data-stu-id="e42f2-116">Data disk images.</span></span>   <span data-ttu-id="e42f2-117">na przykład @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGBd = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="e42f2-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42f2-118">-DefaultProfile</span></span>
<span data-ttu-id="e42f2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e42f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e42f2-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e42f2-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="e42f2-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-122">-Gallery</span><span class="sxs-lookup"><span data-stu-id="e42f2-122">-GalleryName</span></span>
<span data-ttu-id="e42f2-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e42f2-124">-Location</span></span>
<span data-ttu-id="e42f2-125">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="e42f2-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e42f2-126">-Name</span></span>
<span data-ttu-id="e42f2-127">Nazwa wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="e42f2-128">-OSDiskImage</span></span>
<span data-ttu-id="e42f2-129">Obraz dysku systemu operacyjnego, na przykład @ {Source = @ {ID =<source_id>}; SizeInGBd = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="e42f2-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="e42f2-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="e42f2-131">Data zakończenia okresu użytkowania wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="e42f2-131">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="e42f2-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="e42f2-133">Jeśli jest ustawiona, maszyny wirtualne wdrożone z najnowszej wersji definicji obrazu nie będą używać tej wersji obrazu.</span><span class="sxs-lookup"><span data-stu-id="e42f2-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="e42f2-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e42f2-134">-ReplicaCount</span></span>
<span data-ttu-id="e42f2-135">Liczba replik wersji obrazu, które mają zostać utworzone dla każdego regionu.</span><span class="sxs-lookup"><span data-stu-id="e42f2-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="e42f2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42f2-136">-ResourceGroupName</span></span>
<span data-ttu-id="e42f2-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e42f2-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="e42f2-138">-SourceImageId</span></span>
<span data-ttu-id="e42f2-139">Identyfikator obrazu źródłowego, z którego ma zostać utworzona wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="e42f2-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="e42f2-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e42f2-140">-StorageAccountType</span></span>
<span data-ttu-id="e42f2-141">Określa typ konta magazynu, który ma być wykorzystywany do przechowywania obrazu.</span><span class="sxs-lookup"><span data-stu-id="e42f2-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="e42f2-142">Tej właściwości nie można aktualizować.</span><span class="sxs-lookup"><span data-stu-id="e42f2-142">This property is not updatable.</span></span> <span data-ttu-id="e42f2-143">Dostępne wartości to Standard_LRS, Standard_ZRS i Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="e42f2-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="e42f2-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="e42f2-144">-Tag</span></span>
<span data-ttu-id="e42f2-145">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="e42f2-145">Resource tags</span></span>

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

### <span data-ttu-id="e42f2-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="e42f2-146">-TargetRegion</span></span>
<span data-ttu-id="e42f2-147">Regiony docelowe, do których ma być replikowana wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="e42f2-147">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42f2-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e42f2-148">-Confirm</span></span>
<span data-ttu-id="e42f2-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e42f2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42f2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42f2-150">-WhatIf</span></span>
<span data-ttu-id="e42f2-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e42f2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42f2-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e42f2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42f2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42f2-153">CommonParameters</span></span>
<span data-ttu-id="e42f2-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42f2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42f2-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e42f2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42f2-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e42f2-156">INPUTS</span></span>

### <span data-ttu-id="e42f2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e42f2-157">System.String</span></span>

### <span data-ttu-id="e42f2-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e42f2-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e42f2-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e42f2-159">System.Int32</span></span>

### <span data-ttu-id="e42f2-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e42f2-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e42f2-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e42f2-161">System.DateTime</span></span>

### <span data-ttu-id="e42f2-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="e42f2-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="e42f2-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e42f2-163">OUTPUTS</span></span>

### <span data-ttu-id="e42f2-164">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e42f2-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="e42f2-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e42f2-165">NOTES</span></span>

## <span data-ttu-id="e42f2-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e42f2-166">RELATED LINKS</span></span>
