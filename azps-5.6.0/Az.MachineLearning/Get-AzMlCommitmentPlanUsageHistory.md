---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 8baf0e2af5ebc06e51c0f8b588fe04ff3106f892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009626"
---
# <span data-ttu-id="80ccb-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="80ccb-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="80ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="80ccb-103">Pobiera informacje historii użycia dla określonego planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="80ccb-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="80ccb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80ccb-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80ccb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="80ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="80ccb-106">Pobiera informacje historii użycia dla określonego planu zobowiązania, w tym używane zasoby i zasoby pozostałe w planie.</span><span class="sxs-lookup"><span data-stu-id="80ccb-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="80ccb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="80ccb-108">Przykład 1. Uzyskiwanie historii użycia określonego planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="80ccb-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="80ccb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80ccb-109">PARAMETERS</span></span>

### <span data-ttu-id="80ccb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ccb-110">-DefaultProfile</span></span>
<span data-ttu-id="80ccb-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="80ccb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80ccb-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80ccb-112">-Name</span></span>
<span data-ttu-id="80ccb-113">Nazwa planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="80ccb-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="80ccb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ccb-114">-ResourceGroupName</span></span>
<span data-ttu-id="80ccb-115">Nazwa grupy zasobów dla planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="80ccb-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="80ccb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ccb-116">CommonParameters</span></span>
<span data-ttu-id="80ccb-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ccb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ccb-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ccb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ccb-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80ccb-119">INPUTS</span></span>

### <span data-ttu-id="80ccb-120">Brak</span><span class="sxs-lookup"><span data-stu-id="80ccb-120">None</span></span>

## <span data-ttu-id="80ccb-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80ccb-121">OUTPUTS</span></span>

### <span data-ttu-id="80ccb-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="80ccb-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="80ccb-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80ccb-123">NOTES</span></span>
<span data-ttu-id="80ccb-124">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="80ccb-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="80ccb-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80ccb-125">RELATED LINKS</span></span>
