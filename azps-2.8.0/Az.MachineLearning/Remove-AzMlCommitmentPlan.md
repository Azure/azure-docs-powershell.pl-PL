---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 1c022d8ae97ac9f1e51bbabaff15a9dec61f5d87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704932"
---
# <span data-ttu-id="45107-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="45107-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="45107-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45107-102">SYNOPSIS</span></span>
<span data-ttu-id="45107-103">Usuwa plan zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="45107-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="45107-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45107-104">SYNTAX</span></span>

### <span data-ttu-id="45107-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45107-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45107-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="45107-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45107-107">Opis</span><span class="sxs-lookup"><span data-stu-id="45107-107">DESCRIPTION</span></span>
<span data-ttu-id="45107-108">Usuwa plan zobowiązań do usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="45107-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="45107-109">Uwaga: nie można usuwać planów zobowiązań mających związek z zobowiązaniem.</span><span class="sxs-lookup"><span data-stu-id="45107-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="45107-110">Skojarzenia zobowiązań mogą być usuwane tylko przez ich zasoby docelowe.</span><span class="sxs-lookup"><span data-stu-id="45107-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="45107-111">Jeśli na przykład usuniesz usługę sieci Web Azure Machine Learning, skojarzenie zobowiązania, które kojarzy usługę sieci Web z planem zobowiązań, również zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="45107-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="45107-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45107-112">EXAMPLES</span></span>

### <span data-ttu-id="45107-113">Przykład 1: usuwanie planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="45107-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="45107-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45107-114">PARAMETERS</span></span>

### <span data-ttu-id="45107-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45107-115">-DefaultProfile</span></span>
<span data-ttu-id="45107-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="45107-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45107-117">-Force</span><span class="sxs-lookup"><span data-stu-id="45107-117">-Force</span></span>
<span data-ttu-id="45107-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45107-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="45107-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="45107-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="45107-120">Obiekt usługa sieci Web do nauki maszyn.</span><span class="sxs-lookup"><span data-stu-id="45107-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="45107-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45107-121">-Name</span></span>
<span data-ttu-id="45107-122">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="45107-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="45107-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45107-123">-ResourceGroupName</span></span>
<span data-ttu-id="45107-124">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="45107-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="45107-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45107-125">-Confirm</span></span>
<span data-ttu-id="45107-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45107-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45107-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45107-127">-WhatIf</span></span>
<span data-ttu-id="45107-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45107-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45107-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45107-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45107-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45107-130">CommonParameters</span></span>
<span data-ttu-id="45107-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45107-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45107-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45107-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45107-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45107-133">INPUTS</span></span>

### <span data-ttu-id="45107-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="45107-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="45107-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45107-135">OUTPUTS</span></span>

### <span data-ttu-id="45107-136">System. void</span><span class="sxs-lookup"><span data-stu-id="45107-136">System.Void</span></span>

## <span data-ttu-id="45107-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45107-137">NOTES</span></span>
<span data-ttu-id="45107-138">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="45107-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="45107-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45107-139">RELATED LINKS</span></span>
