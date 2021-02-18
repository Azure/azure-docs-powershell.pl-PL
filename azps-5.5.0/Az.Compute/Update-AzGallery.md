---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181538"
---
# <span data-ttu-id="8be53-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="8be53-101">Update-AzGallery</span></span>

## <span data-ttu-id="8be53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be53-102">SYNOPSIS</span></span>
<span data-ttu-id="8be53-103">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="8be53-103">Update a gallery.</span></span>

## <span data-ttu-id="8be53-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8be53-104">SYNTAX</span></span>

### <span data-ttu-id="8be53-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8be53-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be53-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="8be53-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be53-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="8be53-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be53-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8be53-108">DESCRIPTION</span></span>
<span data-ttu-id="8be53-109">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="8be53-109">Update a gallery.</span></span>

## <span data-ttu-id="8be53-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8be53-110">EXAMPLES</span></span>

### <span data-ttu-id="8be53-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8be53-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="8be53-112">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="8be53-112">Update a gallery.</span></span>

## <span data-ttu-id="8be53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8be53-113">PARAMETERS</span></span>

### <span data-ttu-id="8be53-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8be53-114">-AsJob</span></span>
<span data-ttu-id="8be53-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8be53-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8be53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be53-116">-DefaultProfile</span></span>
<span data-ttu-id="8be53-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8be53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be53-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="8be53-118">-Description</span></span>
<span data-ttu-id="8be53-119">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="8be53-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="8be53-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be53-120">-InputObject</span></span>
<span data-ttu-id="8be53-121">Obiekt Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="8be53-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="8be53-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8be53-122">-Name</span></span>
<span data-ttu-id="8be53-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="8be53-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="8be53-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be53-124">-ResourceGroupName</span></span>
<span data-ttu-id="8be53-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8be53-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8be53-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8be53-126">-ResourceId</span></span>
<span data-ttu-id="8be53-127">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="8be53-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="8be53-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="8be53-128">-Tag</span></span>
<span data-ttu-id="8be53-129">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="8be53-129">Resource tags</span></span>

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

### <span data-ttu-id="8be53-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8be53-130">-Confirm</span></span>
<span data-ttu-id="8be53-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8be53-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be53-132">-WhatIf</span></span>
<span data-ttu-id="8be53-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be53-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8be53-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be53-135">CommonParameters</span></span>
<span data-ttu-id="8be53-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be53-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8be53-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be53-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8be53-138">INPUTS</span></span>

### <span data-ttu-id="8be53-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8be53-139">System.String</span></span>

### <span data-ttu-id="8be53-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="8be53-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="8be53-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8be53-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8be53-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8be53-142">OUTPUTS</span></span>

### <span data-ttu-id="8be53-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="8be53-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="8be53-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8be53-144">NOTES</span></span>

## <span data-ttu-id="8be53-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8be53-145">RELATED LINKS</span></span>
