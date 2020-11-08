---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055963"
---
# <span data-ttu-id="e10bb-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="e10bb-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="e10bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e10bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e10bb-103">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="e10bb-103">Get the offer metrics.</span></span>

## <span data-ttu-id="e10bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e10bb-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e10bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e10bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e10bb-106">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="e10bb-106">Get the offer metrics.</span></span>

## <span data-ttu-id="e10bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e10bb-107">EXAMPLES</span></span>

### <span data-ttu-id="e10bb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e10bb-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="e10bb-109">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="e10bb-109">Get the offer metrics.</span></span>

## <span data-ttu-id="e10bb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e10bb-110">PARAMETERS</span></span>

### <span data-ttu-id="e10bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10bb-111">-DefaultProfile</span></span>
<span data-ttu-id="e10bb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e10bb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10bb-113">-Offername</span><span class="sxs-lookup"><span data-stu-id="e10bb-113">-OfferName</span></span>
<span data-ttu-id="e10bb-114">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="e10bb-114">Name of an offer.</span></span>

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

### <span data-ttu-id="e10bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="e10bb-116">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="e10bb-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e10bb-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e10bb-117">-SubscriptionId</span></span>
<span data-ttu-id="e10bb-118">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e10bb-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e10bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10bb-119">CommonParameters</span></span>
<span data-ttu-id="e10bb-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10bb-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e10bb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10bb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e10bb-122">INPUTS</span></span>

## <span data-ttu-id="e10bb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e10bb-123">OUTPUTS</span></span>

### <span data-ttu-id="e10bb-124">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="e10bb-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="e10bb-125">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e10bb-125">ALIASES</span></span>

## <span data-ttu-id="e10bb-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e10bb-126">NOTES</span></span>

## <span data-ttu-id="e10bb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e10bb-127">RELATED LINKS</span></span>

