---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719295"
---
# <span data-ttu-id="e3752-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="e3752-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="e3752-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3752-102">SYNOPSIS</span></span>
<span data-ttu-id="e3752-103">Pobiera informacje o historii użycia określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="e3752-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3752-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3752-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3752-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3752-105">DESCRIPTION</span></span>
<span data-ttu-id="e3752-106">Pobiera informacje o historii użycia określonego planu zobowiązań, w tym zasobów używanych i zasobów pozostałych w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="e3752-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="e3752-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3752-107">EXAMPLES</span></span>

### <span data-ttu-id="e3752-108">--------------------------Przykład 1: Uzyskaj historię użycia dla określonego planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3752-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="e3752-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e3752-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="e3752-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3752-110">PARAMETERS</span></span>

### <span data-ttu-id="e3752-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3752-111">-Name</span></span>
<span data-ttu-id="e3752-112">Nazwa planu zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e3752-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e3752-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3752-113">-ResourceGroupName</span></span>
<span data-ttu-id="e3752-114">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e3752-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e3752-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3752-115">-DefaultProfile</span></span>
<span data-ttu-id="e3752-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3752-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3752-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3752-117">CommonParameters</span></span>
<span data-ttu-id="e3752-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3752-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3752-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3752-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3752-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3752-120">INPUTS</span></span>

## <span data-ttu-id="e3752-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3752-121">OUTPUTS</span></span>

### <span data-ttu-id="e3752-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="e3752-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="e3752-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3752-123">NOTES</span></span>
<span data-ttu-id="e3752-124">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="e3752-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e3752-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3752-125">RELATED LINKS</span></span>

