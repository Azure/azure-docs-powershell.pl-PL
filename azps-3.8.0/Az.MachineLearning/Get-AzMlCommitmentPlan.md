---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053212"
---
# <span data-ttu-id="0d991-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0d991-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="0d991-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d991-102">SYNOPSIS</span></span>
<span data-ttu-id="0d991-103">Pobiera informacje podsumowujące dla co najmniej jednego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="0d991-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="0d991-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d991-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d991-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d991-105">DESCRIPTION</span></span>
<span data-ttu-id="0d991-106">Pobiera informacje dotyczące planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="0d991-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="0d991-107">W zależności od przekazanych parametrów polecenie cmdlet zwraca określony plan zobowiązań, kolekcję planów zobowiązań dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję planów zobowiązań w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0d991-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="0d991-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d991-108">EXAMPLES</span></span>

### <span data-ttu-id="0d991-109">Przykład 1: uzyskiwanie określonego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="0d991-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="0d991-110">Przykład 2: pobieranie wszystkich zasobów planu zobowiązań w bieżącym abonamentzie</span><span class="sxs-lookup"><span data-stu-id="0d991-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="0d991-111">Przykład 3: pobieranie wszystkich planów zobowiązań w bieżącym abonamentu i danej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="0d991-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="0d991-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d991-112">PARAMETERS</span></span>

### <span data-ttu-id="0d991-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d991-113">-DefaultProfile</span></span>
<span data-ttu-id="0d991-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0d991-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d991-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d991-115">-Name</span></span>
<span data-ttu-id="0d991-116">Nazwa planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="0d991-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="0d991-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d991-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d991-118">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="0d991-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="0d991-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d991-119">CommonParameters</span></span>
<span data-ttu-id="0d991-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d991-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d991-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d991-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d991-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d991-122">INPUTS</span></span>

### <span data-ttu-id="0d991-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0d991-123">None</span></span>

## <span data-ttu-id="0d991-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d991-124">OUTPUTS</span></span>

### <span data-ttu-id="0d991-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0d991-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="0d991-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d991-126">NOTES</span></span>
<span data-ttu-id="0d991-127">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="0d991-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0d991-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d991-128">RELATED LINKS</span></span>
