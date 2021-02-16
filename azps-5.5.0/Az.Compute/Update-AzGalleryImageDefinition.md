---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194978"
---
# <span data-ttu-id="9dd8e-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="9dd8e-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="9dd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd8e-103">Aktualizowanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="9dd8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9dd8e-104">SYNTAX</span></span>

### <span data-ttu-id="9dd8e-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9dd8e-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dd8e-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="9dd8e-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dd8e-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="9dd8e-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd8e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9dd8e-108">DESCRIPTION</span></span>
<span data-ttu-id="9dd8e-109">Aktualizowanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="9dd8e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9dd8e-110">EXAMPLES</span></span>

### <span data-ttu-id="9dd8e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9dd8e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="9dd8e-112">Aktualizowanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="9dd8e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dd8e-113">PARAMETERS</span></span>

### <span data-ttu-id="9dd8e-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9dd8e-114">-AsJob</span></span>
<span data-ttu-id="9dd8e-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9dd8e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dd8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd8e-116">-DefaultProfile</span></span>
<span data-ttu-id="9dd8e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd8e-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="9dd8e-118">-Description</span></span>
<span data-ttu-id="9dd8e-119">Opis galerii zasobu definicji obrazu.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="9dd8e-120">-Disallowed Jednakowy</span><span class="sxs-lookup"><span data-stu-id="9dd8e-120">-DisallowedDiskType</span></span>
<span data-ttu-id="9dd8e-121">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="9dd8e-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="9dd8e-122">-EndOfLifeDate</span></span>
<span data-ttu-id="9dd8e-123">Data zakończenia użytkowania galerii Definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="9dd8e-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="9dd8e-124">- Eula</span><span class="sxs-lookup"><span data-stu-id="9dd8e-124">-Eula</span></span>
<span data-ttu-id="9dd8e-125">Umowa Eula dla galerii Definicji obrazów.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="9dd8e-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="9dd8e-126">-GalleryName</span></span>
<span data-ttu-id="9dd8e-127">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="9dd8e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dd8e-128">-InputObject</span></span>
<span data-ttu-id="9dd8e-129">Obiekt definicji obrazów w galerii PS.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd8e-130">- MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="9dd8e-130">-MaximumMemory</span></span>
<span data-ttu-id="9dd8e-131">Maksymalna ilość zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="9dd8e-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="9dd8e-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="9dd8e-132">-MaximumVCPU</span></span>
<span data-ttu-id="9dd8e-133">Maksimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="9dd8e-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="9dd8e-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="9dd8e-134">-MinimumMemory</span></span>
<span data-ttu-id="9dd8e-135">Minimalny poziom zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="9dd8e-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="9dd8e-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="9dd8e-136">-MinimumVCPU</span></span>
<span data-ttu-id="9dd8e-137">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="9dd8e-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="9dd8e-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9dd8e-138">-Name</span></span>
<span data-ttu-id="9dd8e-139">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd8e-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="9dd8e-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="9dd8e-141">Uri zasad zachowania poufności informacji.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="9dd8e-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="9dd8e-142">-PurchasePlanName</span></span>
<span data-ttu-id="9dd8e-143">Identyfikator planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9dd8e-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="9dd8e-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="9dd8e-145">Identyfikator produktu planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9dd8e-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9dd8e-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="9dd8e-147">Identyfikator wydawcy planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9dd8e-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="9dd8e-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="9dd8e-149">Uri notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-149">The release note uri.</span></span>

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

### <span data-ttu-id="9dd8e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd8e-150">-ResourceGroupName</span></span>
<span data-ttu-id="9dd8e-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="9dd8e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd8e-152">-ResourceId</span></span>
<span data-ttu-id="9dd8e-153">Identyfikator zasobu dla definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="9dd8e-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="9dd8e-154">— Tag</span><span class="sxs-lookup"><span data-stu-id="9dd8e-154">-Tag</span></span>
<span data-ttu-id="9dd8e-155">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="9dd8e-155">Resource tags</span></span>

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

### <span data-ttu-id="9dd8e-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9dd8e-156">-Confirm</span></span>
<span data-ttu-id="9dd8e-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd8e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd8e-158">-WhatIf</span></span>
<span data-ttu-id="9dd8e-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd8e-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd8e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd8e-161">CommonParameters</span></span>
<span data-ttu-id="9dd8e-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd8e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd8e-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dd8e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd8e-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dd8e-164">INPUTS</span></span>

### <span data-ttu-id="9dd8e-165">System.String</span><span class="sxs-lookup"><span data-stu-id="9dd8e-165">System.String</span></span>

### <span data-ttu-id="9dd8e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="9dd8e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="9dd8e-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="9dd8e-167">System.DateTime</span></span>

### <span data-ttu-id="9dd8e-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9dd8e-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9dd8e-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9dd8e-169">System.Int32</span></span>

### <span data-ttu-id="9dd8e-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9dd8e-170">System.String[]</span></span>

## <span data-ttu-id="9dd8e-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dd8e-171">OUTPUTS</span></span>

### <span data-ttu-id="9dd8e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="9dd8e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="9dd8e-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9dd8e-173">NOTES</span></span>

## <span data-ttu-id="9dd8e-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9dd8e-174">RELATED LINKS</span></span>
