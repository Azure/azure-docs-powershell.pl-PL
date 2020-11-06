---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554082"
---
# <span data-ttu-id="33d40-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="33d40-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="33d40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33d40-102">SYNOPSIS</span></span>
<span data-ttu-id="33d40-103">Pobiera informacje o historii użycia określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="33d40-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33d40-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33d40-105">DESCRIPTION</span></span>
<span data-ttu-id="33d40-106">Pobiera informacje o historii użycia określonego planu zobowiązań, w tym zasobów używanych i zasobów pozostałych w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="33d40-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="33d40-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33d40-107">EXAMPLES</span></span>

### <span data-ttu-id="33d40-108">Przykład 1: uzyskiwanie historii użycia dla określonego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="33d40-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="33d40-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33d40-109">PARAMETERS</span></span>

### <span data-ttu-id="33d40-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d40-110">-DefaultProfile</span></span>
<span data-ttu-id="33d40-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="33d40-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33d40-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33d40-112">-Name</span></span>
<span data-ttu-id="33d40-113">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="33d40-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="33d40-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d40-114">-ResourceGroupName</span></span>
<span data-ttu-id="33d40-115">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="33d40-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="33d40-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d40-116">CommonParameters</span></span>
<span data-ttu-id="33d40-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d40-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d40-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d40-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d40-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33d40-119">INPUTS</span></span>

### <span data-ttu-id="33d40-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="33d40-120">None</span></span>

## <span data-ttu-id="33d40-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33d40-121">OUTPUTS</span></span>

### <span data-ttu-id="33d40-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="33d40-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="33d40-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33d40-123">NOTES</span></span>
<span data-ttu-id="33d40-124">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="33d40-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="33d40-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33d40-125">RELATED LINKS</span></span>
