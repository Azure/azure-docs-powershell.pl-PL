---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064266"
---
# <span data-ttu-id="57f51-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="57f51-101">Remove-AzGallery</span></span>

## <span data-ttu-id="57f51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57f51-102">SYNOPSIS</span></span>
<span data-ttu-id="57f51-103">Usuwanie galerii.</span><span class="sxs-lookup"><span data-stu-id="57f51-103">Delete a gallery.</span></span>

## <span data-ttu-id="57f51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57f51-104">SYNTAX</span></span>

### <span data-ttu-id="57f51-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="57f51-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f51-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="57f51-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f51-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="57f51-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f51-108">Opis</span><span class="sxs-lookup"><span data-stu-id="57f51-108">DESCRIPTION</span></span>
<span data-ttu-id="57f51-109">Usuwanie galerii.</span><span class="sxs-lookup"><span data-stu-id="57f51-109">Delete a gallery.</span></span>

## <span data-ttu-id="57f51-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57f51-110">EXAMPLES</span></span>

### <span data-ttu-id="57f51-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57f51-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="57f51-112">Usuń daną galerię.</span><span class="sxs-lookup"><span data-stu-id="57f51-112">Delete the given gallery.</span></span>

## <span data-ttu-id="57f51-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57f51-113">PARAMETERS</span></span>

### <span data-ttu-id="57f51-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57f51-114">-AsJob</span></span>
<span data-ttu-id="57f51-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57f51-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57f51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f51-116">-DefaultProfile</span></span>
<span data-ttu-id="57f51-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57f51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f51-118">-Force</span><span class="sxs-lookup"><span data-stu-id="57f51-118">-Force</span></span>
<span data-ttu-id="57f51-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="57f51-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57f51-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57f51-120">-InputObject</span></span>
<span data-ttu-id="57f51-121">Obiekt galerii PS</span><span class="sxs-lookup"><span data-stu-id="57f51-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="57f51-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57f51-122">-Name</span></span>
<span data-ttu-id="57f51-123">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="57f51-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="57f51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f51-124">-ResourceGroupName</span></span>
<span data-ttu-id="57f51-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57f51-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="57f51-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57f51-126">-ResourceId</span></span>
<span data-ttu-id="57f51-127">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="57f51-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="57f51-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57f51-128">-Confirm</span></span>
<span data-ttu-id="57f51-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f51-130">-WhatIf</span></span>
<span data-ttu-id="57f51-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f51-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57f51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f51-133">CommonParameters</span></span>
<span data-ttu-id="57f51-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f51-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57f51-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f51-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57f51-136">INPUTS</span></span>

### <span data-ttu-id="57f51-137">System. String</span><span class="sxs-lookup"><span data-stu-id="57f51-137">System.String</span></span>

### <span data-ttu-id="57f51-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="57f51-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="57f51-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57f51-139">OUTPUTS</span></span>

### <span data-ttu-id="57f51-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="57f51-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="57f51-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57f51-141">NOTES</span></span>

## <span data-ttu-id="57f51-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57f51-142">RELATED LINKS</span></span>
