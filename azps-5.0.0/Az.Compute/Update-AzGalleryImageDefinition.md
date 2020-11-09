---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304177"
---
# <span data-ttu-id="fc5d5-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fc5d5-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="fc5d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5d5-103">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="fc5d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc5d5-104">SYNTAX</span></span>

### <span data-ttu-id="fc5d5-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc5d5-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5d5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fc5d5-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc5d5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fc5d5-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc5d5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc5d5-108">DESCRIPTION</span></span>
<span data-ttu-id="fc5d5-109">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="fc5d5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc5d5-110">EXAMPLES</span></span>

### <span data-ttu-id="fc5d5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc5d5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="fc5d5-112">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="fc5d5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc5d5-113">PARAMETERS</span></span>

### <span data-ttu-id="fc5d5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc5d5-114">-AsJob</span></span>
<span data-ttu-id="fc5d5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fc5d5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc5d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5d5-116">-DefaultProfile</span></span>
<span data-ttu-id="fc5d5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5d5-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="fc5d5-118">-Description</span></span>
<span data-ttu-id="fc5d5-119">Opis zasobu definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="fc5d5-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="fc5d5-120">-DisallowedDiskType</span></span>
<span data-ttu-id="fc5d5-121">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="fc5d5-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="fc5d5-122">-EndOfLifeDate</span></span>
<span data-ttu-id="fc5d5-123">Data zakończenia okresu użytkowania definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="fc5d5-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="fc5d5-124">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="fc5d5-124">-Eula</span></span>
<span data-ttu-id="fc5d5-125">Umowa licencyjna dotycząca definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="fc5d5-126">-Gallery</span><span class="sxs-lookup"><span data-stu-id="fc5d5-126">-GalleryName</span></span>
<span data-ttu-id="fc5d5-127">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="fc5d5-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc5d5-128">-InputObject</span></span>
<span data-ttu-id="fc5d5-129">Obiekt definicji obrazu galerii PS.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="fc5d5-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="fc5d5-130">-MaximumMemory</span></span>
<span data-ttu-id="fc5d5-131">Maksymalnie zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="fc5d5-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="fc5d5-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="fc5d5-132">-MaximumVCPU</span></span>
<span data-ttu-id="fc5d5-133">Maksymalna liczba zalecanych rdzeni procesora</span><span class="sxs-lookup"><span data-stu-id="fc5d5-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fc5d5-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="fc5d5-134">-MinimumMemory</span></span>
<span data-ttu-id="fc5d5-135">Minimalna zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="fc5d5-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="fc5d5-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="fc5d5-136">-MinimumVCPU</span></span>
<span data-ttu-id="fc5d5-137">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="fc5d5-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fc5d5-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc5d5-138">-Name</span></span>
<span data-ttu-id="fc5d5-139">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="fc5d5-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="fc5d5-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="fc5d5-141">Identyfikator URI oświadczenia o ochronie prywatności.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="fc5d5-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="fc5d5-142">-PurchasePlanName</span></span>
<span data-ttu-id="fc5d5-143">Identyfikator planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fc5d5-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="fc5d5-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="fc5d5-145">Identyfikator produktu dla planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fc5d5-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fc5d5-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="fc5d5-147">IDENTYFIKATOR wydawcy planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fc5d5-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="fc5d5-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="fc5d5-149">Identyfikator URI notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-149">The release note uri.</span></span>

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

### <span data-ttu-id="fc5d5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5d5-150">-ResourceGroupName</span></span>
<span data-ttu-id="fc5d5-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc5d5-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc5d5-152">-ResourceId</span></span>
<span data-ttu-id="fc5d5-153">Identyfikator zasobu dla definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="fc5d5-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="fc5d5-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc5d5-154">-Tag</span></span>
<span data-ttu-id="fc5d5-155">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="fc5d5-155">Resource tags</span></span>

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

### <span data-ttu-id="fc5d5-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc5d5-156">-Confirm</span></span>
<span data-ttu-id="fc5d5-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5d5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5d5-158">-WhatIf</span></span>
<span data-ttu-id="fc5d5-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5d5-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5d5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5d5-161">CommonParameters</span></span>
<span data-ttu-id="fc5d5-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc5d5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5d5-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc5d5-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5d5-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc5d5-164">INPUTS</span></span>

### <span data-ttu-id="fc5d5-165">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5d5-165">System.String</span></span>

### <span data-ttu-id="fc5d5-166">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fc5d5-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="fc5d5-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fc5d5-167">System.DateTime</span></span>

### <span data-ttu-id="fc5d5-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc5d5-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fc5d5-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fc5d5-169">System.Int32</span></span>

### <span data-ttu-id="fc5d5-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="fc5d5-170">System.String[]</span></span>

## <span data-ttu-id="fc5d5-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc5d5-171">OUTPUTS</span></span>

### <span data-ttu-id="fc5d5-172">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fc5d5-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="fc5d5-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc5d5-173">NOTES</span></span>

## <span data-ttu-id="fc5d5-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc5d5-174">RELATED LINKS</span></span>
