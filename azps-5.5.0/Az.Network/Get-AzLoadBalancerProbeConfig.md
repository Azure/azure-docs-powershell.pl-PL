---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193835"
---
# <span data-ttu-id="a1fad-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1fad-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a1fad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1fad-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fad-103">Pobiera konfigurację konfiguracji konfiguracji dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a1fad-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="a1fad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1fad-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1fad-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1fad-105">DESCRIPTION</span></span>
<span data-ttu-id="a1fad-106">Polecenie **cmdlet Get-AzLoadBalancerProbeConfig** pobiera jedną lub więcej konfiguracji konfiguracji dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a1fad-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="a1fad-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1fad-107">EXAMPLES</span></span>

### <span data-ttu-id="a1fad-108">Przykład 1. Uzyskiwanie konfiguracji równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a1fad-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="a1fad-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="a1fad-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="a1fad-110">Drugie polecenie pobiera skojarzoną konfigurację o nazwie MyProbe z równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="a1fad-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="a1fad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1fad-111">PARAMETERS</span></span>

### <span data-ttu-id="a1fad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fad-112">-DefaultProfile</span></span>
<span data-ttu-id="a1fad-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1fad-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1fad-114">-LoadBalancer</span></span>
<span data-ttu-id="a1fad-115">Określa, który równoważenie obciążenia jest skojarzone z konfiguracją ładowania.</span><span class="sxs-lookup"><span data-stu-id="a1fad-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="a1fad-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1fad-116">-Name</span></span>
<span data-ttu-id="a1fad-117">Określa nazwę konfiguracji konfiguracji, która ma być uzyskają.</span><span class="sxs-lookup"><span data-stu-id="a1fad-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="a1fad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fad-118">CommonParameters</span></span>
<span data-ttu-id="a1fad-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fad-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1fad-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fad-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1fad-121">INPUTS</span></span>

### <span data-ttu-id="a1fad-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1fad-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1fad-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1fad-123">OUTPUTS</span></span>

### <span data-ttu-id="a1fad-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="a1fad-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="a1fad-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1fad-125">NOTES</span></span>

## <span data-ttu-id="a1fad-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1fad-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1fad-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1fad-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a1fad-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1fad-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a1fad-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1fad-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a1fad-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1fad-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a1fad-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1fad-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


