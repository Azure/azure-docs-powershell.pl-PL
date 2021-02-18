---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181627"
---
# <span data-ttu-id="84afb-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="84afb-101">New-AzGallery</span></span>

## <span data-ttu-id="84afb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84afb-102">SYNOPSIS</span></span>
<span data-ttu-id="84afb-103">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="84afb-103">Create a gallery.</span></span>

## <span data-ttu-id="84afb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84afb-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84afb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="84afb-105">DESCRIPTION</span></span>
<span data-ttu-id="84afb-106">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="84afb-106">Create a gallery.</span></span>

## <span data-ttu-id="84afb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84afb-107">EXAMPLES</span></span>

### <span data-ttu-id="84afb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84afb-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="84afb-109">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="84afb-109">Create a gallery.</span></span>

## <span data-ttu-id="84afb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84afb-110">PARAMETERS</span></span>

### <span data-ttu-id="84afb-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="84afb-111">-AsJob</span></span>
<span data-ttu-id="84afb-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="84afb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84afb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84afb-113">-DefaultProfile</span></span>
<span data-ttu-id="84afb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84afb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84afb-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="84afb-115">-Description</span></span>
<span data-ttu-id="84afb-116">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="84afb-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="84afb-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="84afb-117">-Location</span></span>
<span data-ttu-id="84afb-118">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="84afb-118">Resource location</span></span>

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

### <span data-ttu-id="84afb-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="84afb-119">-Name</span></span>
<span data-ttu-id="84afb-120">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="84afb-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="84afb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84afb-121">-ResourceGroupName</span></span>
<span data-ttu-id="84afb-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84afb-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="84afb-123">— Tag</span><span class="sxs-lookup"><span data-stu-id="84afb-123">-Tag</span></span>
<span data-ttu-id="84afb-124">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="84afb-124">Resource tags</span></span>

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

### <span data-ttu-id="84afb-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84afb-125">-Confirm</span></span>
<span data-ttu-id="84afb-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84afb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84afb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84afb-127">-WhatIf</span></span>
<span data-ttu-id="84afb-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84afb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84afb-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84afb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84afb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84afb-130">CommonParameters</span></span>
<span data-ttu-id="84afb-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84afb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84afb-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84afb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84afb-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84afb-133">INPUTS</span></span>

### <span data-ttu-id="84afb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="84afb-134">System.String</span></span>

### <span data-ttu-id="84afb-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="84afb-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84afb-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84afb-136">OUTPUTS</span></span>

### <span data-ttu-id="84afb-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="84afb-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="84afb-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84afb-138">NOTES</span></span>

## <span data-ttu-id="84afb-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84afb-139">RELATED LINKS</span></span>
