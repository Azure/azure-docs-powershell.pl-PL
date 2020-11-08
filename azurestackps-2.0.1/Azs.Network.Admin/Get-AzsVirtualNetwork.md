---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054229"
---
# <span data-ttu-id="650ff-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="650ff-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="650ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="650ff-102">SYNOPSIS</span></span>
<span data-ttu-id="650ff-103">Zapoznaj się z listą wszystkich sieci wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="650ff-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="650ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="650ff-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="650ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="650ff-105">DESCRIPTION</span></span>
<span data-ttu-id="650ff-106">Zapoznaj się z listą wszystkich sieci wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="650ff-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="650ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="650ff-107">EXAMPLES</span></span>

### <span data-ttu-id="650ff-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="650ff-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="650ff-109">Zwraca listę sieci wirtualnych z sygnaturą stosową platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="650ff-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="650ff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="650ff-110">PARAMETERS</span></span>

### <span data-ttu-id="650ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650ff-111">-DefaultProfile</span></span>
<span data-ttu-id="650ff-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="650ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="650ff-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="650ff-113">-Filter</span></span>
<span data-ttu-id="650ff-114">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="650ff-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="650ff-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="650ff-115">-InlineCount</span></span>
<span data-ttu-id="650ff-116">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="650ff-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="650ff-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="650ff-117">-OrderBy</span></span>
<span data-ttu-id="650ff-118">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="650ff-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="650ff-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="650ff-119">-Skip</span></span>
<span data-ttu-id="650ff-120">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="650ff-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="650ff-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="650ff-121">-SubscriptionId</span></span>
<span data-ttu-id="650ff-122">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="650ff-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="650ff-123">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="650ff-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="650ff-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="650ff-124">-Top</span></span>
<span data-ttu-id="650ff-125">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="650ff-125">OData top parameter.</span></span>

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

### <span data-ttu-id="650ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650ff-126">CommonParameters</span></span>
<span data-ttu-id="650ff-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650ff-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="650ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650ff-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650ff-129">INPUTS</span></span>

## <span data-ttu-id="650ff-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="650ff-130">OUTPUTS</span></span>

### <span data-ttu-id="650ff-131">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="650ff-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="650ff-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="650ff-132">NOTES</span></span>

## <span data-ttu-id="650ff-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="650ff-133">RELATED LINKS</span></span>

