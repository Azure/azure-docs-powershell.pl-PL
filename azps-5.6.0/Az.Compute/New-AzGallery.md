---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 47ba904378ed8f58da29876d5835ca43bb8a7a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959690"
---
# <span data-ttu-id="a5adf-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="a5adf-101">New-AzGallery</span></span>

## <span data-ttu-id="a5adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5adf-102">SYNOPSIS</span></span>
<span data-ttu-id="a5adf-103">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="a5adf-103">Create a gallery.</span></span>

## <span data-ttu-id="a5adf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5adf-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5adf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5adf-105">DESCRIPTION</span></span>
<span data-ttu-id="a5adf-106">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="a5adf-106">Create a gallery.</span></span>

## <span data-ttu-id="a5adf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5adf-107">EXAMPLES</span></span>

### <span data-ttu-id="a5adf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5adf-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="a5adf-109">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="a5adf-109">Create a gallery.</span></span>

## <span data-ttu-id="a5adf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5adf-110">PARAMETERS</span></span>

### <span data-ttu-id="a5adf-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a5adf-111">-AsJob</span></span>
<span data-ttu-id="a5adf-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a5adf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5adf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5adf-113">-DefaultProfile</span></span>
<span data-ttu-id="a5adf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5adf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5adf-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="a5adf-115">-Description</span></span>
<span data-ttu-id="a5adf-116">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="a5adf-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="a5adf-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a5adf-117">-Location</span></span>
<span data-ttu-id="a5adf-118">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="a5adf-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5adf-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a5adf-119">-Name</span></span>
<span data-ttu-id="a5adf-120">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="a5adf-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5adf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5adf-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5adf-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5adf-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5adf-123">— Tag</span><span class="sxs-lookup"><span data-stu-id="a5adf-123">-Tag</span></span>
<span data-ttu-id="a5adf-124">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="a5adf-124">Resource tags</span></span>

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

### <span data-ttu-id="a5adf-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5adf-125">-Confirm</span></span>
<span data-ttu-id="a5adf-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a5adf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5adf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5adf-127">-WhatIf</span></span>
<span data-ttu-id="a5adf-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5adf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5adf-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a5adf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5adf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5adf-130">CommonParameters</span></span>
<span data-ttu-id="a5adf-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5adf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5adf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5adf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5adf-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5adf-133">INPUTS</span></span>

### <span data-ttu-id="a5adf-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a5adf-134">System.String</span></span>

### <span data-ttu-id="a5adf-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5adf-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a5adf-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5adf-136">OUTPUTS</span></span>

### <span data-ttu-id="a5adf-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="a5adf-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="a5adf-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5adf-138">NOTES</span></span>

## <span data-ttu-id="a5adf-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5adf-139">RELATED LINKS</span></span>
