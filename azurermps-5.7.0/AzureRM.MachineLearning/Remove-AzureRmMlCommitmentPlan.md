---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 6c02b076de3d3f63685938a84e4a437e22c1e16f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554135"
---
# <span data-ttu-id="4dbaf-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4dbaf-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="4dbaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbaf-103">Usuwa plan zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dbaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dbaf-104">SYNTAX</span></span>

### <span data-ttu-id="4dbaf-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4dbaf-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dbaf-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4dbaf-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dbaf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4dbaf-107">DESCRIPTION</span></span>
<span data-ttu-id="4dbaf-108">Usuwa plan zobowiązań do usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="4dbaf-109">Uwaga: nie można usuwać planów zobowiązań mających związek z zobowiązaniem.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="4dbaf-110">Skojarzenia zobowiązań mogą być usuwane tylko przez ich zasoby docelowe.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="4dbaf-111">Jeśli na przykład usuniesz usługę sieci Web Azure Machine Learning, skojarzenie zobowiązania, które kojarzy usługę sieci Web z planem zobowiązań, również zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="4dbaf-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dbaf-112">EXAMPLES</span></span>

### <span data-ttu-id="4dbaf-113">--------------------------Przykład 1: usuwanie planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="4dbaf-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="4dbaf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dbaf-114">PARAMETERS</span></span>

### <span data-ttu-id="4dbaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbaf-115">-DefaultProfile</span></span>
<span data-ttu-id="4dbaf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4dbaf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4dbaf-117">-Force</span></span>
<span data-ttu-id="4dbaf-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4dbaf-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="4dbaf-120">Obiekt usługa sieci Web do nauki maszyn.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-120">The machine learning web service object.</span></span>

```yaml
Type: CommitmentPlan
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4dbaf-121">-Name</span></span>
<span data-ttu-id="4dbaf-122">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbaf-123">-ResourceGroupName</span></span>
<span data-ttu-id="4dbaf-124">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dbaf-125">-Confirm</span></span>
<span data-ttu-id="4dbaf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dbaf-127">-WhatIf</span></span>
<span data-ttu-id="4dbaf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dbaf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbaf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbaf-130">CommonParameters</span></span>
<span data-ttu-id="4dbaf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dbaf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbaf-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dbaf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbaf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dbaf-133">INPUTS</span></span>

### <span data-ttu-id="4dbaf-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4dbaf-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="4dbaf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dbaf-135">OUTPUTS</span></span>

### <span data-ttu-id="4dbaf-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4dbaf-136">None</span></span>

## <span data-ttu-id="4dbaf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dbaf-137">NOTES</span></span>
<span data-ttu-id="4dbaf-138">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="4dbaf-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4dbaf-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dbaf-139">RELATED LINKS</span></span>

