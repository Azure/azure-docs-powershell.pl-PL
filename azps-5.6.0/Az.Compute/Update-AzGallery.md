---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 4badbfc9973b20869c6db421bd1299e00337d7fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990417"
---
# <span data-ttu-id="10567-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="10567-101">Update-AzGallery</span></span>

## <span data-ttu-id="10567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10567-102">SYNOPSIS</span></span>
<span data-ttu-id="10567-103">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="10567-103">Update a gallery.</span></span>

## <span data-ttu-id="10567-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10567-104">SYNTAX</span></span>

### <span data-ttu-id="10567-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10567-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10567-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="10567-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10567-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="10567-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10567-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="10567-108">DESCRIPTION</span></span>
<span data-ttu-id="10567-109">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="10567-109">Update a gallery.</span></span>

## <span data-ttu-id="10567-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10567-110">EXAMPLES</span></span>

### <span data-ttu-id="10567-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10567-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="10567-112">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="10567-112">Update a gallery.</span></span>

## <span data-ttu-id="10567-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10567-113">PARAMETERS</span></span>

### <span data-ttu-id="10567-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="10567-114">-AsJob</span></span>
<span data-ttu-id="10567-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="10567-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10567-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10567-116">-DefaultProfile</span></span>
<span data-ttu-id="10567-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10567-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10567-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="10567-118">-Description</span></span>
<span data-ttu-id="10567-119">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="10567-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="10567-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10567-120">-InputObject</span></span>
<span data-ttu-id="10567-121">Obiekt Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="10567-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="10567-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10567-122">-Name</span></span>
<span data-ttu-id="10567-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="10567-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="10567-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10567-124">-ResourceGroupName</span></span>
<span data-ttu-id="10567-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10567-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="10567-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10567-126">-ResourceId</span></span>
<span data-ttu-id="10567-127">Identyfikator zasobu dla galerii</span><span class="sxs-lookup"><span data-stu-id="10567-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="10567-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="10567-128">-Tag</span></span>
<span data-ttu-id="10567-129">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="10567-129">Resource tags</span></span>

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

### <span data-ttu-id="10567-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10567-130">-Confirm</span></span>
<span data-ttu-id="10567-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10567-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10567-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10567-132">-WhatIf</span></span>
<span data-ttu-id="10567-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10567-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10567-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10567-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10567-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10567-135">CommonParameters</span></span>
<span data-ttu-id="10567-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10567-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10567-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10567-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10567-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10567-138">INPUTS</span></span>

### <span data-ttu-id="10567-139">System.String</span><span class="sxs-lookup"><span data-stu-id="10567-139">System.String</span></span>

### <span data-ttu-id="10567-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="10567-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="10567-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="10567-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="10567-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10567-142">OUTPUTS</span></span>

### <span data-ttu-id="10567-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="10567-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="10567-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10567-144">NOTES</span></span>

## <span data-ttu-id="10567-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10567-145">RELATED LINKS</span></span>
