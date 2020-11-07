---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: ac098616d2ee92b4d6910034735824289b971f5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706295"
---
# <span data-ttu-id="fb483-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="fb483-101">Remove-AzGallery</span></span>

## <span data-ttu-id="fb483-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb483-102">SYNOPSIS</span></span>
<span data-ttu-id="fb483-103">Usuwanie galerii.</span><span class="sxs-lookup"><span data-stu-id="fb483-103">Delete a gallery.</span></span>

## <span data-ttu-id="fb483-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb483-104">SYNTAX</span></span>

### <span data-ttu-id="fb483-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb483-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb483-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fb483-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb483-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fb483-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb483-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fb483-108">DESCRIPTION</span></span>
<span data-ttu-id="fb483-109">Usuwanie galerii.</span><span class="sxs-lookup"><span data-stu-id="fb483-109">Delete a gallery.</span></span>

## <span data-ttu-id="fb483-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb483-110">EXAMPLES</span></span>

### <span data-ttu-id="fb483-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb483-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="fb483-112">Usuń daną galerię.</span><span class="sxs-lookup"><span data-stu-id="fb483-112">Delete the given gallery.</span></span>

## <span data-ttu-id="fb483-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb483-113">PARAMETERS</span></span>

### <span data-ttu-id="fb483-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb483-114">-AsJob</span></span>
<span data-ttu-id="fb483-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fb483-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb483-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb483-116">-DefaultProfile</span></span>
<span data-ttu-id="fb483-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb483-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb483-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fb483-118">-Force</span></span>
<span data-ttu-id="fb483-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb483-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb483-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fb483-120">-InputObject</span></span>
<span data-ttu-id="fb483-121">Obiekt galerii PS</span><span class="sxs-lookup"><span data-stu-id="fb483-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="fb483-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb483-122">-Name</span></span>
<span data-ttu-id="fb483-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="fb483-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="fb483-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb483-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb483-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb483-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb483-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb483-126">-ResourceId</span></span>
<span data-ttu-id="fb483-127">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="fb483-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="fb483-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb483-128">-Confirm</span></span>
<span data-ttu-id="fb483-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb483-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb483-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb483-130">-WhatIf</span></span>
<span data-ttu-id="fb483-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb483-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb483-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb483-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb483-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb483-133">CommonParameters</span></span>
<span data-ttu-id="fb483-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb483-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb483-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb483-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb483-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb483-136">INPUTS</span></span>

### <span data-ttu-id="fb483-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fb483-137">System.String</span></span>

### <span data-ttu-id="fb483-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="fb483-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="fb483-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb483-139">OUTPUTS</span></span>

### <span data-ttu-id="fb483-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fb483-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fb483-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb483-141">NOTES</span></span>

## <span data-ttu-id="fb483-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb483-142">RELATED LINKS</span></span>
