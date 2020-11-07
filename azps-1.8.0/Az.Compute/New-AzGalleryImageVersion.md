---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710279"
---
# <span data-ttu-id="7afc4-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7afc4-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="7afc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7afc4-102">SYNOPSIS</span></span>
<span data-ttu-id="7afc4-103">Utwórz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-103">Create a gallery image version.</span></span>

## <span data-ttu-id="7afc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7afc4-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7afc4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7afc4-105">DESCRIPTION</span></span>
<span data-ttu-id="7afc4-106">Utwórz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-106">Create a gallery image version.</span></span>

## <span data-ttu-id="7afc4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7afc4-107">EXAMPLES</span></span>

### <span data-ttu-id="7afc4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7afc4-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="7afc4-109">Utwórz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-109">Create a gallery image version.</span></span>

## <span data-ttu-id="7afc4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7afc4-110">PARAMETERS</span></span>

### <span data-ttu-id="7afc4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7afc4-111">-AsJob</span></span>
<span data-ttu-id="7afc4-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7afc4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7afc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afc4-113">-DefaultProfile</span></span>
<span data-ttu-id="7afc4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7afc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7afc4-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7afc4-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="7afc4-116">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="7afc4-117">-Gallery</span><span class="sxs-lookup"><span data-stu-id="7afc4-117">-GalleryName</span></span>
<span data-ttu-id="7afc4-118">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="7afc4-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7afc4-119">-Location</span></span>
<span data-ttu-id="7afc4-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="7afc4-120">Resource location</span></span>

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

### <span data-ttu-id="7afc4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7afc4-121">-Name</span></span>
<span data-ttu-id="7afc4-122">Nazwa wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="7afc4-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="7afc4-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="7afc4-124">Data zakończenia okresu użytkowania wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="7afc4-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="7afc4-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="7afc4-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="7afc4-126">Jeśli jest ustawiona, maszyny wirtualne wdrożone z najnowszej wersji definicji obrazu nie będą używać tej wersji obrazu.</span><span class="sxs-lookup"><span data-stu-id="7afc4-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="7afc4-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7afc4-127">-ReplicaCount</span></span>
<span data-ttu-id="7afc4-128">Liczba replik wersji obrazu, które mają zostać utworzone dla każdego regionu.</span><span class="sxs-lookup"><span data-stu-id="7afc4-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="7afc4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7afc4-129">-ResourceGroupName</span></span>
<span data-ttu-id="7afc4-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7afc4-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7afc4-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="7afc4-131">-SourceImageId</span></span>
<span data-ttu-id="7afc4-132">Identyfikator obrazu źródłowego, z którego ma zostać utworzona wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="7afc4-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="7afc4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7afc4-133">-Tag</span></span>
<span data-ttu-id="7afc4-134">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="7afc4-134">Resource tags</span></span>

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

### <span data-ttu-id="7afc4-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="7afc4-135">-TargetRegion</span></span>
<span data-ttu-id="7afc4-136">Regiony docelowe, do których ma być replikowana wersja obrazu.</span><span class="sxs-lookup"><span data-stu-id="7afc4-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="7afc4-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7afc4-137">-Confirm</span></span>
<span data-ttu-id="7afc4-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7afc4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7afc4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7afc4-139">-WhatIf</span></span>
<span data-ttu-id="7afc4-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7afc4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7afc4-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7afc4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7afc4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afc4-142">CommonParameters</span></span>
<span data-ttu-id="7afc4-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7afc4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afc4-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7afc4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afc4-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7afc4-145">INPUTS</span></span>

### <span data-ttu-id="7afc4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7afc4-146">System.String</span></span>

### <span data-ttu-id="7afc4-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7afc4-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7afc4-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7afc4-148">System.Int32</span></span>

### <span data-ttu-id="7afc4-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7afc4-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7afc4-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7afc4-150">System.DateTime</span></span>

### <span data-ttu-id="7afc4-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="7afc4-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="7afc4-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7afc4-152">OUTPUTS</span></span>

### <span data-ttu-id="7afc4-153">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7afc4-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="7afc4-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7afc4-154">NOTES</span></span>

## <span data-ttu-id="7afc4-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7afc4-155">RELATED LINKS</span></span>
