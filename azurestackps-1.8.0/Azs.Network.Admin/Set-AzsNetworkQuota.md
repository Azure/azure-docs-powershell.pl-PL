---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889293"
---
# <span data-ttu-id="98f52-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="98f52-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="98f52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98f52-102">SYNOPSIS</span></span>
<span data-ttu-id="98f52-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="98f52-103">Create or update a quota.</span></span>

## <span data-ttu-id="98f52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98f52-104">SYNTAX</span></span>

### <span data-ttu-id="98f52-105">Przydziały (domyślne)</span><span class="sxs-lookup"><span data-stu-id="98f52-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f52-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="98f52-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f52-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="98f52-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f52-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98f52-108">DESCRIPTION</span></span>
<span data-ttu-id="98f52-109">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="98f52-109">Create or update a quota.</span></span>

## <span data-ttu-id="98f52-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98f52-110">EXAMPLES</span></span>

### <span data-ttu-id="98f52-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="98f52-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="98f52-112">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="98f52-112">Update a network quota by name.</span></span>

### <span data-ttu-id="98f52-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="98f52-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="98f52-114">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="98f52-114">Update a network quota by name.</span></span>

## <span data-ttu-id="98f52-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98f52-115">PARAMETERS</span></span>

### <span data-ttu-id="98f52-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98f52-116">-Name</span></span>
<span data-ttu-id="98f52-117">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="98f52-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="98f52-119">Maksymalna dozwolona liczba kart sieciowych przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="98f52-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="98f52-121">Maksymalna dozwolona liczba publicznych adresów IP przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="98f52-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="98f52-123">Maksymalna liczba połączeń bramy sieci wirtualnej dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="98f52-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="98f52-125">Maxium liczba sieci wirtualnych dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="98f52-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="98f52-127">Maksymalna liczba dozwolonych bram sieci wirtualnej na subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="98f52-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="98f52-129">Maksymalna liczba grup zabezpieczeń dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="98f52-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="98f52-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="98f52-131">Maksymalna liczba modułów równoważenia obciążenia dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="98f52-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98f52-132">-Location</span></span>
<span data-ttu-id="98f52-133">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="98f52-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f52-134">-ResourceId</span></span>
<span data-ttu-id="98f52-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="98f52-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98f52-136">-InputObject</span></span>
<span data-ttu-id="98f52-137">Posbbily zmodyfikowano przydział sieciowy zwrócony przez Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="98f52-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f52-138">-WhatIf</span></span>
<span data-ttu-id="98f52-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f52-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f52-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98f52-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98f52-141">-Confirm</span></span>
<span data-ttu-id="98f52-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f52-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f52-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f52-143">CommonParameters</span></span>
<span data-ttu-id="98f52-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f52-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f52-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f52-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f52-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98f52-146">INPUTS</span></span>

## <span data-ttu-id="98f52-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98f52-147">OUTPUTS</span></span>

### <span data-ttu-id="98f52-148">Microsoft. AzureStack. Management. Network. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="98f52-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="98f52-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98f52-149">NOTES</span></span>

## <span data-ttu-id="98f52-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98f52-150">RELATED LINKS</span></span>
