---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199226"
---
# <span data-ttu-id="cd0ce-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="cd0ce-101">Remove-AzImage</span></span>

## <span data-ttu-id="cd0ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0ce-103">Usuwa obraz.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-103">Removes an image.</span></span>

## <span data-ttu-id="cd0ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd0ce-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0ce-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="cd0ce-106">Polecenie **cmdlet Remove-AzImage** usuwa obraz.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="cd0ce-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="cd0ce-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd0ce-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="cd0ce-109">To polecenie usuwa obraz o nazwie "Image01" z grupy zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cd0ce-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cd0ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd0ce-110">PARAMETERS</span></span>

### <span data-ttu-id="cd0ce-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cd0ce-111">-AsJob</span></span>
<span data-ttu-id="cd0ce-112">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cd0ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0ce-113">-DefaultProfile</span></span>
<span data-ttu-id="cd0ce-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd0ce-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cd0ce-115">-Force</span></span>
<span data-ttu-id="cd0ce-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd0ce-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cd0ce-117">-ImageName</span></span>
<span data-ttu-id="cd0ce-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0ce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd0ce-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd0ce-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd0ce-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd0ce-121">-Confirm</span></span>
<span data-ttu-id="cd0ce-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd0ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0ce-123">-WhatIf</span></span>
<span data-ttu-id="cd0ce-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd0ce-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd0ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0ce-126">CommonParameters</span></span>
<span data-ttu-id="cd0ce-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0ce-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd0ce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0ce-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd0ce-129">INPUTS</span></span>

### <span data-ttu-id="cd0ce-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cd0ce-130">System.String</span></span>

## <span data-ttu-id="cd0ce-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd0ce-131">OUTPUTS</span></span>

### <span data-ttu-id="cd0ce-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cd0ce-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cd0ce-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd0ce-133">NOTES</span></span>

## <span data-ttu-id="cd0ce-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd0ce-134">RELATED LINKS</span></span>
