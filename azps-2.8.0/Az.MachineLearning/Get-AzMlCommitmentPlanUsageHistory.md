---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 4d78d6e6a1b0ae5ea9f8815d537bca1496e24bbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704951"
---
# <span data-ttu-id="48d45-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="48d45-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="48d45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48d45-102">SYNOPSIS</span></span>
<span data-ttu-id="48d45-103">Pobiera informacje o historii użycia określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="48d45-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="48d45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48d45-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48d45-105">DESCRIPTION</span></span>
<span data-ttu-id="48d45-106">Pobiera informacje o historii użycia określonego planu zobowiązań, w tym zasobów używanych i zasobów pozostałych w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="48d45-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="48d45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48d45-107">EXAMPLES</span></span>

### <span data-ttu-id="48d45-108">Przykład 1: uzyskiwanie historii użycia dla określonego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="48d45-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="48d45-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48d45-109">PARAMETERS</span></span>

### <span data-ttu-id="48d45-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d45-110">-DefaultProfile</span></span>
<span data-ttu-id="48d45-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="48d45-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48d45-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48d45-112">-Name</span></span>
<span data-ttu-id="48d45-113">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="48d45-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="48d45-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d45-114">-ResourceGroupName</span></span>
<span data-ttu-id="48d45-115">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="48d45-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="48d45-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d45-116">CommonParameters</span></span>
<span data-ttu-id="48d45-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d45-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d45-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d45-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d45-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48d45-119">INPUTS</span></span>

### <span data-ttu-id="48d45-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="48d45-120">None</span></span>

## <span data-ttu-id="48d45-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48d45-121">OUTPUTS</span></span>

### <span data-ttu-id="48d45-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="48d45-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="48d45-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48d45-123">NOTES</span></span>
<span data-ttu-id="48d45-124">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="48d45-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="48d45-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48d45-125">RELATED LINKS</span></span>
