---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d2745a0dd73141c1da7d049494e3a1545ee92599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552756"
---
# <span data-ttu-id="7e21e-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7e21e-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="7e21e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e21e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e21e-103">Tworzy nowy plan zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="7e21e-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e21e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e21e-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e21e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e21e-105">DESCRIPTION</span></span>
<span data-ttu-id="7e21e-106">Tworzy plan zaangażowania w usługę Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e21e-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="7e21e-107">Jeśli w grupie zasobów istnieje plan zobowiązań o tej samej nazwie, to połączenie działa jako operacja aktualizacji, a istniejący plan zobowiązań zostanie zastąpiony.</span><span class="sxs-lookup"><span data-stu-id="7e21e-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="7e21e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e21e-108">EXAMPLES</span></span>

### <span data-ttu-id="7e21e-109">Przykład 1. Tworzenie nowego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="7e21e-109">Example 1: Create a new commitment plan</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="7e21e-110">Tworzy nowy plan zaangażowania w usługę Azure Machine Learning o nazwie "MyCommitmentPlanName" w grupie "Moja zasobów" i w południowo-środkowej Republice Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="7e21e-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="7e21e-111">W tym przykładzie jest używana wersja SKU DevTest/Standard, co oznacza, że zasoby udostępniane przez plan zobowiązań będą definied przez limity DevTest/standardowe.</span><span class="sxs-lookup"><span data-stu-id="7e21e-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="7e21e-112">SkuCapacity w tym przykładzie jest równy 1, co oznacza, że koszt planu będzie spełniać koszt DevTest, a zasoby zawarte w planie będą uzupełniać, co zapewnia DevTest.</span><span class="sxs-lookup"><span data-stu-id="7e21e-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="7e21e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e21e-113">PARAMETERS</span></span>

### <span data-ttu-id="7e21e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e21e-114">-DefaultProfile</span></span>
<span data-ttu-id="7e21e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7e21e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e21e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7e21e-116">-Force</span></span>
<span data-ttu-id="7e21e-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e21e-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7e21e-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7e21e-118">-Location</span></span>
<span data-ttu-id="7e21e-119">Lokalizacja planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7e21e-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7e21e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e21e-120">-Name</span></span>
<span data-ttu-id="7e21e-121">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7e21e-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7e21e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e21e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e21e-123">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7e21e-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7e21e-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7e21e-124">-SkuCapacity</span></span>
<span data-ttu-id="7e21e-125">Pojemność jednostki SKU używana podczas inicjowania obsługi planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7e21e-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7e21e-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e21e-126">-SkuName</span></span>
<span data-ttu-id="7e21e-127">Nazwa jednostki SKU używanej podczas inicjowania obsługi planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7e21e-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7e21e-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7e21e-128">-SkuTier</span></span>
<span data-ttu-id="7e21e-129">Warstwa jednostki SKU używana podczas inicjowania obsługi planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7e21e-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7e21e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e21e-130">-Confirm</span></span>
<span data-ttu-id="7e21e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e21e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e21e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e21e-132">-WhatIf</span></span>
<span data-ttu-id="7e21e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e21e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e21e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e21e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e21e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e21e-135">CommonParameters</span></span>
<span data-ttu-id="7e21e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e21e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e21e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e21e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e21e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e21e-138">INPUTS</span></span>

### <span data-ttu-id="7e21e-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7e21e-139">None</span></span>

## <span data-ttu-id="7e21e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e21e-140">OUTPUTS</span></span>

### <span data-ttu-id="7e21e-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7e21e-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7e21e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e21e-142">NOTES</span></span>
<span data-ttu-id="7e21e-143">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="7e21e-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7e21e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e21e-144">RELATED LINKS</span></span>
