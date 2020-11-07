---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: e7c296c74aad7e733659930aea9487cf2a73aef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717578"
---
# <span data-ttu-id="00bb2-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="00bb2-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="00bb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="00bb2-103">Aktualizuje właściwości istniejącego zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="00bb2-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00bb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00bb2-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tags <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00bb2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="00bb2-106">Umożliwia zaktualizowanie istniejącego zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="00bb2-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="00bb2-107">Należy zwrócić uwagę, że większość właściwości planu zobowiązań jest niezmienna i nie można jej modyfikować.</span><span class="sxs-lookup"><span data-stu-id="00bb2-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="00bb2-108">Właściwości, które można modyfikować, obejmują jednostkę SKU (co umożliwia migrowanie planu zobowiązań z jednej jednostki SKU do innej) i znaczników.</span><span class="sxs-lookup"><span data-stu-id="00bb2-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="00bb2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="00bb2-110">--------------------------Przykład 1: aktualizowanie planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="00bb2-110">--------------------------  Example 1: Update a commitment plan  --------------------------</span></span>
<span data-ttu-id="00bb2-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="00bb2-111">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="00bb2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00bb2-112">PARAMETERS</span></span>

### <span data-ttu-id="00bb2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="00bb2-113">-Force</span></span>
<span data-ttu-id="00bb2-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00bb2-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="00bb2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00bb2-115">-Name</span></span>
<span data-ttu-id="00bb2-116">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="00bb2-116">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="00bb2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bb2-117">-ResourceGroupName</span></span>
<span data-ttu-id="00bb2-118">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="00bb2-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="00bb2-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="00bb2-119">-SkuCapacity</span></span>
<span data-ttu-id="00bb2-120">Pojemność jednostki SKU używana podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="00bb2-120">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="00bb2-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="00bb2-121">-SkuName</span></span>
<span data-ttu-id="00bb2-122">Nazwa jednostki SKU używanej podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="00bb2-122">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="00bb2-123">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="00bb2-123">-SkuTier</span></span>
<span data-ttu-id="00bb2-124">Warstwa jednostki SKU używana podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="00bb2-124">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="00bb2-125">-Tagi</span><span class="sxs-lookup"><span data-stu-id="00bb2-125">-Tags</span></span>
<span data-ttu-id="00bb2-126">Znaczniki zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="00bb2-126">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="00bb2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00bb2-127">-Confirm</span></span>
<span data-ttu-id="00bb2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00bb2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00bb2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00bb2-129">-WhatIf</span></span>
<span data-ttu-id="00bb2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00bb2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00bb2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="00bb2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00bb2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bb2-132">-DefaultProfile</span></span>
<span data-ttu-id="00bb2-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00bb2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00bb2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bb2-134">CommonParameters</span></span>
<span data-ttu-id="00bb2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bb2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bb2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bb2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bb2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00bb2-137">INPUTS</span></span>

## <span data-ttu-id="00bb2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00bb2-138">OUTPUTS</span></span>

### <span data-ttu-id="00bb2-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="00bb2-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="00bb2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00bb2-140">NOTES</span></span>
<span data-ttu-id="00bb2-141">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="00bb2-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="00bb2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00bb2-142">RELATED LINKS</span></span>

