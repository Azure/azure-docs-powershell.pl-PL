---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889253"
---
# <span data-ttu-id="12813-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="12813-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="12813-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12813-102">SYNOPSIS</span></span>
<span data-ttu-id="12813-103">Pobierz metryki planu.</span><span class="sxs-lookup"><span data-stu-id="12813-103">Get the plan metrics.</span></span>

## <span data-ttu-id="12813-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12813-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="12813-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12813-105">DESCRIPTION</span></span>
<span data-ttu-id="12813-106">Pobierz metryki planu.</span><span class="sxs-lookup"><span data-stu-id="12813-106">Get the plan metrics.</span></span>

## <span data-ttu-id="12813-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12813-107">EXAMPLES</span></span>

### <span data-ttu-id="12813-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12813-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="12813-109">Uzyskaj metryki planu.</span><span class="sxs-lookup"><span data-stu-id="12813-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="12813-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12813-110">PARAMETERS</span></span>

### <span data-ttu-id="12813-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="12813-111">-PlanName</span></span>
<span data-ttu-id="12813-112">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="12813-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12813-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12813-113">-ResourceGroupName</span></span>
<span data-ttu-id="12813-114">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="12813-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12813-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12813-115">CommonParameters</span></span>
<span data-ttu-id="12813-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12813-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12813-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12813-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12813-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12813-118">INPUTS</span></span>

## <span data-ttu-id="12813-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12813-119">OUTPUTS</span></span>

### <span data-ttu-id="12813-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="12813-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="12813-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12813-121">NOTES</span></span>

## <span data-ttu-id="12813-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12813-122">RELATED LINKS</span></span>

