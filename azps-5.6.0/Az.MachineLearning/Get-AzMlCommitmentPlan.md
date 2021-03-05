---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: b3ea89f2470052a0d5858da199ee5285b3d5ea18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965825"
---
# <span data-ttu-id="3ee28-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3ee28-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="3ee28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee28-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee28-103">Pobiera informacje podsumowujące dla jednego lub większej liczby planów zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="3ee28-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="3ee28-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ee28-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee28-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ee28-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee28-106">Pobiera informacje o planie zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="3ee28-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="3ee28-107">W zależności od przekazanych parametrów polecenie cmdlet zwraca określony plan zobowiązania, kolekcję planów zobowiązania dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję planów zobowiązania w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3ee28-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="3ee28-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ee28-108">EXAMPLES</span></span>

### <span data-ttu-id="3ee28-109">Przykład 1. Uzyskiwanie konkretnego planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="3ee28-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="3ee28-110">Przykład 2. Uzyskiwanie wszystkich zasobów planu zobowiązania w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3ee28-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="3ee28-111">Przykład 3. Uzyskiwanie wszystkich planów zobowiązania w bieżącej subskrypcji i danej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="3ee28-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="3ee28-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ee28-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee28-113">-DefaultProfile</span></span>
<span data-ttu-id="3ee28-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3ee28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ee28-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3ee28-115">-Name</span></span>
<span data-ttu-id="3ee28-116">Nazwa planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="3ee28-116">The name of the commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee28-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ee28-118">Nazwa grupy zasobów dla planu zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3ee28-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee28-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee28-119">CommonParameters</span></span>
<span data-ttu-id="3ee28-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee28-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee28-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee28-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee28-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ee28-122">INPUTS</span></span>

### <span data-ttu-id="3ee28-123">Brak</span><span class="sxs-lookup"><span data-stu-id="3ee28-123">None</span></span>

## <span data-ttu-id="3ee28-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ee28-124">OUTPUTS</span></span>

### <span data-ttu-id="3ee28-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3ee28-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3ee28-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ee28-126">NOTES</span></span>
<span data-ttu-id="3ee28-127">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3ee28-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3ee28-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ee28-128">RELATED LINKS</span></span>
