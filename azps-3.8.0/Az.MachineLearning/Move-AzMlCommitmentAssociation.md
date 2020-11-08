---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053207"
---
# <span data-ttu-id="9b182-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="9b182-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="9b182-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b182-102">SYNOPSIS</span></span>
<span data-ttu-id="9b182-103">Przenosi stowarzyszenie zobowiązań z jednego planu zobowiązań do innego.</span><span class="sxs-lookup"><span data-stu-id="9b182-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="9b182-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b182-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b182-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b182-105">DESCRIPTION</span></span>
<span data-ttu-id="9b182-106">Przenosi zasób skojarzenia zobowiązań z planu zobowiązań nadrzędnych do innego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="9b182-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="9b182-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b182-107">EXAMPLES</span></span>

### <span data-ttu-id="9b182-108">Przykład 1: przenoszenie powiązania zobowiązań</span><span class="sxs-lookup"><span data-stu-id="9b182-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="9b182-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b182-109">PARAMETERS</span></span>

### <span data-ttu-id="9b182-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="9b182-110">-CommitmentPlanName</span></span>
<span data-ttu-id="9b182-111">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9b182-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="9b182-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b182-112">-DefaultProfile</span></span>
<span data-ttu-id="9b182-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9b182-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b182-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="9b182-114">-DestinationPlanId</span></span>
<span data-ttu-id="9b182-115">Identyfikator zasobu platformy Azure docelowego planu zobowiązań usługi Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9b182-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="9b182-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b182-116">-Name</span></span>
<span data-ttu-id="9b182-117">Nazwa zrzeszenia zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9b182-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="9b182-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b182-118">-ResourceGroupName</span></span>
<span data-ttu-id="9b182-119">Nazwa grupy zasobów dla stowarzyszenia zobowiązanie na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9b182-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="9b182-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b182-120">-Confirm</span></span>
<span data-ttu-id="9b182-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b182-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b182-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b182-122">-WhatIf</span></span>
<span data-ttu-id="9b182-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b182-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b182-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b182-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b182-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b182-125">CommonParameters</span></span>
<span data-ttu-id="9b182-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b182-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b182-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b182-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b182-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b182-128">INPUTS</span></span>

### <span data-ttu-id="9b182-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9b182-129">None</span></span>

## <span data-ttu-id="9b182-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b182-130">OUTPUTS</span></span>

### <span data-ttu-id="9b182-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="9b182-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="9b182-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b182-132">NOTES</span></span>
<span data-ttu-id="9b182-133">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="9b182-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9b182-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b182-134">RELATED LINKS</span></span>
