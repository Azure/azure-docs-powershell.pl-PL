---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 338e65e4795f3b676a1f88e8a8281a41aee5a0c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868836"
---
# <span data-ttu-id="9bbb8-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="9bbb8-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="9bbb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bbb8-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbb8-103">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="9bbb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bbb8-104">SYNTAX</span></span>

### <span data-ttu-id="9bbb8-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bbb8-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bbb8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9bbb8-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bbb8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9bbb8-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bbb8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9bbb8-108">DESCRIPTION</span></span>
<span data-ttu-id="9bbb8-109">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="9bbb8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bbb8-110">EXAMPLES</span></span>

### <span data-ttu-id="9bbb8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bbb8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="9bbb8-112">Aktualizowanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="9bbb8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bbb8-113">PARAMETERS</span></span>

### <span data-ttu-id="9bbb8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bbb8-114">-AsJob</span></span>
<span data-ttu-id="9bbb8-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9bbb8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bbb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbb8-116">-DefaultProfile</span></span>
<span data-ttu-id="9bbb8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bbb8-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="9bbb8-118">-Description</span></span>
<span data-ttu-id="9bbb8-119">Opis zasobu definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="9bbb8-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="9bbb8-120">-DisallowedDiskType</span></span>
<span data-ttu-id="9bbb8-121">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="9bbb8-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="9bbb8-122">-EndOfLifeDate</span></span>
<span data-ttu-id="9bbb8-123">Data zakończenia okresu użytkowania definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="9bbb8-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="9bbb8-124">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="9bbb8-124">-Eula</span></span>
<span data-ttu-id="9bbb8-125">Umowa licencyjna dotycząca definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="9bbb8-126">-Gallery</span><span class="sxs-lookup"><span data-stu-id="9bbb8-126">-GalleryName</span></span>
<span data-ttu-id="9bbb8-127">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="9bbb8-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bbb8-128">-InputObject</span></span>
<span data-ttu-id="9bbb8-129">Obiekt definicji obrazu galerii PS.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="9bbb8-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="9bbb8-130">-MaximumMemory</span></span>
<span data-ttu-id="9bbb8-131">Maksymalnie zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="9bbb8-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="9bbb8-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="9bbb8-132">-MaximumVCPU</span></span>
<span data-ttu-id="9bbb8-133">Maksymalna liczba zalecanych rdzeni procesora</span><span class="sxs-lookup"><span data-stu-id="9bbb8-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="9bbb8-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="9bbb8-134">-MinimumMemory</span></span>
<span data-ttu-id="9bbb8-135">Minimalna zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="9bbb8-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="9bbb8-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="9bbb8-136">-MinimumVCPU</span></span>
<span data-ttu-id="9bbb8-137">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="9bbb8-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="9bbb8-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bbb8-138">-Name</span></span>
<span data-ttu-id="9bbb8-139">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="9bbb8-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="9bbb8-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="9bbb8-141">Identyfikator URI oświadczenia o ochronie prywatności.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="9bbb8-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="9bbb8-142">-PurchasePlanName</span></span>
<span data-ttu-id="9bbb8-143">Identyfikator planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9bbb8-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="9bbb8-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="9bbb8-145">Identyfikator produktu dla planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9bbb8-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9bbb8-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="9bbb8-147">IDENTYFIKATOR wydawcy planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9bbb8-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="9bbb8-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="9bbb8-149">Identyfikator URI notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-149">The release note uri.</span></span>

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

### <span data-ttu-id="9bbb8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bbb8-150">-ResourceGroupName</span></span>
<span data-ttu-id="9bbb8-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bbb8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bbb8-152">-ResourceId</span></span>
<span data-ttu-id="9bbb8-153">Identyfikator zasobu dla definicji obrazu</span><span class="sxs-lookup"><span data-stu-id="9bbb8-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="9bbb8-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bbb8-154">-Tag</span></span>
<span data-ttu-id="9bbb8-155">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="9bbb8-155">Resource tags</span></span>

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

### <span data-ttu-id="9bbb8-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bbb8-156">-Confirm</span></span>
<span data-ttu-id="9bbb8-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bbb8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bbb8-158">-WhatIf</span></span>
<span data-ttu-id="9bbb8-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bbb8-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bbb8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbb8-161">CommonParameters</span></span>
<span data-ttu-id="9bbb8-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bbb8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbb8-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bbb8-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbb8-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bbb8-164">INPUTS</span></span>

### <span data-ttu-id="9bbb8-165">System. String</span><span class="sxs-lookup"><span data-stu-id="9bbb8-165">System.String</span></span>

### <span data-ttu-id="9bbb8-166">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="9bbb8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="9bbb8-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="9bbb8-167">System.DateTime</span></span>

### <span data-ttu-id="9bbb8-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9bbb8-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9bbb8-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9bbb8-169">System.Int32</span></span>

### <span data-ttu-id="9bbb8-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="9bbb8-170">System.String[]</span></span>

## <span data-ttu-id="9bbb8-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bbb8-171">OUTPUTS</span></span>

### <span data-ttu-id="9bbb8-172">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="9bbb8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="9bbb8-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bbb8-173">NOTES</span></span>

## <span data-ttu-id="9bbb8-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bbb8-174">RELATED LINKS</span></span>
