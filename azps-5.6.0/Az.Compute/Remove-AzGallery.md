---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: abc9fd93545f229c39dd696a856781ceed748a77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988359"
---
# <span data-ttu-id="26a65-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="26a65-101">Remove-AzGallery</span></span>

## <span data-ttu-id="26a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a65-102">SYNOPSIS</span></span>
<span data-ttu-id="26a65-103">Usuwanie galerii.</span><span class="sxs-lookup"><span data-stu-id="26a65-103">Delete a gallery.</span></span>

## <span data-ttu-id="26a65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26a65-104">SYNTAX</span></span>

### <span data-ttu-id="26a65-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26a65-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a65-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="26a65-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a65-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="26a65-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a65-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="26a65-108">DESCRIPTION</span></span>
<span data-ttu-id="26a65-109">Usuwanie galerii.</span><span class="sxs-lookup"><span data-stu-id="26a65-109">Delete a gallery.</span></span>

## <span data-ttu-id="26a65-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26a65-110">EXAMPLES</span></span>

### <span data-ttu-id="26a65-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26a65-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="26a65-112">Usuwanie danej galerii.</span><span class="sxs-lookup"><span data-stu-id="26a65-112">Delete the given gallery.</span></span>

## <span data-ttu-id="26a65-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26a65-113">PARAMETERS</span></span>

### <span data-ttu-id="26a65-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="26a65-114">-AsJob</span></span>
<span data-ttu-id="26a65-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="26a65-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26a65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a65-116">-DefaultProfile</span></span>
<span data-ttu-id="26a65-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26a65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26a65-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="26a65-118">-Force</span></span>
<span data-ttu-id="26a65-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="26a65-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26a65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26a65-120">-InputObject</span></span>
<span data-ttu-id="26a65-121">Obiekt Galeria PS</span><span class="sxs-lookup"><span data-stu-id="26a65-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26a65-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26a65-122">-Name</span></span>
<span data-ttu-id="26a65-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="26a65-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26a65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a65-124">-ResourceGroupName</span></span>
<span data-ttu-id="26a65-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26a65-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="26a65-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26a65-126">-ResourceId</span></span>
<span data-ttu-id="26a65-127">Identyfikator zasobu dla galerii</span><span class="sxs-lookup"><span data-stu-id="26a65-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="26a65-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26a65-128">-Confirm</span></span>
<span data-ttu-id="26a65-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26a65-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a65-130">-WhatIf</span></span>
<span data-ttu-id="26a65-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a65-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26a65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a65-133">CommonParameters</span></span>
<span data-ttu-id="26a65-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a65-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26a65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a65-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a65-136">INPUTS</span></span>

### <span data-ttu-id="26a65-137">System.String</span><span class="sxs-lookup"><span data-stu-id="26a65-137">System.String</span></span>

### <span data-ttu-id="26a65-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="26a65-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="26a65-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a65-139">OUTPUTS</span></span>

### <span data-ttu-id="26a65-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="26a65-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="26a65-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26a65-141">NOTES</span></span>

## <span data-ttu-id="26a65-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26a65-142">RELATED LINKS</span></span>
