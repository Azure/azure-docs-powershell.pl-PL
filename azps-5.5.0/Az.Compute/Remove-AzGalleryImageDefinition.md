---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195011"
---
# <span data-ttu-id="6cdae-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6cdae-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="6cdae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cdae-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdae-103">Usuwanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="6cdae-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="6cdae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6cdae-104">SYNTAX</span></span>

### <span data-ttu-id="6cdae-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6cdae-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cdae-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="6cdae-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cdae-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="6cdae-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cdae-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6cdae-108">DESCRIPTION</span></span>
<span data-ttu-id="6cdae-109">Usuwanie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="6cdae-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="6cdae-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6cdae-110">EXAMPLES</span></span>

### <span data-ttu-id="6cdae-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6cdae-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="6cdae-112">Usuń definicję obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="6cdae-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="6cdae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cdae-113">PARAMETERS</span></span>

### <span data-ttu-id="6cdae-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6cdae-114">-AsJob</span></span>
<span data-ttu-id="6cdae-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6cdae-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cdae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdae-116">-DefaultProfile</span></span>
<span data-ttu-id="6cdae-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cdae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cdae-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6cdae-118">-Force</span></span>
<span data-ttu-id="6cdae-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6cdae-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cdae-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6cdae-120">-GalleryName</span></span>
<span data-ttu-id="6cdae-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="6cdae-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="6cdae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cdae-122">-InputObject</span></span>
<span data-ttu-id="6cdae-123">Obiekt Definicji obrazów w galerii PS</span><span class="sxs-lookup"><span data-stu-id="6cdae-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="6cdae-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6cdae-124">-Name</span></span>
<span data-ttu-id="6cdae-125">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="6cdae-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6cdae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdae-126">-ResourceGroupName</span></span>
<span data-ttu-id="6cdae-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6cdae-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cdae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cdae-128">-ResourceId</span></span>
<span data-ttu-id="6cdae-129">Identyfikator zasobu dla definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="6cdae-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="6cdae-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cdae-130">-Confirm</span></span>
<span data-ttu-id="6cdae-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6cdae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cdae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cdae-132">-WhatIf</span></span>
<span data-ttu-id="6cdae-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cdae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cdae-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6cdae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cdae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdae-135">CommonParameters</span></span>
<span data-ttu-id="6cdae-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cdae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdae-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cdae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdae-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cdae-138">INPUTS</span></span>

### <span data-ttu-id="6cdae-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6cdae-139">System.String</span></span>

### <span data-ttu-id="6cdae-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="6cdae-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="6cdae-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cdae-141">OUTPUTS</span></span>

### <span data-ttu-id="6cdae-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6cdae-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6cdae-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6cdae-143">NOTES</span></span>

## <span data-ttu-id="6cdae-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cdae-144">RELATED LINKS</span></span>
