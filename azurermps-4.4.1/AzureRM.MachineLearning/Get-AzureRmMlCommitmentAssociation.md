---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549164"
---
# <span data-ttu-id="a6c77-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="a6c77-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="a6c77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6c77-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c77-103">Pobiera informacje podsumowujące dla jednego lub większej liczby skojarzeń zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a6c77-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6c77-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6c77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6c77-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c77-106">Pobiera informacje o stowarzyszeniu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a6c77-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="a6c77-107">W zależności od przekazanego paramenters polecenie cmdlet zwraca określone powiązanie zobowiązań lub kolekcję skojarzeń zobowiązań dla określonego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a6c77-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="a6c77-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6c77-108">EXAMPLES</span></span>

### <span data-ttu-id="a6c77-109">--------------------------Przykład 1: uzyskiwanie określonego stowarzyszenia zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6c77-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="a6c77-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a6c77-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="a6c77-111">--------------------------Przykład 2: pobieranie wszystkich skojarzeń zobowiązań dla określonego planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6c77-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="a6c77-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a6c77-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="a6c77-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6c77-113">PARAMETERS</span></span>

### <span data-ttu-id="a6c77-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="a6c77-114">-CommitmentPlanName</span></span>
<span data-ttu-id="a6c77-115">Nazwa planu zobowiązań usługi Azure ML, który ma jedno lub więcej skojarzeń zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="a6c77-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="a6c77-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6c77-116">-Name</span></span>
<span data-ttu-id="a6c77-117">Nazwa zrzeszenia zobowiązań na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a6c77-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="a6c77-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c77-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6c77-119">Nazwa grupy zasobów dla stowarzyszenia zobowiązanie na platformie Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a6c77-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="a6c77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c77-120">-DefaultProfile</span></span>
<span data-ttu-id="a6c77-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c77-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6c77-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c77-122">CommonParameters</span></span>
<span data-ttu-id="a6c77-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c77-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c77-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c77-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c77-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6c77-125">INPUTS</span></span>

## <span data-ttu-id="a6c77-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6c77-126">OUTPUTS</span></span>

### <span data-ttu-id="a6c77-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a6c77-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="a6c77-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="a6c77-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="a6c77-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6c77-129">NOTES</span></span>
<span data-ttu-id="a6c77-130">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="a6c77-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a6c77-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6c77-131">RELATED LINKS</span></span>

