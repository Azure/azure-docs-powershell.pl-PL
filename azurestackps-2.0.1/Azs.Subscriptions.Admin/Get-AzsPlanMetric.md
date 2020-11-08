---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054167"
---
# <span data-ttu-id="4ff6f-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="4ff6f-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="4ff6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ff6f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff6f-103">Uzyskiwanie metryk określonego planu.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="4ff6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ff6f-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4ff6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ff6f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff6f-106">Uzyskiwanie metryk określonego planu.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="4ff6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ff6f-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff6f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ff6f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="4ff6f-109">Uzyskaj metryki planu.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="4ff6f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ff6f-110">PARAMETERS</span></span>

### <span data-ttu-id="4ff6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff6f-111">-DefaultProfile</span></span>
<span data-ttu-id="4ff6f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ff6f-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4ff6f-113">-PlanName</span></span>
<span data-ttu-id="4ff6f-114">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-114">Name of the plan.</span></span>

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

### <span data-ttu-id="4ff6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ff6f-116">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4ff6f-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4ff6f-117">-SubscriptionId</span></span>
<span data-ttu-id="4ff6f-118">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ff6f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff6f-119">CommonParameters</span></span>
<span data-ttu-id="4ff6f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff6f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff6f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ff6f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff6f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ff6f-122">INPUTS</span></span>

## <span data-ttu-id="4ff6f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ff6f-123">OUTPUTS</span></span>

### <span data-ttu-id="4ff6f-124">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="4ff6f-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="4ff6f-125">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4ff6f-125">ALIASES</span></span>

## <span data-ttu-id="4ff6f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ff6f-126">NOTES</span></span>

## <span data-ttu-id="4ff6f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ff6f-127">RELATED LINKS</span></span>

