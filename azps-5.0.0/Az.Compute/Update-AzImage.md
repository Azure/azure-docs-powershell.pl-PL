---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304164"
---
# <span data-ttu-id="b85df-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b85df-101">Update-AzImage</span></span>

## <span data-ttu-id="b85df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b85df-102">SYNOPSIS</span></span>
<span data-ttu-id="b85df-103">Umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="b85df-103">Updates an image.</span></span>

## <span data-ttu-id="b85df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b85df-104">SYNTAX</span></span>

### <span data-ttu-id="b85df-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b85df-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85df-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b85df-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85df-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b85df-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b85df-108">DESCRIPTION</span></span>
<span data-ttu-id="b85df-109">Polecenie cmdlet **Update-AzImage** umożliwia zaktualizowanie obrazu.</span><span class="sxs-lookup"><span data-stu-id="b85df-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="b85df-110">Obecnie można aktualizować tylko te Tagi.</span><span class="sxs-lookup"><span data-stu-id="b85df-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="b85df-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b85df-111">EXAMPLES</span></span>

### <span data-ttu-id="b85df-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b85df-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="b85df-113">To polecenie aktualizuje wartość znacznika istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b85df-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b85df-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b85df-114">PARAMETERS</span></span>

### <span data-ttu-id="b85df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b85df-115">-AsJob</span></span>
<span data-ttu-id="b85df-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="b85df-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b85df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85df-117">-DefaultProfile</span></span>
<span data-ttu-id="b85df-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b85df-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85df-119">-Image</span><span class="sxs-lookup"><span data-stu-id="b85df-119">-Image</span></span>
<span data-ttu-id="b85df-120">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="b85df-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b85df-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b85df-121">-ImageName</span></span>
<span data-ttu-id="b85df-122">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="b85df-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85df-123">-ResourceGroupName</span></span>
<span data-ttu-id="b85df-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b85df-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b85df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b85df-125">-ResourceId</span></span>
<span data-ttu-id="b85df-126">Identyfikator zasobu obrazu</span><span class="sxs-lookup"><span data-stu-id="b85df-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="b85df-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b85df-127">-Tag</span></span>
<span data-ttu-id="b85df-128">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="b85df-128">Resource tags</span></span>

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

### <span data-ttu-id="b85df-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b85df-129">-Confirm</span></span>
<span data-ttu-id="b85df-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85df-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85df-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85df-131">-WhatIf</span></span>
<span data-ttu-id="b85df-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85df-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85df-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b85df-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85df-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85df-134">CommonParameters</span></span>
<span data-ttu-id="b85df-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85df-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85df-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b85df-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85df-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b85df-137">INPUTS</span></span>

### <span data-ttu-id="b85df-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b85df-138">System.String</span></span>

### <span data-ttu-id="b85df-139">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="b85df-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b85df-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b85df-140">OUTPUTS</span></span>

### <span data-ttu-id="b85df-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="b85df-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b85df-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b85df-142">NOTES</span></span>

## <span data-ttu-id="b85df-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b85df-143">RELATED LINKS</span></span>
