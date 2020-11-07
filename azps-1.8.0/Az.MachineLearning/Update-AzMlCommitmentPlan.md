---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: c1aa160d7a0773569255f425f3993de0b47d552a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867496"
---
# <span data-ttu-id="a608c-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a608c-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a608c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a608c-102">SYNOPSIS</span></span>
<span data-ttu-id="a608c-103">Aktualizuje właściwości istniejącego zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a608c-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="a608c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a608c-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a608c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a608c-105">DESCRIPTION</span></span>
<span data-ttu-id="a608c-106">Umożliwia zaktualizowanie istniejącego zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a608c-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="a608c-107">Należy zwrócić uwagę, że większość właściwości planu zobowiązań jest niezmienna i nie można jej modyfikować.</span><span class="sxs-lookup"><span data-stu-id="a608c-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="a608c-108">Właściwości, które można modyfikować, obejmują jednostkę SKU (co umożliwia migrowanie planu zobowiązań z jednej jednostki SKU do innej) i znaczników.</span><span class="sxs-lookup"><span data-stu-id="a608c-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="a608c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a608c-109">EXAMPLES</span></span>

### <span data-ttu-id="a608c-110">Przykład 1: aktualizowanie planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="a608c-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="a608c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a608c-111">PARAMETERS</span></span>

### <span data-ttu-id="a608c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a608c-112">-DefaultProfile</span></span>
<span data-ttu-id="a608c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a608c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a608c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a608c-114">-Force</span></span>
<span data-ttu-id="a608c-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a608c-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a608c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a608c-116">-Name</span></span>
<span data-ttu-id="a608c-117">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a608c-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a608c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a608c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a608c-119">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a608c-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a608c-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a608c-120">-SkuCapacity</span></span>
<span data-ttu-id="a608c-121">Pojemność jednostki SKU używana podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a608c-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a608c-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a608c-122">-SkuName</span></span>
<span data-ttu-id="a608c-123">Nazwa jednostki SKU używanej podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a608c-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a608c-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a608c-124">-SkuTier</span></span>
<span data-ttu-id="a608c-125">Warstwa jednostki SKU używana podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a608c-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a608c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a608c-126">-Tag</span></span>
<span data-ttu-id="a608c-127">Znaczniki zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a608c-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="a608c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a608c-128">-Confirm</span></span>
<span data-ttu-id="a608c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a608c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a608c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a608c-130">-WhatIf</span></span>
<span data-ttu-id="a608c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a608c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a608c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a608c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a608c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a608c-133">CommonParameters</span></span>
<span data-ttu-id="a608c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a608c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a608c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a608c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a608c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a608c-136">INPUTS</span></span>

### <span data-ttu-id="a608c-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a608c-137">None</span></span>

## <span data-ttu-id="a608c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a608c-138">OUTPUTS</span></span>

### <span data-ttu-id="a608c-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a608c-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a608c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a608c-140">NOTES</span></span>
<span data-ttu-id="a608c-141">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="a608c-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a608c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a608c-142">RELATED LINKS</span></span>
