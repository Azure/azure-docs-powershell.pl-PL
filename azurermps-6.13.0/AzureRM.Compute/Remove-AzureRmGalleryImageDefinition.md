---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: e6e62fbe52aeb87868c688343ebbaed8f0046891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545479"
---
# <span data-ttu-id="9da66-101">Remove-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="9da66-101">Remove-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="9da66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9da66-102">SYNOPSIS</span></span>
<span data-ttu-id="9da66-103">Usuwanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9da66-103">Delete a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9da66-104">SYNTAX</span></span>

### <span data-ttu-id="9da66-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9da66-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da66-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9da66-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da66-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9da66-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da66-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9da66-108">DESCRIPTION</span></span>
<span data-ttu-id="9da66-109">Usuwanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9da66-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="9da66-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9da66-110">EXAMPLES</span></span>

### <span data-ttu-id="9da66-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9da66-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="9da66-112">Usuwanie definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9da66-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="9da66-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9da66-113">PARAMETERS</span></span>

### <span data-ttu-id="9da66-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9da66-114">-AsJob</span></span>
<span data-ttu-id="9da66-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9da66-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9da66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da66-116">-DefaultProfile</span></span>
<span data-ttu-id="9da66-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9da66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da66-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9da66-118">-Force</span></span>
<span data-ttu-id="9da66-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9da66-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9da66-120">-Gallery</span><span class="sxs-lookup"><span data-stu-id="9da66-120">-GalleryName</span></span>
<span data-ttu-id="9da66-121">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="9da66-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="9da66-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9da66-122">-InputObject</span></span>
<span data-ttu-id="9da66-123">Obiekt definicji obrazu z galerii PS</span><span class="sxs-lookup"><span data-stu-id="9da66-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="9da66-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9da66-124">-Name</span></span>
<span data-ttu-id="9da66-125">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="9da66-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="9da66-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da66-126">-ResourceGroupName</span></span>
<span data-ttu-id="9da66-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9da66-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9da66-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da66-128">-ResourceId</span></span>
<span data-ttu-id="9da66-129">Identyfikator zasobu definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="9da66-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="9da66-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9da66-130">-Confirm</span></span>
<span data-ttu-id="9da66-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da66-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da66-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da66-132">-WhatIf</span></span>
<span data-ttu-id="9da66-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da66-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da66-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9da66-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da66-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da66-135">CommonParameters</span></span>
<span data-ttu-id="9da66-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da66-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da66-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da66-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da66-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9da66-138">INPUTS</span></span>

### <span data-ttu-id="9da66-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9da66-139">System.String</span></span>

### <span data-ttu-id="9da66-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="9da66-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="9da66-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9da66-141">OUTPUTS</span></span>

### <span data-ttu-id="9da66-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9da66-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9da66-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9da66-143">NOTES</span></span>

## <span data-ttu-id="9da66-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9da66-144">RELATED LINKS</span></span>