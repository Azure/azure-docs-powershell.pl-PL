---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385945"
---
# <span data-ttu-id="c48dd-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c48dd-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="c48dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c48dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c48dd-103">Tworzy nowy plan zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="c48dd-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="c48dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c48dd-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c48dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c48dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c48dd-106">Tworzy plan zaangażowania w usługę Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c48dd-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="c48dd-107">Jeśli w grupie zasobów istnieje plan zobowiązań o tej samej nazwie, to połączenie działa jako operacja aktualizacji, a istniejący plan zobowiązań zostanie zastąpiony.</span><span class="sxs-lookup"><span data-stu-id="c48dd-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="c48dd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c48dd-108">EXAMPLES</span></span>

### <span data-ttu-id="c48dd-109">Przykład 1. Tworzenie nowego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="c48dd-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="c48dd-110">Tworzy nowy plan zaangażowania w usługę Azure Machine Learning o nazwie "MyCommitmentPlanName" w grupie "Moja zasobów" i w południowo-środkowej Republice Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="c48dd-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="c48dd-111">W tym przykładzie jest używana wersja SKU DevTest/Standard, co oznacza, że zasoby udostępniane przez plan zobowiązań będą definiowane na podstawie limitów DevTest/standardowej.</span><span class="sxs-lookup"><span data-stu-id="c48dd-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="c48dd-112">SkuCapacity w tym przykładzie jest równy 1, co oznacza, że koszt planu będzie spełniać koszt DevTest, a zasoby zawarte w planie będą uzupełniać, co zapewnia DevTest.</span><span class="sxs-lookup"><span data-stu-id="c48dd-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="c48dd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c48dd-113">PARAMETERS</span></span>

### <span data-ttu-id="c48dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48dd-114">-DefaultProfile</span></span>
<span data-ttu-id="c48dd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c48dd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c48dd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c48dd-116">-Force</span></span>
<span data-ttu-id="c48dd-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c48dd-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c48dd-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c48dd-118">-Location</span></span>
<span data-ttu-id="c48dd-119">Lokalizacja planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c48dd-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c48dd-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c48dd-120">-Name</span></span>
<span data-ttu-id="c48dd-121">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c48dd-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c48dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="c48dd-123">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c48dd-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c48dd-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c48dd-124">-SkuCapacity</span></span>
<span data-ttu-id="c48dd-125">Pojemność jednostki SKU używana podczas inicjowania obsługi planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c48dd-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c48dd-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c48dd-126">-SkuName</span></span>
<span data-ttu-id="c48dd-127">Nazwa jednostki SKU używanej podczas inicjowania obsługi planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c48dd-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c48dd-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c48dd-128">-SkuTier</span></span>
<span data-ttu-id="c48dd-129">Warstwa jednostki SKU używana podczas inicjowania obsługi planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c48dd-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c48dd-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c48dd-130">-Confirm</span></span>
<span data-ttu-id="c48dd-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c48dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c48dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c48dd-132">-WhatIf</span></span>
<span data-ttu-id="c48dd-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c48dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48dd-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c48dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c48dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48dd-135">CommonParameters</span></span>
<span data-ttu-id="c48dd-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48dd-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48dd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48dd-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c48dd-138">INPUTS</span></span>

### <span data-ttu-id="c48dd-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c48dd-139">None</span></span>

## <span data-ttu-id="c48dd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c48dd-140">OUTPUTS</span></span>

### <span data-ttu-id="c48dd-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c48dd-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="c48dd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c48dd-142">NOTES</span></span>
<span data-ttu-id="c48dd-143">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="c48dd-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c48dd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c48dd-144">RELATED LINKS</span></span>
