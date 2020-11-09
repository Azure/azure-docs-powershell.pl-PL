---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304026"
---
# <span data-ttu-id="52e6c-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="52e6c-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="52e6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="52e6c-103">Ogólny obiekt dystrybucyjny</span><span class="sxs-lookup"><span data-stu-id="52e6c-103">Generic distribution object</span></span>

## <span data-ttu-id="52e6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52e6c-104">SYNTAX</span></span>

### <span data-ttu-id="52e6c-105">ManagedImageDistributor (domyślny)</span><span class="sxs-lookup"><span data-stu-id="52e6c-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="52e6c-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="52e6c-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="52e6c-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="52e6c-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="52e6c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="52e6c-108">DESCRIPTION</span></span>
<span data-ttu-id="52e6c-109">Ogólny obiekt dystrybucyjny</span><span class="sxs-lookup"><span data-stu-id="52e6c-109">Generic distribution object</span></span>

## <span data-ttu-id="52e6c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52e6c-110">EXAMPLES</span></span>

### <span data-ttu-id="52e6c-111">Przykład 1. Tworzenie zarządzanego dystrybutora obrazu</span><span class="sxs-lookup"><span data-stu-id="52e6c-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="52e6c-112">To polecenie umożliwia utworzenie zarządzanego dystrybutora obrazu.</span><span class="sxs-lookup"><span data-stu-id="52e6c-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="52e6c-113">Przykład 2: Tworzenie dystrybutora VHD</span><span class="sxs-lookup"><span data-stu-id="52e6c-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="52e6c-114">To polecenie tworzy dystrybutora VHD.</span><span class="sxs-lookup"><span data-stu-id="52e6c-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="52e6c-115">Przykład 3: Tworzenie współużytkowanego obrazu</span><span class="sxs-lookup"><span data-stu-id="52e6c-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="52e6c-116">To polecenie tworzy udostępniony dystrybutor obrazu.</span><span class="sxs-lookup"><span data-stu-id="52e6c-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="52e6c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52e6c-117">PARAMETERS</span></span>

### <span data-ttu-id="52e6c-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="52e6c-118">-ArtifactTag</span></span>
<span data-ttu-id="52e6c-119">Tagi, które zostaną zastosowane do artefaktu po jego utworzeniu/zaktualizowaniu przez dystrybutora.</span><span class="sxs-lookup"><span data-stu-id="52e6c-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="52e6c-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="52e6c-121">Flaga wskazująca, czy utworzona wersja obrazu powinna być wykluczona z najnowszej.</span><span class="sxs-lookup"><span data-stu-id="52e6c-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="52e6c-122">Pomiń, aby użyć wartości domyślnej (FAŁSZ).</span><span class="sxs-lookup"><span data-stu-id="52e6c-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="52e6c-123">-GalleryImageId</span></span>
<span data-ttu-id="52e6c-124">Identyfikator zasobu obrazu galerii udostępnione obrazy.</span><span class="sxs-lookup"><span data-stu-id="52e6c-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="52e6c-125">-ImageId</span></span>
<span data-ttu-id="52e6c-126">Identyfikator zasobu obrazu dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="52e6c-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52e6c-127">-Location</span></span>
<span data-ttu-id="52e6c-128">Lokalizacja na platformie Azure obrazu powinna być zgodna, jeśli obraz już istnieje.</span><span class="sxs-lookup"><span data-stu-id="52e6c-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="52e6c-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="52e6c-130">Dystrybuuj jako obraz dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="52e6c-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="52e6c-131">-ReplicationRegion</span></span>
<span data-ttu-id="52e6c-132">Lista regionów, do których będzie replikowany obraz.</span><span class="sxs-lookup"><span data-stu-id="52e6c-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="52e6c-133">-RunOutputName</span></span>
<span data-ttu-id="52e6c-134">Nazwa, która ma być używana dla skojarzonych RunOutput.</span><span class="sxs-lookup"><span data-stu-id="52e6c-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="52e6c-135">-SharedImageDistributor</span></span>
<span data-ttu-id="52e6c-136">Dystrybucja za pośrednictwem galerii obrazów udostępnionych.</span><span class="sxs-lookup"><span data-stu-id="52e6c-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="52e6c-137">-StorageAccountType</span></span>
<span data-ttu-id="52e6c-138">Typ konta magazynu, który ma być wykorzystywany do przechowywania obrazu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="52e6c-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="52e6c-139">Pomiń, aby użyć domyślnego (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="52e6c-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="52e6c-140">-VhdDistributor</span></span>
<span data-ttu-id="52e6c-141">Rozpowszechnianie za pośrednictwem wirtualnego dysku twardego na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="52e6c-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e6c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e6c-142">CommonParameters</span></span>
<span data-ttu-id="52e6c-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e6c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e6c-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52e6c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e6c-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52e6c-145">INPUTS</span></span>

## <span data-ttu-id="52e6c-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52e6c-146">OUTPUTS</span></span>

### <span data-ttu-id="52e6c-147">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="52e6c-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="52e6c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52e6c-148">NOTES</span></span>

<span data-ttu-id="52e6c-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="52e6c-149">ALIASES</span></span>

## <span data-ttu-id="52e6c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52e6c-150">RELATED LINKS</span></span>

