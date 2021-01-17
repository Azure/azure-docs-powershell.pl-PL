---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380079"
---
# <span data-ttu-id="6ff2a-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6ff2a-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="6ff2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ff2a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff2a-103">Pobiera konfigurację sondy dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="6ff2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ff2a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff2a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ff2a-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff2a-106">Polecenie cmdlet **Get-AzLoadBalancerProbeConfig** umożliwia pobranie co najmniej jednej konfiguracji sondy modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="6ff2a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ff2a-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff2a-108">Przykład 1: Uzyskiwanie konfiguracji sondy modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="6ff2a-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="6ff2a-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6ff2a-110">Drugie polecenie pobiera skojarzoną konfigurację sondy o nazwie Moja Sonda z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="6ff2a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ff2a-111">PARAMETERS</span></span>

### <span data-ttu-id="6ff2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff2a-112">-DefaultProfile</span></span>
<span data-ttu-id="6ff2a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff2a-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="6ff2a-114">-LoadBalancer</span></span>
<span data-ttu-id="6ff2a-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją sondy do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="6ff2a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ff2a-116">-Name</span></span>
<span data-ttu-id="6ff2a-117">Określa nazwę konfiguracji sondy, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="6ff2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff2a-118">CommonParameters</span></span>
<span data-ttu-id="6ff2a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff2a-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ff2a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff2a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ff2a-121">INPUTS</span></span>

### <span data-ttu-id="6ff2a-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ff2a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6ff2a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ff2a-123">OUTPUTS</span></span>

### <span data-ttu-id="6ff2a-124">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="6ff2a-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="6ff2a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ff2a-125">NOTES</span></span>

## <span data-ttu-id="6ff2a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ff2a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6ff2a-127">Dodaj-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6ff2a-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="6ff2a-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ff2a-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6ff2a-129">Nowe — AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6ff2a-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="6ff2a-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6ff2a-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="6ff2a-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6ff2a-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


