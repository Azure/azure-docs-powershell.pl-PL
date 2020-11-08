---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224574"
---
# <span data-ttu-id="85295-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="85295-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="85295-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85295-102">SYNOPSIS</span></span>
<span data-ttu-id="85295-103">Usuwanie wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="85295-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="85295-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85295-104">SYNTAX</span></span>

### <span data-ttu-id="85295-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85295-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85295-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="85295-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85295-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="85295-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85295-108">Opis</span><span class="sxs-lookup"><span data-stu-id="85295-108">DESCRIPTION</span></span>
<span data-ttu-id="85295-109">Usuwanie wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="85295-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="85295-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85295-110">EXAMPLES</span></span>

### <span data-ttu-id="85295-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85295-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="85295-112">Usunięcie podanej wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="85295-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="85295-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85295-113">PARAMETERS</span></span>

### <span data-ttu-id="85295-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85295-114">-AsJob</span></span>
<span data-ttu-id="85295-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="85295-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85295-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85295-116">-DefaultProfile</span></span>
<span data-ttu-id="85295-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85295-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85295-118">-Force</span><span class="sxs-lookup"><span data-stu-id="85295-118">-Force</span></span>
<span data-ttu-id="85295-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="85295-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85295-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="85295-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="85295-121">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="85295-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="85295-122">-Gallery</span><span class="sxs-lookup"><span data-stu-id="85295-122">-GalleryName</span></span>
<span data-ttu-id="85295-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="85295-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="85295-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85295-124">-InputObject</span></span>
<span data-ttu-id="85295-125">Obiekt wersja obrazu galerii PS</span><span class="sxs-lookup"><span data-stu-id="85295-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="85295-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85295-126">-Name</span></span>
<span data-ttu-id="85295-127">Nazwa wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="85295-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="85295-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85295-128">-ResourceGroupName</span></span>
<span data-ttu-id="85295-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85295-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="85295-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85295-130">-ResourceId</span></span>
<span data-ttu-id="85295-131">Wersja obrazu galerii identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="85295-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="85295-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85295-132">-Confirm</span></span>
<span data-ttu-id="85295-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85295-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85295-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85295-134">-WhatIf</span></span>
<span data-ttu-id="85295-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85295-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85295-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85295-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85295-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85295-137">CommonParameters</span></span>
<span data-ttu-id="85295-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85295-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85295-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85295-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85295-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85295-140">INPUTS</span></span>

### <span data-ttu-id="85295-141">System. String</span><span class="sxs-lookup"><span data-stu-id="85295-141">System.String</span></span>

### <span data-ttu-id="85295-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="85295-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="85295-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85295-143">OUTPUTS</span></span>

### <span data-ttu-id="85295-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="85295-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="85295-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85295-145">NOTES</span></span>

## <span data-ttu-id="85295-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85295-146">RELATED LINKS</span></span>
