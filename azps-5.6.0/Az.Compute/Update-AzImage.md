---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: edf0ce1b67c25b8f5e48282dba45e845820c7b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971409"
---
# <span data-ttu-id="99c47-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="99c47-101">Update-AzImage</span></span>

## <span data-ttu-id="99c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c47-102">SYNOPSIS</span></span>
<span data-ttu-id="99c47-103">Aktualizuje obraz.</span><span class="sxs-lookup"><span data-stu-id="99c47-103">Updates an image.</span></span>

## <span data-ttu-id="99c47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99c47-104">SYNTAX</span></span>

### <span data-ttu-id="99c47-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99c47-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c47-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="99c47-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c47-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="99c47-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c47-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="99c47-108">DESCRIPTION</span></span>
<span data-ttu-id="99c47-109">Polecenie **cmdlet Update-AzImage** aktualizuje obraz.</span><span class="sxs-lookup"><span data-stu-id="99c47-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="99c47-110">Obecnie można aktualizować tylko znaczniki.</span><span class="sxs-lookup"><span data-stu-id="99c47-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="99c47-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99c47-111">EXAMPLES</span></span>

### <span data-ttu-id="99c47-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99c47-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="99c47-113">To polecenie aktualizuje wartość tagu istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="99c47-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="99c47-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99c47-114">PARAMETERS</span></span>

### <span data-ttu-id="99c47-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="99c47-115">-AsJob</span></span>
<span data-ttu-id="99c47-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="99c47-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="99c47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c47-117">-DefaultProfile</span></span>
<span data-ttu-id="99c47-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99c47-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c47-119">— Obraz</span><span class="sxs-lookup"><span data-stu-id="99c47-119">-Image</span></span>
<span data-ttu-id="99c47-120">Określa obiekt obrazu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="99c47-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99c47-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="99c47-121">-ImageName</span></span>
<span data-ttu-id="99c47-122">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="99c47-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99c47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c47-123">-ResourceGroupName</span></span>
<span data-ttu-id="99c47-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99c47-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="99c47-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99c47-125">-ResourceId</span></span>
<span data-ttu-id="99c47-126">Identyfikator zasobu dla obrazu</span><span class="sxs-lookup"><span data-stu-id="99c47-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="99c47-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="99c47-127">-Tag</span></span>
<span data-ttu-id="99c47-128">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="99c47-128">Resource tags</span></span>

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

### <span data-ttu-id="99c47-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99c47-129">-Confirm</span></span>
<span data-ttu-id="99c47-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99c47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c47-131">-WhatIf</span></span>
<span data-ttu-id="99c47-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99c47-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c47-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99c47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c47-134">CommonParameters</span></span>
<span data-ttu-id="99c47-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c47-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99c47-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c47-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99c47-137">INPUTS</span></span>

### <span data-ttu-id="99c47-138">System.String</span><span class="sxs-lookup"><span data-stu-id="99c47-138">System.String</span></span>

### <span data-ttu-id="99c47-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="99c47-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="99c47-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99c47-140">OUTPUTS</span></span>

### <span data-ttu-id="99c47-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="99c47-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="99c47-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99c47-142">NOTES</span></span>

## <span data-ttu-id="99c47-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99c47-143">RELATED LINKS</span></span>
