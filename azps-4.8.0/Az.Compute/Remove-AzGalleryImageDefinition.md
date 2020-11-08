---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062591"
---
# <span data-ttu-id="988b8-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="988b8-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="988b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="988b8-102">SYNOPSIS</span></span>
<span data-ttu-id="988b8-103">Usuwanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="988b8-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="988b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="988b8-104">SYNTAX</span></span>

### <span data-ttu-id="988b8-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="988b8-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988b8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="988b8-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988b8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="988b8-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="988b8-108">DESCRIPTION</span></span>
<span data-ttu-id="988b8-109">Usuwanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="988b8-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="988b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="988b8-110">EXAMPLES</span></span>

### <span data-ttu-id="988b8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="988b8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="988b8-112">Usuwanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="988b8-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="988b8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="988b8-113">PARAMETERS</span></span>

### <span data-ttu-id="988b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="988b8-114">-AsJob</span></span>
<span data-ttu-id="988b8-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="988b8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="988b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988b8-116">-DefaultProfile</span></span>
<span data-ttu-id="988b8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="988b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988b8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="988b8-118">-Force</span></span>
<span data-ttu-id="988b8-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="988b8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="988b8-120">-Gallery</span><span class="sxs-lookup"><span data-stu-id="988b8-120">-GalleryName</span></span>
<span data-ttu-id="988b8-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="988b8-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="988b8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="988b8-122">-InputObject</span></span>
<span data-ttu-id="988b8-123">Obiekt definicji obrazu z galerii PS</span><span class="sxs-lookup"><span data-stu-id="988b8-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="988b8-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="988b8-124">-Name</span></span>
<span data-ttu-id="988b8-125">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="988b8-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="988b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="988b8-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="988b8-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="988b8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="988b8-128">-ResourceId</span></span>
<span data-ttu-id="988b8-129">Identyfikator zasobu definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="988b8-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="988b8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="988b8-130">-Confirm</span></span>
<span data-ttu-id="988b8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988b8-132">-WhatIf</span></span>
<span data-ttu-id="988b8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988b8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="988b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988b8-135">CommonParameters</span></span>
<span data-ttu-id="988b8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988b8-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="988b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988b8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="988b8-138">INPUTS</span></span>

### <span data-ttu-id="988b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="988b8-139">System.String</span></span>

### <span data-ttu-id="988b8-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="988b8-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="988b8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="988b8-141">OUTPUTS</span></span>

### <span data-ttu-id="988b8-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="988b8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="988b8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="988b8-143">NOTES</span></span>

## <span data-ttu-id="988b8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="988b8-144">RELATED LINKS</span></span>
