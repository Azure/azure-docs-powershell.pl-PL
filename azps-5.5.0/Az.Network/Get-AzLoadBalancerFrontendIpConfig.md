---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179875"
---
# <span data-ttu-id="ee310-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ee310-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ee310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee310-102">SYNOPSIS</span></span>
<span data-ttu-id="ee310-103">Pobiera konfigurację frontoronu IP w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ee310-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="ee310-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee310-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee310-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee310-105">DESCRIPTION</span></span>
<span data-ttu-id="ee310-106">Polecenie **cmdlet Get-AzLoadBalancerFrontendIpConfig** otrzymuje konfigurację frontoronu IP lub listę konfiguracji frontoronu IP w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ee310-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="ee310-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee310-107">EXAMPLES</span></span>

### <span data-ttu-id="ee310-108">Przykład 1. Uzyskiwanie konfiguracji frontoronu ip w ładowarce</span><span class="sxs-lookup"><span data-stu-id="ee310-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="ee310-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="ee310-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ee310-110">Drugie polecenie pobiera skojarzoną z tym równoważeniem obciążenia konfigurację frontonu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="ee310-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="ee310-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee310-111">PARAMETERS</span></span>

### <span data-ttu-id="ee310-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee310-112">-DefaultProfile</span></span>
<span data-ttu-id="ee310-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee310-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee310-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee310-114">-LoadBalancer</span></span>
<span data-ttu-id="ee310-115">Określa, jaka wartość ma być skojarzona z konfiguracją frontonu ip.</span><span class="sxs-lookup"><span data-stu-id="ee310-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee310-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ee310-116">-Name</span></span>
<span data-ttu-id="ee310-117">Określa nazwę urządzenia do równoważenia obciążenia, które zawiera konfigurację frontoronu IP do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="ee310-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="ee310-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee310-118">CommonParameters</span></span>
<span data-ttu-id="ee310-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee310-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee310-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee310-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee310-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee310-121">INPUTS</span></span>

### <span data-ttu-id="ee310-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee310-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ee310-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee310-123">OUTPUTS</span></span>

### <span data-ttu-id="ee310-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee310-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ee310-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee310-125">NOTES</span></span>

## <span data-ttu-id="ee310-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee310-126">RELATED LINKS</span></span>

[<span data-ttu-id="ee310-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ee310-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ee310-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ee310-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ee310-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ee310-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ee310-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ee310-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ee310-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ee310-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


