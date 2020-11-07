---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719629"
---
# <span data-ttu-id="74d26-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="74d26-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="74d26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74d26-102">SYNOPSIS</span></span>
<span data-ttu-id="74d26-103">Usuwa plan zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="74d26-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74d26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74d26-104">SYNTAX</span></span>

### <span data-ttu-id="74d26-105">Usuwanie planu zobowiązań usługi Azure ML określonego przez nazwę i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="74d26-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d26-106">Usuwanie planu zobowiązań usługi Azure ML określonego jako obiekt.</span><span class="sxs-lookup"><span data-stu-id="74d26-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d26-107">Opis</span><span class="sxs-lookup"><span data-stu-id="74d26-107">DESCRIPTION</span></span>
<span data-ttu-id="74d26-108">Usuwa plan zobowiązań do usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="74d26-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="74d26-109">Uwaga: nie można usuwać planów zobowiązań mających związek z zobowiązaniem.</span><span class="sxs-lookup"><span data-stu-id="74d26-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="74d26-110">Skojarzenia zobowiązań mogą być usuwane tylko przez ich zasoby docelowe.</span><span class="sxs-lookup"><span data-stu-id="74d26-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="74d26-111">Jeśli na przykład usuniesz usługę sieci Web Azure Machine Learning, skojarzenie zobowiązania, które kojarzy usługę sieci Web z planem zobowiązań, również zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="74d26-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="74d26-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74d26-112">EXAMPLES</span></span>

### <span data-ttu-id="74d26-113">--------------------------Przykład 1: usuwanie planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="74d26-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="74d26-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="74d26-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="74d26-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74d26-115">PARAMETERS</span></span>

### <span data-ttu-id="74d26-116">-Force</span><span class="sxs-lookup"><span data-stu-id="74d26-116">-Force</span></span>
<span data-ttu-id="74d26-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74d26-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74d26-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="74d26-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="74d26-119">Obiekt usługa sieci Web do nauki maszyn.</span><span class="sxs-lookup"><span data-stu-id="74d26-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d26-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74d26-120">-Name</span></span>
<span data-ttu-id="74d26-121">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="74d26-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d26-122">-ResourceGroupName</span></span>
<span data-ttu-id="74d26-123">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="74d26-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d26-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74d26-124">-Confirm</span></span>
<span data-ttu-id="74d26-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d26-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d26-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d26-126">-WhatIf</span></span>
<span data-ttu-id="74d26-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d26-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74d26-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74d26-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d26-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d26-129">-DefaultProfile</span></span>
<span data-ttu-id="74d26-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74d26-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d26-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d26-131">CommonParameters</span></span>
<span data-ttu-id="74d26-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d26-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d26-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d26-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d26-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74d26-134">INPUTS</span></span>

### <span data-ttu-id="74d26-135">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="74d26-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="74d26-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74d26-136">OUTPUTS</span></span>

### <span data-ttu-id="74d26-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="74d26-137">None</span></span>

## <span data-ttu-id="74d26-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74d26-138">NOTES</span></span>
<span data-ttu-id="74d26-139">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="74d26-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="74d26-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74d26-140">RELATED LINKS</span></span>

