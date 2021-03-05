---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 287db082c5cbe842b0a92b124870effb77068912
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960554"
---
# <span data-ttu-id="af07e-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="af07e-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="af07e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af07e-102">SYNOPSIS</span></span>
<span data-ttu-id="af07e-103">Usuwa plan zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="af07e-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="af07e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af07e-104">SYNTAX</span></span>

### <span data-ttu-id="af07e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="af07e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af07e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="af07e-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af07e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="af07e-107">DESCRIPTION</span></span>
<span data-ttu-id="af07e-108">Usuwa plan zobowiązania usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="af07e-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="af07e-109">Należy pamiętać, że nie można usuwać planów zobowiązania, które mają skojarzenia ze zobowiązaniami.</span><span class="sxs-lookup"><span data-stu-id="af07e-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="af07e-110">Skojarzenia zobowiązania mogą być usuwane tylko przez ich zasób docelowy.</span><span class="sxs-lookup"><span data-stu-id="af07e-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="af07e-111">Jeśli na przykład usuniesz usługę internetową Azure Machine Learning, zostanie również usunięte skojarzenie zobowiązania, które skojarzy usługę sieci Web z planem zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="af07e-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="af07e-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af07e-112">EXAMPLES</span></span>

### <span data-ttu-id="af07e-113">Przykład 1. Usuwanie planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="af07e-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="af07e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af07e-114">PARAMETERS</span></span>

### <span data-ttu-id="af07e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af07e-115">-DefaultProfile</span></span>
<span data-ttu-id="af07e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="af07e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af07e-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="af07e-117">-Force</span></span>
<span data-ttu-id="af07e-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="af07e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="af07e-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="af07e-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="af07e-120">Obiekt usługi sieci Web uczenia maszynowego.</span><span class="sxs-lookup"><span data-stu-id="af07e-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af07e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="af07e-121">-Name</span></span>
<span data-ttu-id="af07e-122">Nazwa planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="af07e-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af07e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af07e-123">-ResourceGroupName</span></span>
<span data-ttu-id="af07e-124">Nazwa grupy zasobów dla planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="af07e-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af07e-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af07e-125">-Confirm</span></span>
<span data-ttu-id="af07e-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="af07e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af07e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af07e-127">-WhatIf</span></span>
<span data-ttu-id="af07e-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af07e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af07e-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="af07e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af07e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af07e-130">CommonParameters</span></span>
<span data-ttu-id="af07e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af07e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af07e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af07e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af07e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af07e-133">INPUTS</span></span>

### <span data-ttu-id="af07e-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="af07e-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="af07e-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af07e-135">OUTPUTS</span></span>

### <span data-ttu-id="af07e-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="af07e-136">System.Void</span></span>

## <span data-ttu-id="af07e-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af07e-137">NOTES</span></span>
<span data-ttu-id="af07e-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="af07e-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="af07e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af07e-139">RELATED LINKS</span></span>
