---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177706"
---
# <span data-ttu-id="59f34-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="59f34-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="59f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f34-102">SYNOPSIS</span></span>
<span data-ttu-id="59f34-103">Utwórz definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="59f34-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="59f34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59f34-104">SYNTAX</span></span>

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

## <span data-ttu-id="59f34-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="59f34-105">DESCRIPTION</span></span>
<span data-ttu-id="59f34-106">Utwórz definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="59f34-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="59f34-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59f34-107">EXAMPLES</span></span>

### <span data-ttu-id="59f34-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59f34-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="59f34-109">Utwórz definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="59f34-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="59f34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59f34-110">PARAMETERS</span></span>

### <span data-ttu-id="59f34-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="59f34-111">-AsJob</span></span>
<span data-ttu-id="59f34-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="59f34-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59f34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f34-113">-DefaultProfile</span></span>
<span data-ttu-id="59f34-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59f34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f34-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="59f34-115">-Description</span></span>
<span data-ttu-id="59f34-116">Opis galerii zasobu definicji obrazu.</span><span class="sxs-lookup"><span data-stu-id="59f34-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="59f34-117">-Disallowed Jednakowy</span><span class="sxs-lookup"><span data-stu-id="59f34-117">-DisallowedDiskType</span></span>
<span data-ttu-id="59f34-118">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="59f34-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="59f34-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="59f34-119">-EndOfLifeDate</span></span>
<span data-ttu-id="59f34-120">Data zakończenia użytkowania galerii Definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="59f34-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="59f34-121">- Eula</span><span class="sxs-lookup"><span data-stu-id="59f34-121">-Eula</span></span>
<span data-ttu-id="59f34-122">Umowa Eula dla galerii Definicji obrazów.</span><span class="sxs-lookup"><span data-stu-id="59f34-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="59f34-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="59f34-123">-GalleryName</span></span>
<span data-ttu-id="59f34-124">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="59f34-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="59f34-125">—HyperV Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="59f34-125">-HyperVGeneration</span></span>
<span data-ttu-id="59f34-126">Generowanie hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="59f34-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="59f34-127">Dotyczy tylko dyskietek systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="59f34-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="59f34-128">Dozwolone wartości to V1 i V2.</span><span class="sxs-lookup"><span data-stu-id="59f34-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="59f34-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="59f34-129">-Location</span></span>
<span data-ttu-id="59f34-130">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="59f34-130">Resource location</span></span>

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

### <span data-ttu-id="59f34-131">- MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="59f34-131">-MaximumMemory</span></span>
<span data-ttu-id="59f34-132">Maksymalna ilość zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="59f34-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="59f34-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="59f34-133">-MaximumVCPU</span></span>
<span data-ttu-id="59f34-134">Maksimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="59f34-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="59f34-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="59f34-135">-MinimumMemory</span></span>
<span data-ttu-id="59f34-136">Minimalny poziom zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="59f34-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="59f34-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="59f34-137">-MinimumVCPU</span></span>
<span data-ttu-id="59f34-138">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="59f34-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="59f34-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59f34-139">-Name</span></span>
<span data-ttu-id="59f34-140">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="59f34-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="59f34-141">— Oferta</span><span class="sxs-lookup"><span data-stu-id="59f34-141">-Offer</span></span>
<span data-ttu-id="59f34-142">Nazwa oferty galerii Definicji obrazów.</span><span class="sxs-lookup"><span data-stu-id="59f34-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="59f34-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="59f34-143">-OsState</span></span>
<span data-ttu-id="59f34-144">Stan systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="59f34-144">The state of OS</span></span>

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

### <span data-ttu-id="59f34-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="59f34-145">-OsType</span></span>
<span data-ttu-id="59f34-146">Typ systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="59f34-146">The type of OS</span></span>

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

### <span data-ttu-id="59f34-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="59f34-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="59f34-148">Uri zasad zachowania poufności informacji.</span><span class="sxs-lookup"><span data-stu-id="59f34-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="59f34-149">— Publisher</span><span class="sxs-lookup"><span data-stu-id="59f34-149">-Publisher</span></span>
<span data-ttu-id="59f34-150">Nazwa wydawcy definicji obrazów galerii.</span><span class="sxs-lookup"><span data-stu-id="59f34-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="59f34-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="59f34-151">-PurchasePlanName</span></span>
<span data-ttu-id="59f34-152">Identyfikator planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="59f34-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="59f34-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="59f34-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="59f34-154">Identyfikator produktu planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="59f34-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="59f34-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="59f34-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="59f34-156">Identyfikator wydawcy planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="59f34-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="59f34-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="59f34-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="59f34-158">Uri notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="59f34-158">The release note uri.</span></span>

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

### <span data-ttu-id="59f34-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f34-159">-ResourceGroupName</span></span>
<span data-ttu-id="59f34-160">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59f34-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="59f34-161">- SKU</span><span class="sxs-lookup"><span data-stu-id="59f34-161">-Sku</span></span>
<span data-ttu-id="59f34-162">Nazwa galerii SKU definicji obrazu.</span><span class="sxs-lookup"><span data-stu-id="59f34-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="59f34-163">— Tag</span><span class="sxs-lookup"><span data-stu-id="59f34-163">-Tag</span></span>
<span data-ttu-id="59f34-164">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="59f34-164">Resource tags</span></span>

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

### <span data-ttu-id="59f34-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59f34-165">-Confirm</span></span>
<span data-ttu-id="59f34-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59f34-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f34-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f34-167">-WhatIf</span></span>
<span data-ttu-id="59f34-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59f34-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f34-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="59f34-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f34-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f34-170">CommonParameters</span></span>
<span data-ttu-id="59f34-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f34-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f34-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59f34-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f34-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59f34-173">INPUTS</span></span>

### <span data-ttu-id="59f34-174">System.String</span><span class="sxs-lookup"><span data-stu-id="59f34-174">System.String</span></span>

### <span data-ttu-id="59f34-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="59f34-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="59f34-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="59f34-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="59f34-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="59f34-177">System.DateTime</span></span>

### <span data-ttu-id="59f34-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="59f34-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="59f34-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="59f34-179">System.Int32</span></span>

### <span data-ttu-id="59f34-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="59f34-180">System.String[]</span></span>

## <span data-ttu-id="59f34-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59f34-181">OUTPUTS</span></span>

### <span data-ttu-id="59f34-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="59f34-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="59f34-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59f34-183">NOTES</span></span>

## <span data-ttu-id="59f34-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59f34-184">RELATED LINKS</span></span>
