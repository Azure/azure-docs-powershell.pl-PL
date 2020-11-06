---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 0cda9ee6f6a93a43234835104130ea39782f36d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545656"
---
# <span data-ttu-id="b5360-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b5360-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="b5360-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5360-102">SYNOPSIS</span></span>
<span data-ttu-id="b5360-103">Aktualizuje właściwości istniejącego zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b5360-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5360-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5360-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5360-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5360-105">DESCRIPTION</span></span>
<span data-ttu-id="b5360-106">Umożliwia zaktualizowanie istniejącego zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b5360-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="b5360-107">Należy zwrócić uwagę, że większość właściwości planu zobowiązań jest niezmienna i nie można jej modyfikować.</span><span class="sxs-lookup"><span data-stu-id="b5360-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="b5360-108">Właściwości, które można modyfikować, obejmują jednostkę SKU (co umożliwia migrowanie planu zobowiązań z jednej jednostki SKU do innej) i znaczników.</span><span class="sxs-lookup"><span data-stu-id="b5360-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="b5360-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5360-109">EXAMPLES</span></span>

### <span data-ttu-id="b5360-110">Przykład 1: aktualizowanie planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="b5360-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="b5360-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5360-111">PARAMETERS</span></span>

### <span data-ttu-id="b5360-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5360-112">-DefaultProfile</span></span>
<span data-ttu-id="b5360-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b5360-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5360-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b5360-114">-Force</span></span>
<span data-ttu-id="b5360-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b5360-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b5360-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5360-116">-Name</span></span>
<span data-ttu-id="b5360-117">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5360-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5360-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5360-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5360-119">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5360-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5360-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b5360-120">-SkuCapacity</span></span>
<span data-ttu-id="b5360-121">Pojemność jednostki SKU używana podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5360-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5360-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b5360-122">-SkuName</span></span>
<span data-ttu-id="b5360-123">Nazwa jednostki SKU używanej podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5360-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5360-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b5360-124">-SkuTier</span></span>
<span data-ttu-id="b5360-125">Warstwa jednostki SKU używana podczas aktualizowania planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5360-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5360-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5360-126">-Tag</span></span>
<span data-ttu-id="b5360-127">Znaczniki zasobu planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b5360-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5360-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5360-128">-Confirm</span></span>
<span data-ttu-id="b5360-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5360-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5360-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5360-130">-WhatIf</span></span>
<span data-ttu-id="b5360-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5360-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5360-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5360-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5360-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5360-133">CommonParameters</span></span>
<span data-ttu-id="b5360-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5360-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5360-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5360-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5360-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5360-136">INPUTS</span></span>

### <span data-ttu-id="b5360-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5360-137">None</span></span>
<span data-ttu-id="b5360-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b5360-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5360-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5360-139">OUTPUTS</span></span>

### <span data-ttu-id="b5360-140">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b5360-140">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b5360-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5360-141">NOTES</span></span>
<span data-ttu-id="b5360-142">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="b5360-142">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b5360-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5360-143">RELATED LINKS</span></span>
