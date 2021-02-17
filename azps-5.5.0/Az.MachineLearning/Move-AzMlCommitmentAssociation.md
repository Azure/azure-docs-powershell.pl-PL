---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192275"
---
# <span data-ttu-id="2ec27-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="2ec27-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="2ec27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec27-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec27-103">Przenosi skojarzenie zobowiązania z jednego planu zobowiązania do innego.</span><span class="sxs-lookup"><span data-stu-id="2ec27-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="2ec27-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ec27-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ec27-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ec27-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec27-106">Przenosi zasób skojarzenia zobowiązania z jego nadrzędnego planu zobowiązania do innego planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="2ec27-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="2ec27-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ec27-107">EXAMPLES</span></span>

### <span data-ttu-id="2ec27-108">Przykład 1. Przenoszenie skojarzenia zobowiązania</span><span class="sxs-lookup"><span data-stu-id="2ec27-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="2ec27-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ec27-109">PARAMETERS</span></span>

### <span data-ttu-id="2ec27-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="2ec27-110">-CommitmentPlanName</span></span>
<span data-ttu-id="2ec27-111">Nazwa planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="2ec27-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2ec27-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec27-112">-DefaultProfile</span></span>
<span data-ttu-id="2ec27-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2ec27-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ec27-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="2ec27-114">-DestinationPlanId</span></span>
<span data-ttu-id="2ec27-115">Identyfikator zasobu Azure docelowego planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="2ec27-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2ec27-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ec27-116">-Name</span></span>
<span data-ttu-id="2ec27-117">Nazwa skojarzenia zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="2ec27-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="2ec27-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec27-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ec27-119">Nazwa grupy zasobów dla skojarzenia zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="2ec27-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="2ec27-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ec27-120">-Confirm</span></span>
<span data-ttu-id="2ec27-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ec27-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec27-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec27-122">-WhatIf</span></span>
<span data-ttu-id="2ec27-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec27-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ec27-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ec27-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec27-125">CommonParameters</span></span>
<span data-ttu-id="2ec27-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec27-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec27-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec27-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ec27-128">INPUTS</span></span>

### <span data-ttu-id="2ec27-129">Brak</span><span class="sxs-lookup"><span data-stu-id="2ec27-129">None</span></span>

## <span data-ttu-id="2ec27-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ec27-130">OUTPUTS</span></span>

### <span data-ttu-id="2ec27-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2ec27-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="2ec27-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ec27-132">NOTES</span></span>
<span data-ttu-id="2ec27-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2ec27-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2ec27-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ec27-134">RELATED LINKS</span></span>
