---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523650"
---
# <span data-ttu-id="f3bdd-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="f3bdd-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="f3bdd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bdd-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-103">Create or update a quota.</span></span>

## <span data-ttu-id="f3bdd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3bdd-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3bdd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="f3bdd-106">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-106">Create or update a quota.</span></span>

## <span data-ttu-id="f3bdd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="f3bdd-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3bdd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="f3bdd-109">Utwórz nowy przydział sieci z wartościami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="f3bdd-110">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3bdd-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="f3bdd-111">Utwórz nowy przydział sieci z wartościami niedomyślnymi przydziału.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="f3bdd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3bdd-112">PARAMETERS</span></span>

### <span data-ttu-id="f3bdd-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f3bdd-113">-Location</span></span>
<span data-ttu-id="f3bdd-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-115">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-115">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="f3bdd-116">Maksymalna liczba modułów równoważenia obciążenia dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-116">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-117">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-117">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="f3bdd-118">Maksymalna dozwolona liczba kart sieciowych przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-118">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-119">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-119">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="f3bdd-120">Maksymalna dozwolona liczba publicznych adresów IP przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-120">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-121">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-121">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="f3bdd-122">Maksymalna liczba grup zabezpieczeń dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-122">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="f3bdd-124">Maksymalna liczba połączeń bramy sieci wirtualnej dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-124">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-125">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-125">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="f3bdd-126">Maksymalna liczba dozwolonych bram sieci wirtualnej na subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-126">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-127">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="f3bdd-127">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="f3bdd-128">Maxium liczba sieci wirtualnych dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-128">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-129">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="f3bdd-129">-MigrationPhase</span></span>
<span data-ttu-id="f3bdd-130">Przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-130">Deprecated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3bdd-131">-Name</span></span>
<span data-ttu-id="f3bdd-132">Nazwa zasobu przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-132">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdd-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3bdd-133">-Confirm</span></span>
<span data-ttu-id="f3bdd-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3bdd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3bdd-135">-WhatIf</span></span>
<span data-ttu-id="f3bdd-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3bdd-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3bdd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bdd-138">CommonParameters</span></span>
<span data-ttu-id="f3bdd-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3bdd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bdd-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3bdd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bdd-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3bdd-141">INPUTS</span></span>

## <span data-ttu-id="f3bdd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3bdd-142">OUTPUTS</span></span>

### <span data-ttu-id="f3bdd-143">Microsoft. AzureStack. Management. Network. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="f3bdd-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="f3bdd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3bdd-144">NOTES</span></span>

## <span data-ttu-id="f3bdd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3bdd-145">RELATED LINKS</span></span>

