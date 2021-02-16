---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187539"
---
# <span data-ttu-id="b6265-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b6265-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="b6265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6265-102">SYNOPSIS</span></span>
<span data-ttu-id="b6265-103">Pobiera informacje historii użycia dla określonego planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="b6265-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="b6265-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6265-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6265-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6265-105">DESCRIPTION</span></span>
<span data-ttu-id="b6265-106">Pobiera informacje historii użycia dla określonego planu zobowiązania, w tym używane zasoby i zasoby pozostałe w planie.</span><span class="sxs-lookup"><span data-stu-id="b6265-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="b6265-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6265-107">EXAMPLES</span></span>

### <span data-ttu-id="b6265-108">Przykład 1. Uzyskiwanie historii użycia określonego planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="b6265-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="b6265-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6265-109">PARAMETERS</span></span>

### <span data-ttu-id="b6265-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6265-110">-DefaultProfile</span></span>
<span data-ttu-id="b6265-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b6265-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6265-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6265-112">-Name</span></span>
<span data-ttu-id="b6265-113">Nazwa planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b6265-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b6265-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6265-114">-ResourceGroupName</span></span>
<span data-ttu-id="b6265-115">Nazwa grupy zasobów dla planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b6265-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b6265-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6265-116">CommonParameters</span></span>
<span data-ttu-id="b6265-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6265-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6265-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6265-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6265-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6265-119">INPUTS</span></span>

### <span data-ttu-id="b6265-120">Brak</span><span class="sxs-lookup"><span data-stu-id="b6265-120">None</span></span>

## <span data-ttu-id="b6265-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6265-121">OUTPUTS</span></span>

### <span data-ttu-id="b6265-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b6265-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="b6265-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6265-123">NOTES</span></span>
<span data-ttu-id="b6265-124">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b6265-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b6265-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6265-125">RELATED LINKS</span></span>
