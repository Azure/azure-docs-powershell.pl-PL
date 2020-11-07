---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888685"
---
# <span data-ttu-id="08941-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="08941-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="08941-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08941-102">SYNOPSIS</span></span>
<span data-ttu-id="08941-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="08941-103">Create or update a quota.</span></span>

## <span data-ttu-id="08941-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08941-104">SYNTAX</span></span>

### <span data-ttu-id="08941-105">Przydziały (domyślne)</span><span class="sxs-lookup"><span data-stu-id="08941-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08941-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="08941-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08941-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="08941-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08941-108">Opis</span><span class="sxs-lookup"><span data-stu-id="08941-108">DESCRIPTION</span></span>
<span data-ttu-id="08941-109">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="08941-109">Create or update a quota.</span></span>

## <span data-ttu-id="08941-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08941-110">EXAMPLES</span></span>

### <span data-ttu-id="08941-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="08941-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="08941-112">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="08941-112">Update a network quota by name.</span></span>

### <span data-ttu-id="08941-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="08941-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="08941-114">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="08941-114">Update a network quota by name.</span></span>

## <span data-ttu-id="08941-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08941-115">PARAMETERS</span></span>

### <span data-ttu-id="08941-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08941-116">-InputObject</span></span>
<span data-ttu-id="08941-117">Posbbily zmodyfikowano przydział sieciowy zwrócony przez Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="08941-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="08941-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="08941-118">-Location</span></span>
<span data-ttu-id="08941-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="08941-119">Location of the resource.</span></span>

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

### <span data-ttu-id="08941-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="08941-121">Maksymalna liczba modułów równoważenia obciążenia dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="08941-121">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="08941-123">Maksymalna dozwolona liczba kart sieciowych przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="08941-123">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-124">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="08941-125">Maksymalna dozwolona liczba publicznych adresów IP przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="08941-125">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="08941-127">Maksymalna liczba grup zabezpieczeń dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="08941-127">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="08941-129">Maksymalna liczba połączeń bramy sieci wirtualnej dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="08941-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="08941-131">Maksymalna liczba dozwolonych bram sieci wirtualnej na subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="08941-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="08941-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="08941-133">Maxium liczba sieci wirtualnych dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="08941-133">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="08941-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08941-134">-Name</span></span>
<span data-ttu-id="08941-135">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="08941-135">Name of the resource.</span></span>

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

### <span data-ttu-id="08941-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08941-136">-ResourceId</span></span>
<span data-ttu-id="08941-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="08941-137">The resource id.</span></span>

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

### <span data-ttu-id="08941-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08941-138">-Confirm</span></span>
<span data-ttu-id="08941-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08941-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08941-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08941-140">-WhatIf</span></span>
<span data-ttu-id="08941-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08941-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08941-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08941-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08941-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08941-143">CommonParameters</span></span>
<span data-ttu-id="08941-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08941-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08941-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08941-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08941-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08941-146">INPUTS</span></span>

## <span data-ttu-id="08941-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08941-147">OUTPUTS</span></span>

### <span data-ttu-id="08941-148">Microsoft. AzureStack. Management. Network. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="08941-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="08941-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08941-149">NOTES</span></span>

## <span data-ttu-id="08941-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08941-150">RELATED LINKS</span></span>

