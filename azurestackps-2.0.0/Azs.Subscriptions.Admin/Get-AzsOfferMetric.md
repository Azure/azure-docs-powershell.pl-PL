---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054083"
---
# <span data-ttu-id="ffc1d-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="ffc1d-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="ffc1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc1d-103">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-103">Get the offer metrics.</span></span>

## <span data-ttu-id="ffc1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffc1d-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ffc1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffc1d-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc1d-106">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-106">Get the offer metrics.</span></span>

## <span data-ttu-id="ffc1d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffc1d-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc1d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffc1d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="ffc1d-109">Pobierz metryki oferty.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-109">Get the offer metrics.</span></span>

## <span data-ttu-id="ffc1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffc1d-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc1d-111">-DefaultProfile</span></span>
<span data-ttu-id="ffc1d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc1d-113">-Offername</span><span class="sxs-lookup"><span data-stu-id="ffc1d-113">-OfferName</span></span>
<span data-ttu-id="ffc1d-114">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-114">Name of an offer.</span></span>

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

### <span data-ttu-id="ffc1d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc1d-115">-ResourceGroupName</span></span>
<span data-ttu-id="ffc1d-116">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ffc1d-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ffc1d-117">-SubscriptionId</span></span>
<span data-ttu-id="ffc1d-118">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ffc1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc1d-119">CommonParameters</span></span>
<span data-ttu-id="ffc1d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc1d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffc1d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc1d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffc1d-122">INPUTS</span></span>

## <span data-ttu-id="ffc1d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffc1d-123">OUTPUTS</span></span>

### <span data-ttu-id="ffc1d-124">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="ffc1d-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="ffc1d-125">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ffc1d-125">ALIASES</span></span>

## <span data-ttu-id="ffc1d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffc1d-126">NOTES</span></span>

## <span data-ttu-id="ffc1d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffc1d-127">RELATED LINKS</span></span>

