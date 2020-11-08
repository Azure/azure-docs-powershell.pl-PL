---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222034"
---
# <span data-ttu-id="686fd-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="686fd-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="686fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="686fd-102">SYNOPSIS</span></span>
<span data-ttu-id="686fd-103">Aktualizowanie wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-103">Update a gallery image version.</span></span>

## <span data-ttu-id="686fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="686fd-104">SYNTAX</span></span>

### <span data-ttu-id="686fd-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="686fd-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="686fd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="686fd-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="686fd-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="686fd-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="686fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="686fd-108">DESCRIPTION</span></span>
<span data-ttu-id="686fd-109">Aktualizowanie wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-109">Update a gallery image version.</span></span>

## <span data-ttu-id="686fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="686fd-110">EXAMPLES</span></span>

### <span data-ttu-id="686fd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="686fd-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="686fd-112">Aktualizowanie wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-112">Update a gallery image version.</span></span>

## <span data-ttu-id="686fd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="686fd-113">PARAMETERS</span></span>

### <span data-ttu-id="686fd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="686fd-114">-AsJob</span></span>
<span data-ttu-id="686fd-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="686fd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="686fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686fd-116">-DefaultProfile</span></span>
<span data-ttu-id="686fd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="686fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="686fd-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="686fd-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="686fd-119">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="686fd-120">-Gallery</span><span class="sxs-lookup"><span data-stu-id="686fd-120">-GalleryName</span></span>
<span data-ttu-id="686fd-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="686fd-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="686fd-122">-InputObject</span></span>
<span data-ttu-id="686fd-123">Obiekt wersja obrazu galerii PS.</span><span class="sxs-lookup"><span data-stu-id="686fd-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="686fd-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="686fd-124">-Name</span></span>
<span data-ttu-id="686fd-125">Nazwa wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="686fd-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="686fd-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="686fd-127">Data zakończenia okresu użytkowania wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="686fd-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="686fd-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="686fd-129">Jeśli jest ustawiona, maszyny wirtualne wdrożone z najnowszej wersji definicji obrazu nie będą używać tej wersji obrazu.</span><span class="sxs-lookup"><span data-stu-id="686fd-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="686fd-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="686fd-130">-ReplicaCount</span></span>
<span data-ttu-id="686fd-131">Liczba replik wersji obrazu, które mają zostać utworzone dla każdego regionu.</span><span class="sxs-lookup"><span data-stu-id="686fd-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="686fd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="686fd-132">-ResourceGroupName</span></span>
<span data-ttu-id="686fd-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="686fd-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="686fd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="686fd-134">-ResourceId</span></span>
<span data-ttu-id="686fd-135">Identyfikator zasobu dla wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="686fd-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="686fd-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="686fd-136">-Tag</span></span>
<span data-ttu-id="686fd-137">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="686fd-137">Resource tags</span></span>

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

### <span data-ttu-id="686fd-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="686fd-138">-TargetRegion</span></span>
<span data-ttu-id="686fd-139">Regiony docelowe, do których ma być replikowana wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="686fd-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="686fd-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="686fd-140">-Confirm</span></span>
<span data-ttu-id="686fd-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="686fd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="686fd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="686fd-142">-WhatIf</span></span>
<span data-ttu-id="686fd-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="686fd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="686fd-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="686fd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="686fd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686fd-145">CommonParameters</span></span>
<span data-ttu-id="686fd-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686fd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686fd-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="686fd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686fd-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="686fd-148">INPUTS</span></span>

### <span data-ttu-id="686fd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="686fd-149">System.String</span></span>

### <span data-ttu-id="686fd-150">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="686fd-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="686fd-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="686fd-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="686fd-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="686fd-152">System.Int32</span></span>

### <span data-ttu-id="686fd-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="686fd-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="686fd-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="686fd-154">System.DateTime</span></span>

### <span data-ttu-id="686fd-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="686fd-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="686fd-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="686fd-156">OUTPUTS</span></span>

### <span data-ttu-id="686fd-157">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="686fd-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="686fd-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="686fd-158">NOTES</span></span>

## <span data-ttu-id="686fd-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="686fd-159">RELATED LINKS</span></span>
