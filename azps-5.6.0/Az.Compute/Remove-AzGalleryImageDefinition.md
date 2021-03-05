---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: d632f3f9717c706adf2881aa177d9cb7ff2425dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988345"
---
# <span data-ttu-id="4fbb1-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4fbb1-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="4fbb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbb1-103">Usuwanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="4fbb1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4fbb1-104">SYNTAX</span></span>

### <span data-ttu-id="4fbb1-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4fbb1-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fbb1-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="4fbb1-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fbb1-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="4fbb1-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fbb1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4fbb1-108">DESCRIPTION</span></span>
<span data-ttu-id="4fbb1-109">Usuwanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="4fbb1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4fbb1-110">EXAMPLES</span></span>

### <span data-ttu-id="4fbb1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4fbb1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="4fbb1-112">Usuń definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="4fbb1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fbb1-113">PARAMETERS</span></span>

### <span data-ttu-id="4fbb1-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4fbb1-114">-AsJob</span></span>
<span data-ttu-id="4fbb1-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4fbb1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fbb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbb1-116">-DefaultProfile</span></span>
<span data-ttu-id="4fbb1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fbb1-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4fbb1-118">-Force</span></span>
<span data-ttu-id="4fbb1-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fbb1-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4fbb1-120">-GalleryName</span></span>
<span data-ttu-id="4fbb1-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="4fbb1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fbb1-122">-InputObject</span></span>
<span data-ttu-id="4fbb1-123">Obiekt Definicji obrazów w galerii PS</span><span class="sxs-lookup"><span data-stu-id="4fbb1-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="4fbb1-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4fbb1-124">-Name</span></span>
<span data-ttu-id="4fbb1-125">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4fbb1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbb1-126">-ResourceGroupName</span></span>
<span data-ttu-id="4fbb1-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fbb1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fbb1-128">-ResourceId</span></span>
<span data-ttu-id="4fbb1-129">Identyfikator zasobu dla definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="4fbb1-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="4fbb1-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fbb1-130">-Confirm</span></span>
<span data-ttu-id="4fbb1-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fbb1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fbb1-132">-WhatIf</span></span>
<span data-ttu-id="4fbb1-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fbb1-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fbb1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbb1-135">CommonParameters</span></span>
<span data-ttu-id="4fbb1-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fbb1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbb1-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fbb1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbb1-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fbb1-138">INPUTS</span></span>

### <span data-ttu-id="4fbb1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4fbb1-139">System.String</span></span>

### <span data-ttu-id="4fbb1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4fbb1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4fbb1-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fbb1-141">OUTPUTS</span></span>

### <span data-ttu-id="4fbb1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4fbb1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4fbb1-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4fbb1-143">NOTES</span></span>

## <span data-ttu-id="4fbb1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fbb1-144">RELATED LINKS</span></span>
