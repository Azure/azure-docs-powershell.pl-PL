---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013041"
---
# <span data-ttu-id="ada2f-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="ada2f-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="ada2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada2f-102">SYNOPSIS</span></span>
<span data-ttu-id="ada2f-103">W tym artykule opisano źródło obrazów maszyn wirtualnych do tworzenia, dostosowywania i rozpowszechniania.</span><span class="sxs-lookup"><span data-stu-id="ada2f-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="ada2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ada2f-104">SYNTAX</span></span>

### <span data-ttu-id="ada2f-105">ManagedImage (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ada2f-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="ada2f-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="ada2f-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="ada2f-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="ada2f-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ada2f-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="ada2f-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ada2f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ada2f-109">DESCRIPTION</span></span>
<span data-ttu-id="ada2f-110">W tym artykule opisano źródło obrazów maszyn wirtualnych do tworzenia, dostosowywania i rozpowszechniania.</span><span class="sxs-lookup"><span data-stu-id="ada2f-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="ada2f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ada2f-111">EXAMPLES</span></span>

### <span data-ttu-id="ada2f-112">Przykład 1. Tworzenie zarządzanego źródła obrazów</span><span class="sxs-lookup"><span data-stu-id="ada2f-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="ada2f-113">To polecenie tworzy zarządzane źródło obrazów.</span><span class="sxs-lookup"><span data-stu-id="ada2f-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="ada2f-114">Przykład 2. Tworzenie udostępnionego źródła obrazów</span><span class="sxs-lookup"><span data-stu-id="ada2f-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="ada2f-115">To polecenie tworzy udostępnione źródło obrazów.</span><span class="sxs-lookup"><span data-stu-id="ada2f-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="ada2f-116">Przykład 3. Tworzenie platonu ze źródła obrazu</span><span class="sxs-lookup"><span data-stu-id="ada2f-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="ada2f-117">To polecenie tworzy poszyfrowanie źródła obrazów.</span><span class="sxs-lookup"><span data-stu-id="ada2f-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="ada2f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada2f-118">PARAMETERS</span></span>

### <span data-ttu-id="ada2f-119">- ImageId</span><span class="sxs-lookup"><span data-stu-id="ada2f-119">-ImageId</span></span>
<span data-ttu-id="ada2f-120">ARM identyfikator zasobu obrazu zarządzanego w subskrypcji klienta.</span><span class="sxs-lookup"><span data-stu-id="ada2f-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="ada2f-121">-ImageVersionId</span></span>
<span data-ttu-id="ada2f-122">ARM identyfikator zasobu wersji obrazu w udostępnionej galerii obrazów.</span><span class="sxs-lookup"><span data-stu-id="ada2f-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-123">— Oferta</span><span class="sxs-lookup"><span data-stu-id="ada2f-123">-Offer</span></span>
<span data-ttu-id="ada2f-124">Oferta obrazów z [galerii Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="ada2f-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ada2f-125">-PlanName</span></span>
<span data-ttu-id="ada2f-126">Nazwa planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="ada2f-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ada2f-127">-PlanProduct</span></span>
<span data-ttu-id="ada2f-128">Produkt planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="ada2f-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ada2f-129">-PlanPublisher</span></span>
<span data-ttu-id="ada2f-130">Wydawca planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="ada2f-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-131">— Publisher</span><span class="sxs-lookup"><span data-stu-id="ada2f-131">-Publisher</span></span>
<span data-ttu-id="ada2f-132">Obraz Programu Publisher w [galerii azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="ada2f-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="ada2f-133">-Sku</span></span>
<span data-ttu-id="ada2f-134">SKU obrazów z [galerii azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="ada2f-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="ada2f-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="ada2f-136">W tym artykule opisano źródło obrazu, które jest obrazem zarządzanym w subskrypcji klienta.</span><span class="sxs-lookup"><span data-stu-id="ada2f-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="ada2f-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="ada2f-138">W tym artykule opisano źródło obrazów z [galerii azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="ada2f-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="ada2f-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="ada2f-140">W tym artykule opisano źródło obrazów, które jest wersją obrazu w udostępnionej galerii obrazów.</span><span class="sxs-lookup"><span data-stu-id="ada2f-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-141">— Wersja</span><span class="sxs-lookup"><span data-stu-id="ada2f-141">-Version</span></span>
<span data-ttu-id="ada2f-142">Wersja obrazu z [galerii azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="ada2f-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada2f-143">CommonParameters</span></span>
<span data-ttu-id="ada2f-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada2f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada2f-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ada2f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada2f-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada2f-146">INPUTS</span></span>

## <span data-ttu-id="ada2f-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada2f-147">OUTPUTS</span></span>

### <span data-ttu-id="ada2f-148">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="ada2f-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="ada2f-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ada2f-149">NOTES</span></span>

<span data-ttu-id="ada2f-150">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ada2f-150">ALIASES</span></span>

## <span data-ttu-id="ada2f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada2f-151">RELATED LINKS</span></span>

