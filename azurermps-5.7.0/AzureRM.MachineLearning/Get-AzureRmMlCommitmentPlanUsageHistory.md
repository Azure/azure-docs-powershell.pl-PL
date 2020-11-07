---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93719679"
---
# <span data-ttu-id="e6456-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="e6456-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="e6456-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6456-102">SYNOPSIS</span></span>
<span data-ttu-id="e6456-103">Pobiera informacje o historii użycia określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="e6456-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6456-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6456-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6456-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6456-105">DESCRIPTION</span></span>
<span data-ttu-id="e6456-106">Pobiera informacje o historii użycia określonego planu zobowiązań, w tym zasobów używanych i zasobów pozostałych w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="e6456-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="e6456-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6456-107">EXAMPLES</span></span>

### <span data-ttu-id="e6456-108">--------------------------Przykład 1: Uzyskaj historię użycia dla określonego planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6456-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="e6456-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6456-109">PARAMETERS</span></span>

### <span data-ttu-id="e6456-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6456-110">-DefaultProfile</span></span>
<span data-ttu-id="e6456-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e6456-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6456-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6456-112">-Name</span></span>
<span data-ttu-id="e6456-113">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e6456-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6456-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6456-114">-ResourceGroupName</span></span>
<span data-ttu-id="e6456-115">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e6456-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6456-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6456-116">CommonParameters</span></span>
<span data-ttu-id="e6456-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6456-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6456-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6456-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6456-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6456-119">INPUTS</span></span>

### <span data-ttu-id="e6456-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e6456-120">None</span></span>
<span data-ttu-id="e6456-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e6456-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6456-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6456-122">OUTPUTS</span></span>

### <span data-ttu-id="e6456-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="e6456-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="e6456-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6456-124">NOTES</span></span>
<span data-ttu-id="e6456-125">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="e6456-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e6456-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6456-126">RELATED LINKS</span></span>

