---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: d299fa4fc2866729ed9f933e3553c1fe7ac56b4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706125"
---
# <span data-ttu-id="b4dfb-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="b4dfb-101">Update-AzGallery</span></span>

## <span data-ttu-id="b4dfb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="b4dfb-103">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-103">Update a gallery.</span></span>

## <span data-ttu-id="b4dfb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4dfb-104">SYNTAX</span></span>

### <span data-ttu-id="b4dfb-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4dfb-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4dfb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b4dfb-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4dfb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b4dfb-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4dfb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b4dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="b4dfb-109">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-109">Update a gallery.</span></span>

## <span data-ttu-id="b4dfb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="b4dfb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4dfb-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="b4dfb-112">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-112">Update a gallery.</span></span>

## <span data-ttu-id="b4dfb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4dfb-113">PARAMETERS</span></span>

### <span data-ttu-id="b4dfb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4dfb-114">-AsJob</span></span>
<span data-ttu-id="b4dfb-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4dfb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4dfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4dfb-116">-DefaultProfile</span></span>
<span data-ttu-id="b4dfb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4dfb-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="b4dfb-118">-Description</span></span>
<span data-ttu-id="b4dfb-119">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="b4dfb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4dfb-120">-InputObject</span></span>
<span data-ttu-id="b4dfb-121">Obiekt z galerii PS.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="b4dfb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4dfb-122">-Name</span></span>
<span data-ttu-id="b4dfb-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="b4dfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4dfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4dfb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4dfb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4dfb-126">-ResourceId</span></span>
<span data-ttu-id="b4dfb-127">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="b4dfb-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="b4dfb-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4dfb-128">-Tag</span></span>
<span data-ttu-id="b4dfb-129">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="b4dfb-129">Resource tags</span></span>

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

### <span data-ttu-id="b4dfb-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4dfb-130">-Confirm</span></span>
<span data-ttu-id="b4dfb-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4dfb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4dfb-132">-WhatIf</span></span>
<span data-ttu-id="b4dfb-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4dfb-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4dfb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4dfb-135">CommonParameters</span></span>
<span data-ttu-id="b4dfb-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4dfb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4dfb-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4dfb-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4dfb-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4dfb-138">INPUTS</span></span>

### <span data-ttu-id="b4dfb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4dfb-139">System.String</span></span>

### <span data-ttu-id="b4dfb-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="b4dfb-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="b4dfb-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4dfb-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4dfb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4dfb-142">OUTPUTS</span></span>

### <span data-ttu-id="b4dfb-143">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="b4dfb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="b4dfb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4dfb-144">NOTES</span></span>

## <span data-ttu-id="b4dfb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4dfb-145">RELATED LINKS</span></span>
