---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051754"
---
# <span data-ttu-id="b6cd9-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="b6cd9-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="b6cd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cd9-103">Pobiera informacje podsumowujące dla jednego lub większej liczby skojarzeń zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="b6cd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6cd9-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6cd9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="b6cd9-106">Pobiera informacje o stowarzyszeniu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="b6cd9-107">W zależności od przekazanych parametrów polecenie cmdlet zwraca określone powiązanie zobowiązań lub kolekcję skojarzeń zobowiązań dla określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="b6cd9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6cd9-108">EXAMPLES</span></span>

### <span data-ttu-id="b6cd9-109">Przykład 1: uzyskiwanie określonego stowarzyszenia zobowiązań</span><span class="sxs-lookup"><span data-stu-id="b6cd9-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="b6cd9-110">Przykład 2: uzyskiwanie wszystkich skojarzeń zobowiązań dla określonego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="b6cd9-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="b6cd9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6cd9-111">PARAMETERS</span></span>

### <span data-ttu-id="b6cd9-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="b6cd9-112">-CommitmentPlanName</span></span>
<span data-ttu-id="b6cd9-113">Nazwa planu zobowiązań usługi Azure ML, który ma jedno lub więcej skojarzeń zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="b6cd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cd9-114">-DefaultProfile</span></span>
<span data-ttu-id="b6cd9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6cd9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6cd9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6cd9-116">-Name</span></span>
<span data-ttu-id="b6cd9-117">Nazwa zrzeszenia zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="b6cd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6cd9-119">Nazwa grupy zasobów dla stowarzyszenia zobowiązanie na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="b6cd9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cd9-120">CommonParameters</span></span>
<span data-ttu-id="b6cd9-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cd9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cd9-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cd9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cd9-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6cd9-123">INPUTS</span></span>

### <span data-ttu-id="b6cd9-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6cd9-124">None</span></span>

## <span data-ttu-id="b6cd9-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6cd9-125">OUTPUTS</span></span>

### <span data-ttu-id="b6cd9-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b6cd9-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b6cd9-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6cd9-127">NOTES</span></span>
<span data-ttu-id="b6cd9-128">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="b6cd9-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b6cd9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6cd9-129">RELATED LINKS</span></span>
