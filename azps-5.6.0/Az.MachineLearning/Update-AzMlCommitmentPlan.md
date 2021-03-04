---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 6bd60ced20e9c5b8ce9c3be01d419af55281aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956122"
---
# <span data-ttu-id="cff2f-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="cff2f-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="cff2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff2f-102">SYNOPSIS</span></span>
<span data-ttu-id="cff2f-103">Aktualizuje właściwości istniejącego zasobu planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="cff2f-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="cff2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cff2f-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cff2f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cff2f-105">DESCRIPTION</span></span>
<span data-ttu-id="cff2f-106">Aktualizuje istniejący zasób planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="cff2f-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="cff2f-107">Zwróć uwagę, że większość właściwości planu zobowiązania jest niezmienialna i nie można ich modyfikować.</span><span class="sxs-lookup"><span data-stu-id="cff2f-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="cff2f-108">Właściwości, które można modyfikować, to między innymi SKU (umożliwiająca migrowanie planu zobowiązania z jednej wersji SKU do drugiej) i Tagi.</span><span class="sxs-lookup"><span data-stu-id="cff2f-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="cff2f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cff2f-109">EXAMPLES</span></span>

### <span data-ttu-id="cff2f-110">Przykład 1. Aktualizowanie planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="cff2f-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="cff2f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cff2f-111">PARAMETERS</span></span>

### <span data-ttu-id="cff2f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff2f-112">-DefaultProfile</span></span>
<span data-ttu-id="cff2f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cff2f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cff2f-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cff2f-114">-Force</span></span>
<span data-ttu-id="cff2f-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cff2f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cff2f-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cff2f-116">-Name</span></span>
<span data-ttu-id="cff2f-117">Nazwa planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cff2f-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff2f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff2f-118">-ResourceGroupName</span></span>
<span data-ttu-id="cff2f-119">Nazwa grupy zasobów dla planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cff2f-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff2f-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="cff2f-120">-SkuCapacity</span></span>
<span data-ttu-id="cff2f-121">Wydajność wersji SKU do użycia podczas aktualizowania planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cff2f-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff2f-122">-SKUName</span><span class="sxs-lookup"><span data-stu-id="cff2f-122">-SkuName</span></span>
<span data-ttu-id="cff2f-123">Nazwa sku, która ma być używania podczas aktualizowania planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cff2f-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff2f-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cff2f-124">-SkuTier</span></span>
<span data-ttu-id="cff2f-125">Warstwa sku, która ma być używania podczas aktualizowania planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="cff2f-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff2f-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="cff2f-126">-Tag</span></span>
<span data-ttu-id="cff2f-127">Tagi dla zasobu planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="cff2f-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff2f-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cff2f-128">-Confirm</span></span>
<span data-ttu-id="cff2f-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cff2f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cff2f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff2f-130">-WhatIf</span></span>
<span data-ttu-id="cff2f-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cff2f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cff2f-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cff2f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cff2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff2f-133">CommonParameters</span></span>
<span data-ttu-id="cff2f-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff2f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff2f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff2f-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cff2f-136">INPUTS</span></span>

### <span data-ttu-id="cff2f-137">Brak</span><span class="sxs-lookup"><span data-stu-id="cff2f-137">None</span></span>

## <span data-ttu-id="cff2f-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cff2f-138">OUTPUTS</span></span>

### <span data-ttu-id="cff2f-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="cff2f-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="cff2f-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cff2f-140">NOTES</span></span>
<span data-ttu-id="cff2f-141">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="cff2f-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="cff2f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cff2f-142">RELATED LINKS</span></span>
