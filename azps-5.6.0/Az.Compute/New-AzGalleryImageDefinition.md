---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: fbfb0a10016d81edcffeb62580b1ca0ff9b5b341
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957569"
---
# <span data-ttu-id="243e6-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="243e6-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="243e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="243e6-102">SYNOPSIS</span></span>
<span data-ttu-id="243e6-103">Utwórz definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="243e6-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="243e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="243e6-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="243e6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="243e6-105">DESCRIPTION</span></span>
<span data-ttu-id="243e6-106">Utwórz definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="243e6-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="243e6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="243e6-107">EXAMPLES</span></span>

### <span data-ttu-id="243e6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="243e6-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="243e6-109">Utwórz definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="243e6-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="243e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="243e6-110">PARAMETERS</span></span>

### <span data-ttu-id="243e6-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="243e6-111">-AsJob</span></span>
<span data-ttu-id="243e6-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="243e6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="243e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243e6-113">-DefaultProfile</span></span>
<span data-ttu-id="243e6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="243e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="243e6-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="243e6-115">-Description</span></span>
<span data-ttu-id="243e6-116">Opis galerii obrazu zasobu Definicji.</span><span class="sxs-lookup"><span data-stu-id="243e6-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="243e6-117">-Disallowed PrzekwalifikowanyTyp</span><span class="sxs-lookup"><span data-stu-id="243e6-117">-DisallowedDiskType</span></span>
<span data-ttu-id="243e6-118">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="243e6-118">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="243e6-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="243e6-119">-EndOfLifeDate</span></span>
<span data-ttu-id="243e6-120">Data zakończenia użytkowania galerii Definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="243e6-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="243e6-121">- Eula</span><span class="sxs-lookup"><span data-stu-id="243e6-121">-Eula</span></span>
<span data-ttu-id="243e6-122">Umowa Eula dla galerii Definicji obrazów.</span><span class="sxs-lookup"><span data-stu-id="243e6-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="243e6-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="243e6-123">-GalleryName</span></span>
<span data-ttu-id="243e6-124">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="243e6-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="243e6-125">-HyperV Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="243e6-125">-HyperVGeneration</span></span>
<span data-ttu-id="243e6-126">Generowanie hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="243e6-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="243e6-127">Dotyczy tylko dyskietek systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="243e6-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="243e6-128">Dozwolone wartości to V1 i V2.</span><span class="sxs-lookup"><span data-stu-id="243e6-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="243e6-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="243e6-129">-Location</span></span>
<span data-ttu-id="243e6-130">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="243e6-130">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="243e6-131">- MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="243e6-131">-MaximumMemory</span></span>
<span data-ttu-id="243e6-132">Maksymalna ilość zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="243e6-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="243e6-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="243e6-133">-MaximumVCPU</span></span>
<span data-ttu-id="243e6-134">Maksimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="243e6-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="243e6-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="243e6-135">-MinimumMemory</span></span>
<span data-ttu-id="243e6-136">Minimalny poziom zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="243e6-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="243e6-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="243e6-137">-MinimumVCPU</span></span>
<span data-ttu-id="243e6-138">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="243e6-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="243e6-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="243e6-139">-Name</span></span>
<span data-ttu-id="243e6-140">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="243e6-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="243e6-141">— Oferta</span><span class="sxs-lookup"><span data-stu-id="243e6-141">-Offer</span></span>
<span data-ttu-id="243e6-142">Nazwa oferty galerii Definicji obrazów.</span><span class="sxs-lookup"><span data-stu-id="243e6-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="243e6-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="243e6-143">-OsState</span></span>
<span data-ttu-id="243e6-144">Stan systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="243e6-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="243e6-145">- OsType</span><span class="sxs-lookup"><span data-stu-id="243e6-145">-OsType</span></span>
<span data-ttu-id="243e6-146">Typ systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="243e6-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="243e6-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="243e6-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="243e6-148">Uri zasad zachowania poufności informacji.</span><span class="sxs-lookup"><span data-stu-id="243e6-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="243e6-149">— Publisher</span><span class="sxs-lookup"><span data-stu-id="243e6-149">-Publisher</span></span>
<span data-ttu-id="243e6-150">Nazwa wydawcy definicji obrazów galerii.</span><span class="sxs-lookup"><span data-stu-id="243e6-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="243e6-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="243e6-151">-PurchasePlanName</span></span>
<span data-ttu-id="243e6-152">Identyfikator planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="243e6-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="243e6-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="243e6-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="243e6-154">Identyfikator produktu planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="243e6-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="243e6-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="243e6-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="243e6-156">Identyfikator wydawcy planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="243e6-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="243e6-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="243e6-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="243e6-158">Uri notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="243e6-158">The release note uri.</span></span>

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

### <span data-ttu-id="243e6-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="243e6-159">-ResourceGroupName</span></span>
<span data-ttu-id="243e6-160">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="243e6-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="243e6-161">- SKU</span><span class="sxs-lookup"><span data-stu-id="243e6-161">-Sku</span></span>
<span data-ttu-id="243e6-162">Nazwa galerii SKU definicji obrazu.</span><span class="sxs-lookup"><span data-stu-id="243e6-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="243e6-163">— Tag</span><span class="sxs-lookup"><span data-stu-id="243e6-163">-Tag</span></span>
<span data-ttu-id="243e6-164">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="243e6-164">Resource tags</span></span>

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

### <span data-ttu-id="243e6-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="243e6-165">-Confirm</span></span>
<span data-ttu-id="243e6-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="243e6-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="243e6-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="243e6-167">-WhatIf</span></span>
<span data-ttu-id="243e6-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="243e6-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="243e6-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="243e6-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="243e6-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243e6-170">CommonParameters</span></span>
<span data-ttu-id="243e6-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243e6-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243e6-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="243e6-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243e6-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="243e6-173">INPUTS</span></span>

### <span data-ttu-id="243e6-174">System.String</span><span class="sxs-lookup"><span data-stu-id="243e6-174">System.String</span></span>

### <span data-ttu-id="243e6-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="243e6-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="243e6-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="243e6-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="243e6-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="243e6-177">System.DateTime</span></span>

### <span data-ttu-id="243e6-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="243e6-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="243e6-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="243e6-179">System.Int32</span></span>

### <span data-ttu-id="243e6-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="243e6-180">System.String[]</span></span>

## <span data-ttu-id="243e6-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="243e6-181">OUTPUTS</span></span>

### <span data-ttu-id="243e6-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="243e6-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="243e6-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="243e6-183">NOTES</span></span>

## <span data-ttu-id="243e6-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="243e6-184">RELATED LINKS</span></span>
