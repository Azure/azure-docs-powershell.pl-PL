---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 5404cf82308c63a5ba6fe07ef4ac01101f44c48c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718914"
---
# <span data-ttu-id="e8dd9-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e8dd9-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="e8dd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="e8dd9-103">Pobiera informacje podsumowujące dla co najmniej jednego planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8dd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8dd9-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8dd9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="e8dd9-106">Pobiera informacje dotyczące planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="e8dd9-107">W zależności od przekazanego paramenters polecenie cmdlet zwraca określony plan zobowiązań, kolekcję planów zobowiązań dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję planów zobowiązań w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="e8dd9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8dd9-108">EXAMPLES</span></span>

### <span data-ttu-id="e8dd9-109">--------------------------Przykład 1: uzyskiwanie określonego planu zobowiązań--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8dd9-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="e8dd9-110">--------------------------Przykład 2: pobieranie wszystkich zasobów planu zobowiązań w bieżącej subskrypcji--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8dd9-110">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="e8dd9-111">--------------------------Przykład 3: Pobierz wszystkie plany zobowiązań w bieżącym abonamentu i danej grupie zasobów--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8dd9-111">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="e8dd9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8dd9-112">PARAMETERS</span></span>

### <span data-ttu-id="e8dd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8dd9-113">-DefaultProfile</span></span>
<span data-ttu-id="e8dd9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e8dd9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8dd9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8dd9-115">-Name</span></span>
<span data-ttu-id="e8dd9-116">Nazwa planu zobowiązań.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-116">The name of the commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8dd9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8dd9-118">Nazwa grupy zasobów dla planu zobowiązań w usłudze Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8dd9-119">CommonParameters</span></span>
<span data-ttu-id="e8dd9-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8dd9-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8dd9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8dd9-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8dd9-122">INPUTS</span></span>

### <span data-ttu-id="e8dd9-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8dd9-123">None</span></span>
<span data-ttu-id="e8dd9-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e8dd9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8dd9-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8dd9-125">OUTPUTS</span></span>

### <span data-ttu-id="e8dd9-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e8dd9-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="e8dd9-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. MODELES. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="e8dd9-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="e8dd9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8dd9-128">NOTES</span></span>
<span data-ttu-id="e8dd9-129">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="e8dd9-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e8dd9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8dd9-130">RELATED LINKS</span></span>

