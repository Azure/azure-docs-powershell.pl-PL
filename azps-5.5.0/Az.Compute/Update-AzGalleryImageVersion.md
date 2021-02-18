---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181531"
---
# <span data-ttu-id="bc07e-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bc07e-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="bc07e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc07e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc07e-103">Aktualizowanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-103">Update a gallery image version.</span></span>

## <span data-ttu-id="bc07e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc07e-104">SYNTAX</span></span>

### <span data-ttu-id="bc07e-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bc07e-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc07e-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="bc07e-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc07e-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="bc07e-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc07e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc07e-108">DESCRIPTION</span></span>
<span data-ttu-id="bc07e-109">Aktualizowanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-109">Update a gallery image version.</span></span>

## <span data-ttu-id="bc07e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc07e-110">EXAMPLES</span></span>

### <span data-ttu-id="bc07e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc07e-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="bc07e-112">Aktualizowanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-112">Update a gallery image version.</span></span>

## <span data-ttu-id="bc07e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc07e-113">PARAMETERS</span></span>

### <span data-ttu-id="bc07e-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bc07e-114">-AsJob</span></span>
<span data-ttu-id="bc07e-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bc07e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc07e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc07e-116">-DefaultProfile</span></span>
<span data-ttu-id="bc07e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc07e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc07e-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bc07e-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="bc07e-119">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc07e-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="bc07e-120">-GalleryName</span></span>
<span data-ttu-id="bc07e-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc07e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc07e-122">-InputObject</span></span>
<span data-ttu-id="bc07e-123">Obiekt wersji obrazu z galerii PS.</span><span class="sxs-lookup"><span data-stu-id="bc07e-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc07e-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc07e-124">-Name</span></span>
<span data-ttu-id="bc07e-125">Nazwa wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc07e-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bc07e-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="bc07e-127">Data zakończenia użytkowania galerii wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="bc07e-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="bc07e-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="bc07e-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="bc07e-129">Jeśli ta definicja obrazu jest ustawiona, maszyny wirtualne wdrożone z najnowszej wersji definicji obrazu nie będą używać tej wersji obrazu.</span><span class="sxs-lookup"><span data-stu-id="bc07e-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="bc07e-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="bc07e-130">-ReplicaCount</span></span>
<span data-ttu-id="bc07e-131">Liczba replik wersji obrazu do utworzenia dla każdego regionu.</span><span class="sxs-lookup"><span data-stu-id="bc07e-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="bc07e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc07e-132">-ResourceGroupName</span></span>
<span data-ttu-id="bc07e-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc07e-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc07e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc07e-134">-ResourceId</span></span>
<span data-ttu-id="bc07e-135">Identyfikator zasobu dla wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="bc07e-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc07e-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="bc07e-136">-Tag</span></span>
<span data-ttu-id="bc07e-137">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="bc07e-137">Resource tags</span></span>

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

### <span data-ttu-id="bc07e-138">- TargetRegion</span><span class="sxs-lookup"><span data-stu-id="bc07e-138">-TargetRegion</span></span>
<span data-ttu-id="bc07e-139">Regiony docelowe, do których będzie replikowana wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="bc07e-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="bc07e-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc07e-140">-Confirm</span></span>
<span data-ttu-id="bc07e-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc07e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc07e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc07e-142">-WhatIf</span></span>
<span data-ttu-id="bc07e-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc07e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc07e-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bc07e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc07e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc07e-145">CommonParameters</span></span>
<span data-ttu-id="bc07e-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc07e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc07e-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc07e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc07e-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc07e-148">INPUTS</span></span>

### <span data-ttu-id="bc07e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="bc07e-149">System.String</span></span>

### <span data-ttu-id="bc07e-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bc07e-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="bc07e-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc07e-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc07e-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bc07e-152">System.Int32</span></span>

### <span data-ttu-id="bc07e-153">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="bc07e-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bc07e-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="bc07e-154">System.DateTime</span></span>

### <span data-ttu-id="bc07e-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="bc07e-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bc07e-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc07e-156">OUTPUTS</span></span>

### <span data-ttu-id="bc07e-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bc07e-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="bc07e-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc07e-158">NOTES</span></span>

## <span data-ttu-id="bc07e-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc07e-159">RELATED LINKS</span></span>
