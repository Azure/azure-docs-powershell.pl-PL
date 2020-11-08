---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219546"
---
# <span data-ttu-id="b49e4-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b49e4-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b49e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b49e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b49e4-103">Pobiera konfigurację IP frontonu w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b49e4-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="b49e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b49e4-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b49e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b49e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b49e4-106">Polecenie cmdlet **Get-AzLoadBalancerFrontendIpConfig** Pobiera konfigurację adresu IP frontonu lub listy konfiguracji adresów IP frontonu w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b49e4-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="b49e4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b49e4-107">EXAMPLES</span></span>

### <span data-ttu-id="b49e4-108">Przykład 1: Uzyskiwanie konfiguracji frontonu IP w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b49e4-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="b49e4-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="b49e4-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b49e4-110">Drugie polecenie pobiera konfigurację IP front-end skojarzoną z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b49e4-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="b49e4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b49e4-111">PARAMETERS</span></span>

### <span data-ttu-id="b49e4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49e4-112">-DefaultProfile</span></span>
<span data-ttu-id="b49e4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b49e4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b49e4-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b49e4-114">-LoadBalancer</span></span>
<span data-ttu-id="b49e4-115">Umożliwia określenie modułu równoważenia obciążenia skojarzonego z konfiguracją IP frontonu w celu uzyskania.</span><span class="sxs-lookup"><span data-stu-id="b49e4-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="b49e4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b49e4-116">-Name</span></span>
<span data-ttu-id="b49e4-117">Określa nazwę modułu równoważenia obciążenia zawierającego konfigurację frontonu IP do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b49e4-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="b49e4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49e4-118">CommonParameters</span></span>
<span data-ttu-id="b49e4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49e4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49e4-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b49e4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49e4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b49e4-121">INPUTS</span></span>

### <span data-ttu-id="b49e4-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b49e4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b49e4-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b49e4-123">OUTPUTS</span></span>

### <span data-ttu-id="b49e4-124">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b49e4-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b49e4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b49e4-125">NOTES</span></span>

## <span data-ttu-id="b49e4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b49e4-126">RELATED LINKS</span></span>

[<span data-ttu-id="b49e4-127">Dodaj-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b49e4-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b49e4-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b49e4-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b49e4-129">Nowe — AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b49e4-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b49e4-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b49e4-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b49e4-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b49e4-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


