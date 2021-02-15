---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177619"
---
# <span data-ttu-id="d2c8c-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d2c8c-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="d2c8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c8c-103">Usuwanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="d2c8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2c8c-104">SYNTAX</span></span>

### <span data-ttu-id="d2c8c-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d2c8c-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2c8c-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="d2c8c-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2c8c-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="d2c8c-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c8c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2c8c-108">DESCRIPTION</span></span>
<span data-ttu-id="d2c8c-109">Usuwanie wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="d2c8c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2c8c-110">EXAMPLES</span></span>

### <span data-ttu-id="d2c8c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2c8c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="d2c8c-112">Usuń wersję obrazu z danej galerii.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="d2c8c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c8c-113">PARAMETERS</span></span>

### <span data-ttu-id="d2c8c-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2c8c-114">-AsJob</span></span>
<span data-ttu-id="d2c8c-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2c8c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2c8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c8c-116">-DefaultProfile</span></span>
<span data-ttu-id="d2c8c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c8c-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d2c8c-118">-Force</span></span>
<span data-ttu-id="d2c8c-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2c8c-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d2c8c-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="d2c8c-121">Nazwa definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8c-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="d2c8c-122">-GalleryName</span></span>
<span data-ttu-id="d2c8c-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="d2c8c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2c8c-124">-InputObject</span></span>
<span data-ttu-id="d2c8c-125">Obiekt Wersja w galerii PS</span><span class="sxs-lookup"><span data-stu-id="d2c8c-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8c-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2c8c-126">-Name</span></span>
<span data-ttu-id="d2c8c-127">Nazwa wersji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c8c-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2c8c-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="d2c8c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2c8c-130">-ResourceId</span></span>
<span data-ttu-id="d2c8c-131">Identyfikator zasobu dla wersji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="d2c8c-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="d2c8c-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2c8c-132">-Confirm</span></span>
<span data-ttu-id="d2c8c-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c8c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c8c-134">-WhatIf</span></span>
<span data-ttu-id="d2c8c-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c8c-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c8c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c8c-137">CommonParameters</span></span>
<span data-ttu-id="d2c8c-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c8c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2c8c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c8c-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2c8c-140">INPUTS</span></span>

### <span data-ttu-id="d2c8c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d2c8c-141">System.String</span></span>

### <span data-ttu-id="d2c8c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d2c8c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d2c8c-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2c8c-143">OUTPUTS</span></span>

### <span data-ttu-id="d2c8c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d2c8c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d2c8c-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2c8c-145">NOTES</span></span>

## <span data-ttu-id="d2c8c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2c8c-146">RELATED LINKS</span></span>
