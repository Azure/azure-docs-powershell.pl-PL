---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 1f6773aafbb717387d2d1a984db03e4d2739194f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710171"
---
# <span data-ttu-id="e57b9-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="e57b9-101">Update-AzGallery</span></span>

## <span data-ttu-id="e57b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e57b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e57b9-103">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="e57b9-103">Update a gallery.</span></span>

## <span data-ttu-id="e57b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e57b9-104">SYNTAX</span></span>

### <span data-ttu-id="e57b9-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e57b9-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e57b9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e57b9-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e57b9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e57b9-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e57b9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e57b9-108">DESCRIPTION</span></span>
<span data-ttu-id="e57b9-109">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="e57b9-109">Update a gallery.</span></span>

## <span data-ttu-id="e57b9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e57b9-110">EXAMPLES</span></span>

### <span data-ttu-id="e57b9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e57b9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="e57b9-112">Aktualizowanie galerii.</span><span class="sxs-lookup"><span data-stu-id="e57b9-112">Update a gallery.</span></span>

## <span data-ttu-id="e57b9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e57b9-113">PARAMETERS</span></span>

### <span data-ttu-id="e57b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e57b9-114">-AsJob</span></span>
<span data-ttu-id="e57b9-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e57b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e57b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57b9-116">-DefaultProfile</span></span>
<span data-ttu-id="e57b9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e57b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e57b9-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="e57b9-118">-Description</span></span>
<span data-ttu-id="e57b9-119">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="e57b9-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="e57b9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e57b9-120">-InputObject</span></span>
<span data-ttu-id="e57b9-121">Obiekt z galerii PS.</span><span class="sxs-lookup"><span data-stu-id="e57b9-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="e57b9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e57b9-122">-Name</span></span>
<span data-ttu-id="e57b9-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="e57b9-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="e57b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="e57b9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e57b9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e57b9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e57b9-126">-ResourceId</span></span>
<span data-ttu-id="e57b9-127">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="e57b9-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="e57b9-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="e57b9-128">-Tag</span></span>
<span data-ttu-id="e57b9-129">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="e57b9-129">Resource tags</span></span>

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

### <span data-ttu-id="e57b9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e57b9-130">-Confirm</span></span>
<span data-ttu-id="e57b9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e57b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e57b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57b9-132">-WhatIf</span></span>
<span data-ttu-id="e57b9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e57b9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e57b9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e57b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e57b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57b9-135">CommonParameters</span></span>
<span data-ttu-id="e57b9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57b9-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57b9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57b9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e57b9-138">INPUTS</span></span>

### <span data-ttu-id="e57b9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e57b9-139">System.String</span></span>

### <span data-ttu-id="e57b9-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="e57b9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="e57b9-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e57b9-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e57b9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e57b9-142">OUTPUTS</span></span>

### <span data-ttu-id="e57b9-143">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="e57b9-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="e57b9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e57b9-144">NOTES</span></span>

## <span data-ttu-id="e57b9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e57b9-145">RELATED LINKS</span></span>
