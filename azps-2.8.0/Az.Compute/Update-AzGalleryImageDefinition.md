---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: d0a149f5ee2e03345cd433952d49748886c066ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706124"
---
# <span data-ttu-id="f0917-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f0917-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="f0917-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0917-102">SYNOPSIS</span></span>
<span data-ttu-id="f0917-103">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="f0917-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0917-104">SYNTAX</span></span>

### <span data-ttu-id="f0917-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f0917-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0917-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f0917-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0917-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f0917-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0917-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f0917-108">DESCRIPTION</span></span>
<span data-ttu-id="f0917-109">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="f0917-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0917-110">EXAMPLES</span></span>

### <span data-ttu-id="f0917-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0917-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="f0917-112">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="f0917-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0917-113">PARAMETERS</span></span>

### <span data-ttu-id="f0917-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0917-114">-AsJob</span></span>
<span data-ttu-id="f0917-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f0917-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0917-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0917-116">-DefaultProfile</span></span>
<span data-ttu-id="f0917-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0917-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0917-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="f0917-118">-Description</span></span>
<span data-ttu-id="f0917-119">Opis zasobu definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="f0917-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="f0917-120">-DisallowedDiskType</span></span>
<span data-ttu-id="f0917-121">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="f0917-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="f0917-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="f0917-122">-EndOfLifeDate</span></span>
<span data-ttu-id="f0917-123">Data zakończenia okresu użytkowania definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="f0917-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="f0917-124">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="f0917-124">-Eula</span></span>
<span data-ttu-id="f0917-125">Umowa licencyjna dotycząca definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="f0917-126">-Gallery</span><span class="sxs-lookup"><span data-stu-id="f0917-126">-GalleryName</span></span>
<span data-ttu-id="f0917-127">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="f0917-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0917-128">-InputObject</span></span>
<span data-ttu-id="f0917-129">Obiekt definicji obrazu galerii PS.</span><span class="sxs-lookup"><span data-stu-id="f0917-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="f0917-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="f0917-130">-MaximumMemory</span></span>
<span data-ttu-id="f0917-131">Maksymalnie zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="f0917-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="f0917-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="f0917-132">-MaximumVCPU</span></span>
<span data-ttu-id="f0917-133">Maksymalna liczba zalecanych rdzeni procesora</span><span class="sxs-lookup"><span data-stu-id="f0917-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="f0917-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="f0917-134">-MinimumMemory</span></span>
<span data-ttu-id="f0917-135">Minimalna zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="f0917-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="f0917-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="f0917-136">-MinimumVCPU</span></span>
<span data-ttu-id="f0917-137">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="f0917-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="f0917-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f0917-138">-Name</span></span>
<span data-ttu-id="f0917-139">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="f0917-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="f0917-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="f0917-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="f0917-141">Identyfikator URI oświadczenia o ochronie prywatności.</span><span class="sxs-lookup"><span data-stu-id="f0917-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="f0917-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="f0917-142">-PurchasePlanName</span></span>
<span data-ttu-id="f0917-143">Identyfikator planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="f0917-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f0917-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="f0917-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="f0917-145">Identyfikator produktu dla planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="f0917-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f0917-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f0917-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="f0917-147">IDENTYFIKATOR wydawcy planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="f0917-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="f0917-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="f0917-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="f0917-149">Identyfikator URI notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="f0917-149">The release note uri.</span></span>

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

### <span data-ttu-id="f0917-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0917-150">-ResourceGroupName</span></span>
<span data-ttu-id="f0917-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0917-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0917-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0917-152">-ResourceId</span></span>
<span data-ttu-id="f0917-153">Identyfikator zasobu dla definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="f0917-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="f0917-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0917-154">-Tag</span></span>
<span data-ttu-id="f0917-155">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="f0917-155">Resource tags</span></span>

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

### <span data-ttu-id="f0917-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0917-156">-Confirm</span></span>
<span data-ttu-id="f0917-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0917-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0917-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0917-158">-WhatIf</span></span>
<span data-ttu-id="f0917-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0917-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0917-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0917-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0917-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0917-161">CommonParameters</span></span>
<span data-ttu-id="f0917-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0917-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0917-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0917-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0917-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0917-164">INPUTS</span></span>

### <span data-ttu-id="f0917-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f0917-165">System.String</span></span>

### <span data-ttu-id="f0917-166">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="f0917-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="f0917-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f0917-167">System.DateTime</span></span>

### <span data-ttu-id="f0917-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0917-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f0917-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f0917-169">System.Int32</span></span>

### <span data-ttu-id="f0917-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="f0917-170">System.String[]</span></span>

## <span data-ttu-id="f0917-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0917-171">OUTPUTS</span></span>

### <span data-ttu-id="f0917-172">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="f0917-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="f0917-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0917-173">NOTES</span></span>

## <span data-ttu-id="f0917-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0917-174">RELATED LINKS</span></span>
