---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553840"
---
# <span data-ttu-id="eea4d-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="eea4d-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="eea4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eea4d-102">SYNOPSIS</span></span>
<span data-ttu-id="eea4d-103">Przenosi stowarzyszenie zobowiązań z jednego planu zobowiązań do innego.</span><span class="sxs-lookup"><span data-stu-id="eea4d-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eea4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eea4d-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eea4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eea4d-105">DESCRIPTION</span></span>
<span data-ttu-id="eea4d-106">Przenosi zasób skojarzenia zobowiązań z planu zobowiązań nadrzędnych do innego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="eea4d-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="eea4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eea4d-107">EXAMPLES</span></span>

### <span data-ttu-id="eea4d-108">--------------------------Przykład 1: przenoszenie skojarzeń zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="eea4d-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="eea4d-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="eea4d-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="eea4d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eea4d-110">PARAMETERS</span></span>

### <span data-ttu-id="eea4d-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="eea4d-111">-CommitmentPlanName</span></span>
<span data-ttu-id="eea4d-112">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="eea4d-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eea4d-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="eea4d-113">-DestinationPlanId</span></span>
<span data-ttu-id="eea4d-114">Identyfikator zasobu platformy Azure docelowego planu zobowiązań usługi Azure ML.</span><span class="sxs-lookup"><span data-stu-id="eea4d-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eea4d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eea4d-115">-Name</span></span>
<span data-ttu-id="eea4d-116">Nazwa zrzeszenia zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="eea4d-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="eea4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="eea4d-118">Nazwa grupy zasobów dla stowarzyszenia zobowiązanie na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="eea4d-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="eea4d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eea4d-119">-Confirm</span></span>
<span data-ttu-id="eea4d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea4d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea4d-121">-WhatIf</span></span>
<span data-ttu-id="eea4d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea4d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eea4d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eea4d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea4d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea4d-124">-DefaultProfile</span></span>
<span data-ttu-id="eea4d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eea4d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea4d-126">CommonParameters</span></span>
<span data-ttu-id="eea4d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea4d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea4d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea4d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eea4d-129">INPUTS</span></span>

## <span data-ttu-id="eea4d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eea4d-130">OUTPUTS</span></span>

### <span data-ttu-id="eea4d-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="eea4d-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="eea4d-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="eea4d-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="eea4d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eea4d-133">NOTES</span></span>
<span data-ttu-id="eea4d-134">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="eea4d-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="eea4d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eea4d-135">RELATED LINKS</span></span>

