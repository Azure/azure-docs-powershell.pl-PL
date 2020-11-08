---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049317"
---
# <span data-ttu-id="cc770-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="cc770-101">Remove-AzImage</span></span>

## <span data-ttu-id="cc770-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc770-102">SYNOPSIS</span></span>
<span data-ttu-id="cc770-103">Usuwa obraz.</span><span class="sxs-lookup"><span data-stu-id="cc770-103">Removes an image.</span></span>

## <span data-ttu-id="cc770-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc770-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc770-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc770-105">DESCRIPTION</span></span>
<span data-ttu-id="cc770-106">Polecenie cmdlet **Remove-AzImage** usuwa obraz..</span><span class="sxs-lookup"><span data-stu-id="cc770-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="cc770-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc770-107">EXAMPLES</span></span>

### <span data-ttu-id="cc770-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc770-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="cc770-109">To polecenie usuwa obraz o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cc770-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cc770-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc770-110">PARAMETERS</span></span>

### <span data-ttu-id="cc770-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc770-111">-AsJob</span></span>
<span data-ttu-id="cc770-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="cc770-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cc770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc770-113">-DefaultProfile</span></span>
<span data-ttu-id="cc770-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc770-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc770-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc770-115">-Force</span></span>
<span data-ttu-id="cc770-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc770-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc770-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cc770-117">-ImageName</span></span>
<span data-ttu-id="cc770-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="cc770-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="cc770-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc770-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc770-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc770-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cc770-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc770-121">-Confirm</span></span>
<span data-ttu-id="cc770-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc770-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc770-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc770-123">-WhatIf</span></span>
<span data-ttu-id="cc770-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc770-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc770-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc770-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc770-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc770-126">CommonParameters</span></span>
<span data-ttu-id="cc770-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc770-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc770-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc770-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc770-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc770-129">INPUTS</span></span>

### <span data-ttu-id="cc770-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cc770-130">System.String</span></span>

## <span data-ttu-id="cc770-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc770-131">OUTPUTS</span></span>

### <span data-ttu-id="cc770-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cc770-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cc770-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc770-133">NOTES</span></span>

## <span data-ttu-id="cc770-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc770-134">RELATED LINKS</span></span>
