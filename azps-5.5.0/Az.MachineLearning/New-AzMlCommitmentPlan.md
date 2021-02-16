---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241339"
---
# <span data-ttu-id="bc154-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="bc154-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="bc154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc154-102">SYNOPSIS</span></span>
<span data-ttu-id="bc154-103">Tworzy nowy plan zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="bc154-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="bc154-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc154-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc154-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc154-105">DESCRIPTION</span></span>
<span data-ttu-id="bc154-106">Tworzy plan zobowiązania usługi Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc154-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="bc154-107">Jeśli w grupie zasobów istnieje plan zobowiązania o takiej samej nazwie, połączenie działa jako operacja aktualizacji, a istniejący plan zobowiązania zostanie zastąpiony.</span><span class="sxs-lookup"><span data-stu-id="bc154-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="bc154-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc154-108">EXAMPLES</span></span>

### <span data-ttu-id="bc154-109">Przykład 1. Tworzenie nowego planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="bc154-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="bc154-110">Tworzy nowy plan zobowiązania usługi Azure Machine Learning o nazwie "MyCommitmentPlanName" w grupie "MyResourceGroup" i w południowo-środkowym regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="bc154-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="bc154-111">W tym przykładzie używany jest test/standard SKU DevTest, co oznacza, że zasoby udostępniane w planie zobowiązania zostaną określone przez limity testu/standardu dev.</span><span class="sxs-lookup"><span data-stu-id="bc154-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="bc154-112">W tym przykładzie SKUCapacity ma 1, co oznacza, że koszt planu będzie 1x kosztem Testu Deweloperów, a zasoby w planie będą 1x tym, co zapewnia test dev.</span><span class="sxs-lookup"><span data-stu-id="bc154-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="bc154-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc154-113">PARAMETERS</span></span>

### <span data-ttu-id="bc154-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc154-114">-DefaultProfile</span></span>
<span data-ttu-id="bc154-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bc154-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc154-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bc154-116">-Force</span></span>
<span data-ttu-id="bc154-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc154-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bc154-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bc154-118">-Location</span></span>
<span data-ttu-id="bc154-119">Lokalizacja planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bc154-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bc154-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc154-120">-Name</span></span>
<span data-ttu-id="bc154-121">Nazwa planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bc154-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bc154-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc154-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc154-123">Nazwa grupy zasobów dla planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bc154-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bc154-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bc154-124">-SkuCapacity</span></span>
<span data-ttu-id="bc154-125">Pojemność wersji SKU do użycia podczas inicjowania obsługi administracyjnej planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bc154-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bc154-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="bc154-126">-SkuName</span></span>
<span data-ttu-id="bc154-127">Nazwa sku, która ma być używania podczas inicjowania obsługi administracyjnej planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bc154-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bc154-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bc154-128">-SkuTier</span></span>
<span data-ttu-id="bc154-129">Warstwa sKU do użycia podczas inicjowania obsługi administracyjnej planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bc154-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bc154-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc154-130">-Confirm</span></span>
<span data-ttu-id="bc154-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc154-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc154-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc154-132">-WhatIf</span></span>
<span data-ttu-id="bc154-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc154-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc154-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bc154-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc154-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc154-135">CommonParameters</span></span>
<span data-ttu-id="bc154-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc154-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc154-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc154-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc154-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc154-138">INPUTS</span></span>

### <span data-ttu-id="bc154-139">Brak</span><span class="sxs-lookup"><span data-stu-id="bc154-139">None</span></span>

## <span data-ttu-id="bc154-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc154-140">OUTPUTS</span></span>

### <span data-ttu-id="bc154-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="bc154-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="bc154-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc154-142">NOTES</span></span>
<span data-ttu-id="bc154-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="bc154-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bc154-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc154-144">RELATED LINKS</span></span>
