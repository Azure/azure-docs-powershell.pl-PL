---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554142"
---
# <span data-ttu-id="44cd9-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="44cd9-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="44cd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="44cd9-103">Przenosi stowarzyszenie zobowiązań z jednego planu zobowiązań do innego.</span><span class="sxs-lookup"><span data-stu-id="44cd9-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44cd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44cd9-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44cd9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="44cd9-106">Przenosi zasób skojarzenia zobowiązań z planu zobowiązań nadrzędnych do innego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="44cd9-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="44cd9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44cd9-107">EXAMPLES</span></span>

### <span data-ttu-id="44cd9-108">--------------------------Przykład 1: przenoszenie skojarzeń zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="44cd9-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="44cd9-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44cd9-109">PARAMETERS</span></span>

### <span data-ttu-id="44cd9-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="44cd9-110">-CommitmentPlanName</span></span>
<span data-ttu-id="44cd9-111">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="44cd9-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="44cd9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cd9-112">-DefaultProfile</span></span>
<span data-ttu-id="44cd9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="44cd9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44cd9-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="44cd9-114">-DestinationPlanId</span></span>
<span data-ttu-id="44cd9-115">Identyfikator zasobu platformy Azure docelowego planu zobowiązań usługi Azure ML.</span><span class="sxs-lookup"><span data-stu-id="44cd9-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="44cd9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44cd9-116">-Name</span></span>
<span data-ttu-id="44cd9-117">Nazwa zrzeszenia zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="44cd9-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="44cd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="44cd9-119">Nazwa grupy zasobów dla stowarzyszenia zobowiązanie na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="44cd9-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="44cd9-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44cd9-120">-Confirm</span></span>
<span data-ttu-id="44cd9-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cd9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44cd9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44cd9-122">-WhatIf</span></span>
<span data-ttu-id="44cd9-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cd9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44cd9-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44cd9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44cd9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cd9-125">CommonParameters</span></span>
<span data-ttu-id="44cd9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cd9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cd9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cd9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cd9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44cd9-128">INPUTS</span></span>

### <span data-ttu-id="44cd9-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="44cd9-129">None</span></span>
<span data-ttu-id="44cd9-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="44cd9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44cd9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44cd9-131">OUTPUTS</span></span>

### <span data-ttu-id="44cd9-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="44cd9-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="44cd9-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="44cd9-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="44cd9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44cd9-134">NOTES</span></span>
<span data-ttu-id="44cd9-135">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="44cd9-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="44cd9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44cd9-136">RELATED LINKS</span></span>

