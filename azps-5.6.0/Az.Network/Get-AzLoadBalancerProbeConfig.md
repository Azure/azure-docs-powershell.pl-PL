---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 43c3b4d17d024eaae06c7d7f891dfd2ea3e08aa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006458"
---
# <span data-ttu-id="fcfba-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fcfba-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="fcfba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcfba-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfba-103">Pobiera konfigurację konfiguracji konfiguracji dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fcfba-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="fcfba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcfba-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcfba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcfba-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfba-106">Polecenie **cmdlet Get-AzLoadBalancerProbeConfig** pobiera jedną lub więcej konfiguracji konfiguracji dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fcfba-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="fcfba-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcfba-107">EXAMPLES</span></span>

### <span data-ttu-id="fcfba-108">Przykład 1. Uzyskiwanie konfiguracji równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fcfba-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="fcfba-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="fcfba-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="fcfba-110">Drugie polecenie pobiera skojarzoną konfigurację o nazwie MyProbe z równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="fcfba-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="fcfba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcfba-111">PARAMETERS</span></span>

### <span data-ttu-id="fcfba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfba-112">-DefaultProfile</span></span>
<span data-ttu-id="fcfba-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcfba-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcfba-114">-LoadBalancer</span></span>
<span data-ttu-id="fcfba-115">Określa, który równoważenie obciążenia jest skojarzone z konfiguracją konfiguracji ładowania.</span><span class="sxs-lookup"><span data-stu-id="fcfba-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="fcfba-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fcfba-116">-Name</span></span>
<span data-ttu-id="fcfba-117">Określa nazwę konfiguracji konfiguracji, która ma być uzyskają.</span><span class="sxs-lookup"><span data-stu-id="fcfba-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="fcfba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfba-118">CommonParameters</span></span>
<span data-ttu-id="fcfba-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfba-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcfba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfba-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcfba-121">INPUTS</span></span>

### <span data-ttu-id="fcfba-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcfba-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fcfba-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcfba-123">OUTPUTS</span></span>

### <span data-ttu-id="fcfba-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="fcfba-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="fcfba-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcfba-125">NOTES</span></span>

## <span data-ttu-id="fcfba-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcfba-126">RELATED LINKS</span></span>

[<span data-ttu-id="fcfba-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fcfba-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="fcfba-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcfba-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="fcfba-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fcfba-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="fcfba-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fcfba-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="fcfba-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fcfba-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


