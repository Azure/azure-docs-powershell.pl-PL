---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222337"
---
# <span data-ttu-id="d3ae2-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="d3ae2-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="d3ae2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ae2-103">Zawiera opis źródła obrazu maszyny wirtualnej umożliwiającego tworzenie, dostosowywanie i dystrybucję.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="d3ae2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3ae2-104">SYNTAX</span></span>

### <span data-ttu-id="d3ae2-105">ManagedImage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d3ae2-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3ae2-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="d3ae2-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3ae2-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="d3ae2-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3ae2-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="d3ae2-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="d3ae2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d3ae2-109">DESCRIPTION</span></span>
<span data-ttu-id="d3ae2-110">Zawiera opis źródła obrazu maszyny wirtualnej umożliwiającego tworzenie, dostosowywanie i dystrybucję.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="d3ae2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3ae2-111">EXAMPLES</span></span>

### <span data-ttu-id="d3ae2-112">Przykład 1. Tworzenie źródła obrazu zarządzanego</span><span class="sxs-lookup"><span data-stu-id="d3ae2-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="d3ae2-113">To polecenie tworzy zarządzane źródło obrazu.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="d3ae2-114">Przykład 2: tworzenie źródła obrazu udostępnionego</span><span class="sxs-lookup"><span data-stu-id="d3ae2-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="d3ae2-115">To polecenie tworzy źródło obrazu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="d3ae2-116">Przykład 3: tworzenie źródła obrazu programu platfrom</span><span class="sxs-lookup"><span data-stu-id="d3ae2-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="d3ae2-117">To polecenie tworzy źródło obrazu w platfrom.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="d3ae2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3ae2-118">PARAMETERS</span></span>

### <span data-ttu-id="d3ae2-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="d3ae2-119">-ImageId</span></span>
<span data-ttu-id="d3ae2-120">Identyfikator zasobu ARM obrazu zarządzanego w subskrypcji klienta.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="d3ae2-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="d3ae2-121">-ImageVersionId</span></span>
<span data-ttu-id="d3ae2-122">Identyfikator zasobu ARM w wersji obrazu w galerii udostępnione obrazy.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="d3ae2-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="d3ae2-123">-Offer</span></span>
<span data-ttu-id="d3ae2-124">Oferta obrazu z [obrazów galerii platformy Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="d3ae2-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="d3ae2-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d3ae2-125">-PlanName</span></span>
<span data-ttu-id="d3ae2-126">Nazwa planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="d3ae2-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="d3ae2-127">-PlanProduct</span></span>
<span data-ttu-id="d3ae2-128">Iloczyn planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="d3ae2-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d3ae2-129">-PlanPublisher</span></span>
<span data-ttu-id="d3ae2-130">Wydawca planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="d3ae2-131">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="d3ae2-131">-Publisher</span></span>
<span data-ttu-id="d3ae2-132">Obraz programu Publisher w [obrazach galerii platformy Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="d3ae2-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="d3ae2-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="d3ae2-133">-Sku</span></span>
<span data-ttu-id="d3ae2-134">Obrazy SKU z [Galerii Azure Gallery](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="d3ae2-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="d3ae2-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="d3ae2-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="d3ae2-136">W tym artykule opisano źródło obrazu, które jest obrazem zarządzanym w subskrypcji klienta.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="d3ae2-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="d3ae2-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="d3ae2-138">Zawiera opis źródła obrazu z [obrazów galerii platformy Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="d3ae2-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="d3ae2-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="d3ae2-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="d3ae2-140">W tym artykule opisano źródło obrazu, które jest wersją obrazu w galerii obrazów udostępnionych.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="d3ae2-141">-Version</span><span class="sxs-lookup"><span data-stu-id="d3ae2-141">-Version</span></span>
<span data-ttu-id="d3ae2-142">Wersja obrazu z [obrazów galerii platformy Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="d3ae2-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="d3ae2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ae2-143">CommonParameters</span></span>
<span data-ttu-id="d3ae2-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ae2-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3ae2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ae2-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3ae2-146">INPUTS</span></span>

## <span data-ttu-id="d3ae2-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3ae2-147">OUTPUTS</span></span>

### <span data-ttu-id="d3ae2-148">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="d3ae2-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="d3ae2-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3ae2-149">NOTES</span></span>

<span data-ttu-id="d3ae2-150">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d3ae2-150">ALIASES</span></span>

## <span data-ttu-id="d3ae2-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3ae2-151">RELATED LINKS</span></span>

