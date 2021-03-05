---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 09871f6d7876b5f197af515f531c85b8bf6a3d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972065"
---
# <span data-ttu-id="e7ebf-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e7ebf-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="e7ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ebf-103">Aktualizowanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="e7ebf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7ebf-104">SYNTAX</span></span>

### <span data-ttu-id="e7ebf-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7ebf-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ebf-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="e7ebf-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ebf-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="e7ebf-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7ebf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7ebf-108">DESCRIPTION</span></span>
<span data-ttu-id="e7ebf-109">Aktualizowanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="e7ebf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7ebf-110">EXAMPLES</span></span>

### <span data-ttu-id="e7ebf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7ebf-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="e7ebf-112">Aktualizowanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="e7ebf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7ebf-113">PARAMETERS</span></span>

### <span data-ttu-id="e7ebf-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e7ebf-114">-AsJob</span></span>
<span data-ttu-id="e7ebf-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e7ebf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7ebf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ebf-116">-DefaultProfile</span></span>
<span data-ttu-id="e7ebf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ebf-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="e7ebf-118">-Description</span></span>
<span data-ttu-id="e7ebf-119">Opis galerii obrazu zasobu Definicji.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="e7ebf-120">-Disallowed PrzekwalifikowanyTyp</span><span class="sxs-lookup"><span data-stu-id="e7ebf-120">-DisallowedDiskType</span></span>
<span data-ttu-id="e7ebf-121">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="e7ebf-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="e7ebf-122">-EndOfLifeDate</span></span>
<span data-ttu-id="e7ebf-123">Data zakończenia użytkowania galerii Definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="e7ebf-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="e7ebf-124">- Eula</span><span class="sxs-lookup"><span data-stu-id="e7ebf-124">-Eula</span></span>
<span data-ttu-id="e7ebf-125">Umowa Eula dla galerii Definicji obrazów.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="e7ebf-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="e7ebf-126">-GalleryName</span></span>
<span data-ttu-id="e7ebf-127">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="e7ebf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7ebf-128">-InputObject</span></span>
<span data-ttu-id="e7ebf-129">Obiekt definicji obrazów w galerii PS.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="e7ebf-130">- MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="e7ebf-130">-MaximumMemory</span></span>
<span data-ttu-id="e7ebf-131">Maksymalna ilość zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="e7ebf-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="e7ebf-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="e7ebf-132">-MaximumVCPU</span></span>
<span data-ttu-id="e7ebf-133">Maksimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="e7ebf-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="e7ebf-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="e7ebf-134">-MinimumMemory</span></span>
<span data-ttu-id="e7ebf-135">Minimalny poziom zalecanej pamięci</span><span class="sxs-lookup"><span data-stu-id="e7ebf-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="e7ebf-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="e7ebf-136">-MinimumVCPU</span></span>
<span data-ttu-id="e7ebf-137">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="e7ebf-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="e7ebf-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7ebf-138">-Name</span></span>
<span data-ttu-id="e7ebf-139">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="e7ebf-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="e7ebf-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="e7ebf-141">Uri zasad zachowania poufności informacji.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="e7ebf-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="e7ebf-142">-PurchasePlanName</span></span>
<span data-ttu-id="e7ebf-143">Identyfikator planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e7ebf-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="e7ebf-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="e7ebf-145">Identyfikator produktu planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e7ebf-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="e7ebf-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="e7ebf-147">Identyfikator wydawcy planu zakupu.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e7ebf-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="e7ebf-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="e7ebf-149">Uri notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-149">The release note uri.</span></span>

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

### <span data-ttu-id="e7ebf-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ebf-150">-ResourceGroupName</span></span>
<span data-ttu-id="e7ebf-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7ebf-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ebf-152">-ResourceId</span></span>
<span data-ttu-id="e7ebf-153">Identyfikator zasobu dla definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="e7ebf-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="e7ebf-154">— Tag</span><span class="sxs-lookup"><span data-stu-id="e7ebf-154">-Tag</span></span>
<span data-ttu-id="e7ebf-155">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="e7ebf-155">Resource tags</span></span>

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

### <span data-ttu-id="e7ebf-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7ebf-156">-Confirm</span></span>
<span data-ttu-id="e7ebf-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ebf-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ebf-158">-WhatIf</span></span>
<span data-ttu-id="e7ebf-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ebf-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ebf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ebf-161">CommonParameters</span></span>
<span data-ttu-id="e7ebf-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ebf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ebf-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7ebf-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ebf-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7ebf-164">INPUTS</span></span>

### <span data-ttu-id="e7ebf-165">System.String</span><span class="sxs-lookup"><span data-stu-id="e7ebf-165">System.String</span></span>

### <span data-ttu-id="e7ebf-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e7ebf-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="e7ebf-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="e7ebf-167">System.DateTime</span></span>

### <span data-ttu-id="e7ebf-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7ebf-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e7ebf-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e7ebf-169">System.Int32</span></span>

### <span data-ttu-id="e7ebf-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e7ebf-170">System.String[]</span></span>

## <span data-ttu-id="e7ebf-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7ebf-171">OUTPUTS</span></span>

### <span data-ttu-id="e7ebf-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e7ebf-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="e7ebf-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7ebf-173">NOTES</span></span>

## <span data-ttu-id="e7ebf-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7ebf-174">RELATED LINKS</span></span>
