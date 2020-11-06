---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549163"
---
# <span data-ttu-id="56851-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="56851-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="56851-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56851-102">SYNOPSIS</span></span>
<span data-ttu-id="56851-103">Pobiera informacje podsumowujące dla co najmniej jednego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="56851-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56851-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56851-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56851-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56851-105">DESCRIPTION</span></span>
<span data-ttu-id="56851-106">Pobiera informacje dotyczące planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="56851-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="56851-107">W zależności od przekazanego paramenters polecenie cmdlet zwraca określony plan zobowiązań, kolekcję planów zobowiązań dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję planów zobowiązań w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56851-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="56851-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56851-108">EXAMPLES</span></span>

### <span data-ttu-id="56851-109">--------------------------Przykład 1: uzyskiwanie określonego planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="56851-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="56851-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="56851-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="56851-111">--------------------------Przykład 2: pobieranie wszystkich zasobów planu zobowiązań w bieżącej subskrypcji--------------------------</span><span class="sxs-lookup"><span data-stu-id="56851-111">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
<span data-ttu-id="56851-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="56851-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="56851-113">--------------------------Przykład 3: Pobierz wszystkie plany zobowiązań w bieżącym abonamentu i danej grupie zasobów--------------------------</span><span class="sxs-lookup"><span data-stu-id="56851-113">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="56851-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="56851-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="56851-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56851-115">PARAMETERS</span></span>

### <span data-ttu-id="56851-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56851-116">-Name</span></span>
<span data-ttu-id="56851-117">Nazwa planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="56851-117">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="56851-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56851-118">-ResourceGroupName</span></span>
<span data-ttu-id="56851-119">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="56851-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="56851-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56851-120">-DefaultProfile</span></span>
<span data-ttu-id="56851-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56851-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56851-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56851-122">CommonParameters</span></span>
<span data-ttu-id="56851-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56851-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56851-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56851-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56851-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56851-125">INPUTS</span></span>

## <span data-ttu-id="56851-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56851-126">OUTPUTS</span></span>

### <span data-ttu-id="56851-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="56851-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="56851-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="56851-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="56851-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56851-129">NOTES</span></span>
<span data-ttu-id="56851-130">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="56851-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="56851-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56851-131">RELATED LINKS</span></span>

