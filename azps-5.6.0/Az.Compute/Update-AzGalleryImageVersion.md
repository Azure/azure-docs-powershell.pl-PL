---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 6d708689c4156cb01e950490314d7fdd2a88b67c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971425"
---
# <span data-ttu-id="f261c-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f261c-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f261c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f261c-102">SYNOPSIS</span></span>
<span data-ttu-id="f261c-103">Aktualizowanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-103">Update a gallery image version.</span></span>

## <span data-ttu-id="f261c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f261c-104">SYNTAX</span></span>

### <span data-ttu-id="f261c-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f261c-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f261c-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="f261c-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f261c-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="f261c-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f261c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f261c-108">DESCRIPTION</span></span>
<span data-ttu-id="f261c-109">Aktualizowanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-109">Update a gallery image version.</span></span>

## <span data-ttu-id="f261c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f261c-110">EXAMPLES</span></span>

### <span data-ttu-id="f261c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f261c-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="f261c-112">Aktualizowanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-112">Update a gallery image version.</span></span>

## <span data-ttu-id="f261c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f261c-113">PARAMETERS</span></span>

### <span data-ttu-id="f261c-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f261c-114">-AsJob</span></span>
<span data-ttu-id="f261c-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f261c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f261c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f261c-116">-DefaultProfile</span></span>
<span data-ttu-id="f261c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f261c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f261c-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f261c-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f261c-119">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="f261c-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f261c-120">-GalleryName</span></span>
<span data-ttu-id="f261c-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="f261c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f261c-122">-InputObject</span></span>
<span data-ttu-id="f261c-123">Obiekt wersji obrazu z galerii PS.</span><span class="sxs-lookup"><span data-stu-id="f261c-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="f261c-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f261c-124">-Name</span></span>
<span data-ttu-id="f261c-125">Nazwa wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="f261c-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="f261c-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="f261c-127">Data zakończenia użytkowania galerii wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="f261c-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="f261c-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="f261c-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="f261c-129">Jeśli ta definicja obrazu jest ustawiona, maszyny wirtualne wdrożone z najnowszej wersji definicji obrazu nie będą używać tej wersji obrazu.</span><span class="sxs-lookup"><span data-stu-id="f261c-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="f261c-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="f261c-130">-ReplicaCount</span></span>
<span data-ttu-id="f261c-131">Liczba replik wersji obrazu do utworzenia dla każdego regionu.</span><span class="sxs-lookup"><span data-stu-id="f261c-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="f261c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f261c-132">-ResourceGroupName</span></span>
<span data-ttu-id="f261c-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f261c-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="f261c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f261c-134">-ResourceId</span></span>
<span data-ttu-id="f261c-135">Identyfikator zasobu dla wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f261c-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="f261c-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="f261c-136">-Tag</span></span>
<span data-ttu-id="f261c-137">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="f261c-137">Resource tags</span></span>

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

### <span data-ttu-id="f261c-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f261c-138">-TargetRegion</span></span>
<span data-ttu-id="f261c-139">Regiony docelowe, do których będzie replikowana wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="f261c-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="f261c-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f261c-140">-Confirm</span></span>
<span data-ttu-id="f261c-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f261c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f261c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f261c-142">-WhatIf</span></span>
<span data-ttu-id="f261c-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f261c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f261c-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f261c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f261c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f261c-145">CommonParameters</span></span>
<span data-ttu-id="f261c-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f261c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f261c-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f261c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f261c-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f261c-148">INPUTS</span></span>

### <span data-ttu-id="f261c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f261c-149">System.String</span></span>

### <span data-ttu-id="f261c-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f261c-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="f261c-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f261c-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f261c-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f261c-152">System.Int32</span></span>

### <span data-ttu-id="f261c-153">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f261c-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f261c-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="f261c-154">System.DateTime</span></span>

### <span data-ttu-id="f261c-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="f261c-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="f261c-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f261c-156">OUTPUTS</span></span>

### <span data-ttu-id="f261c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f261c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f261c-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f261c-158">NOTES</span></span>

## <span data-ttu-id="f261c-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f261c-159">RELATED LINKS</span></span>
