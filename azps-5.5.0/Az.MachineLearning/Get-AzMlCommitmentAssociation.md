---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194170"
---
# <span data-ttu-id="09717-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="09717-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="09717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09717-102">SYNOPSIS</span></span>
<span data-ttu-id="09717-103">Pobiera informacje podsumowujące dla co najmniej jednego skojarzenia zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="09717-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="09717-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09717-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09717-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="09717-105">DESCRIPTION</span></span>
<span data-ttu-id="09717-106">Pobiera informacje o skojarzeniach zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="09717-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="09717-107">W zależności od przekazanych parametrów polecenie cmdlet zwraca określone skojarzenie zobowiązania lub kolekcję skojarzeń zobowiązania dla określonego planu zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="09717-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="09717-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09717-108">EXAMPLES</span></span>

### <span data-ttu-id="09717-109">Przykład 1. Uzyskiwanie określonego skojarzenia zobowiązania</span><span class="sxs-lookup"><span data-stu-id="09717-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="09717-110">Przykład 2. Pobierz wszystkie skojarzenia dla określonego planu zobowiązania</span><span class="sxs-lookup"><span data-stu-id="09717-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="09717-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09717-111">PARAMETERS</span></span>

### <span data-ttu-id="09717-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="09717-112">-CommitmentPlanName</span></span>
<span data-ttu-id="09717-113">Nazwa planu zobowiązania Azure ML, który ma co najmniej jedno skojarzenia zobowiązania.</span><span class="sxs-lookup"><span data-stu-id="09717-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="09717-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09717-114">-DefaultProfile</span></span>
<span data-ttu-id="09717-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="09717-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09717-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09717-116">-Name</span></span>
<span data-ttu-id="09717-117">Nazwa skojarzenia zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="09717-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="09717-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09717-118">-ResourceGroupName</span></span>
<span data-ttu-id="09717-119">Nazwa grupy zasobów dla skojarzenia zobowiązania Azure ML.</span><span class="sxs-lookup"><span data-stu-id="09717-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="09717-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09717-120">CommonParameters</span></span>
<span data-ttu-id="09717-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09717-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09717-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09717-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09717-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09717-123">INPUTS</span></span>

### <span data-ttu-id="09717-124">Brak</span><span class="sxs-lookup"><span data-stu-id="09717-124">None</span></span>

## <span data-ttu-id="09717-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09717-125">OUTPUTS</span></span>

### <span data-ttu-id="09717-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="09717-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="09717-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09717-127">NOTES</span></span>
<span data-ttu-id="09717-128">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="09717-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="09717-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09717-129">RELATED LINKS</span></span>
