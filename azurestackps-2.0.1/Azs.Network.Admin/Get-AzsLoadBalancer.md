---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054181"
---
# <span data-ttu-id="5f562-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f562-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="5f562-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f562-102">SYNOPSIS</span></span>
<span data-ttu-id="5f562-103">Zapoznaj się z listą wszystkich modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5f562-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="5f562-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f562-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5f562-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f562-105">DESCRIPTION</span></span>
<span data-ttu-id="5f562-106">Zapoznaj się z listą wszystkich modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5f562-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="5f562-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f562-107">EXAMPLES</span></span>

### <span data-ttu-id="5f562-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f562-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="5f562-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f562-109">PARAMETERS</span></span>

### <span data-ttu-id="5f562-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f562-110">-DefaultProfile</span></span>
<span data-ttu-id="5f562-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f562-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f562-112">-Filter</span><span class="sxs-lookup"><span data-stu-id="5f562-112">-Filter</span></span>
<span data-ttu-id="5f562-113">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="5f562-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="5f562-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="5f562-114">-InlineCount</span></span>
<span data-ttu-id="5f562-115">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="5f562-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="5f562-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5f562-116">-OrderBy</span></span>
<span data-ttu-id="5f562-117">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="5f562-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="5f562-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="5f562-118">-Skip</span></span>
<span data-ttu-id="5f562-119">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="5f562-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="5f562-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5f562-120">-SubscriptionId</span></span>
<span data-ttu-id="5f562-121">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5f562-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5f562-122">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5f562-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5f562-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="5f562-123">-Top</span></span>
<span data-ttu-id="5f562-124">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="5f562-124">OData top parameter.</span></span>

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

### <span data-ttu-id="5f562-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f562-125">CommonParameters</span></span>
<span data-ttu-id="5f562-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f562-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f562-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f562-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f562-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f562-128">INPUTS</span></span>

## <span data-ttu-id="5f562-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f562-129">OUTPUTS</span></span>

### <span data-ttu-id="5f562-130">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f562-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="5f562-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f562-131">NOTES</span></span>

## <span data-ttu-id="5f562-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f562-132">RELATED LINKS</span></span>

