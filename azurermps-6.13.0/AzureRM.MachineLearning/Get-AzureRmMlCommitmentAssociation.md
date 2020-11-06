---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 5535ccb243b6c49d95f06c8cd13cf95bab52abe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546532"
---
# <span data-ttu-id="7a94e-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="7a94e-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="7a94e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a94e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a94e-103">Pobiera informacje podsumowujące dla jednego lub większej liczby skojarzeń zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="7a94e-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a94e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a94e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a94e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a94e-105">DESCRIPTION</span></span>
<span data-ttu-id="7a94e-106">Pobiera informacje o stowarzyszeniu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="7a94e-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="7a94e-107">W zależności od przekazanego paramenters polecenie cmdlet zwraca określone powiązanie zobowiązań lub kolekcję skojarzeń zobowiązań dla określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="7a94e-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="7a94e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a94e-108">EXAMPLES</span></span>

### <span data-ttu-id="7a94e-109">Przykład 1: uzyskiwanie określonego stowarzyszenia zobowiązań</span><span class="sxs-lookup"><span data-stu-id="7a94e-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="7a94e-110">Przykład 2: uzyskiwanie wszystkich skojarzeń zobowiązań dla określonego planu zobowiązań</span><span class="sxs-lookup"><span data-stu-id="7a94e-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="7a94e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a94e-111">PARAMETERS</span></span>

### <span data-ttu-id="7a94e-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="7a94e-112">-CommitmentPlanName</span></span>
<span data-ttu-id="7a94e-113">Nazwa planu zobowiązań usługi Azure ML, który ma jedno lub więcej skojarzeń zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="7a94e-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="7a94e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a94e-114">-DefaultProfile</span></span>
<span data-ttu-id="7a94e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7a94e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a94e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a94e-116">-Name</span></span>
<span data-ttu-id="7a94e-117">Nazwa zrzeszenia zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7a94e-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7a94e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a94e-118">-ResourceGroupName</span></span>
<span data-ttu-id="7a94e-119">Nazwa grupy zasobów dla stowarzyszenia zobowiązanie na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7a94e-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7a94e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a94e-120">CommonParameters</span></span>
<span data-ttu-id="7a94e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a94e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a94e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a94e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a94e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a94e-123">INPUTS</span></span>

### <span data-ttu-id="7a94e-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7a94e-124">None</span></span>

## <span data-ttu-id="7a94e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a94e-125">OUTPUTS</span></span>

### <span data-ttu-id="7a94e-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7a94e-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7a94e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a94e-127">NOTES</span></span>
<span data-ttu-id="7a94e-128">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="7a94e-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7a94e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a94e-129">RELATED LINKS</span></span>
