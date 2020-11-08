---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055781"
---
# <span data-ttu-id="1d66a-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="1d66a-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="1d66a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d66a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d66a-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="1d66a-103">Create or update a quota.</span></span>

## <span data-ttu-id="1d66a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d66a-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d66a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d66a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d66a-106">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="1d66a-106">Create or update a quota.</span></span>

## <span data-ttu-id="1d66a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d66a-107">EXAMPLES</span></span>

### <span data-ttu-id="1d66a-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="1d66a-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="1d66a-109">Utwórz nowy przydział sieci z wartościami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="1d66a-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="1d66a-110">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="1d66a-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="1d66a-111">Utwórz nowy przydział sieci z wartościami niedomyślnymi przydziału.</span><span class="sxs-lookup"><span data-stu-id="1d66a-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="1d66a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d66a-112">PARAMETERS</span></span>

### <span data-ttu-id="1d66a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d66a-113">-Name</span></span>
<span data-ttu-id="1d66a-114">Nazwa zasobu przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="1d66a-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="1d66a-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="1d66a-116">Maksymalna dozwolona liczba kart sieciowych przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="1d66a-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="1d66a-118">Maksymalna dozwolona liczba publicznych adresów IP przypadająca na jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="1d66a-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="1d66a-120">Maksymalna liczba połączeń bramy sieci wirtualnej dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="1d66a-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="1d66a-122">Maxium liczba sieci wirtualnych dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="1d66a-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="1d66a-124">Maksymalna liczba dozwolonych bram sieci wirtualnej na subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="1d66a-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="1d66a-126">Maksymalna liczba grup zabezpieczeń dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="1d66a-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="1d66a-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="1d66a-128">Maksymalna liczba modułów równoważenia obciążenia dozwolonych na abonament.</span><span class="sxs-lookup"><span data-stu-id="1d66a-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="1d66a-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1d66a-129">-Location</span></span>
<span data-ttu-id="1d66a-130">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1d66a-130">Location of the resource.</span></span>

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

### <span data-ttu-id="1d66a-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="1d66a-131">-MigrationPhase</span></span>
<span data-ttu-id="1d66a-132">Stan migracji, taki jak brak, przygotuj, Zatwierdź i Przerwij.</span><span class="sxs-lookup"><span data-stu-id="1d66a-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="1d66a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d66a-133">-WhatIf</span></span>
<span data-ttu-id="1d66a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d66a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d66a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d66a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d66a-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d66a-136">-Confirm</span></span>
<span data-ttu-id="1d66a-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d66a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d66a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d66a-138">CommonParameters</span></span>
<span data-ttu-id="1d66a-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d66a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d66a-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d66a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d66a-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d66a-141">INPUTS</span></span>

## <span data-ttu-id="1d66a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d66a-142">OUTPUTS</span></span>

### <span data-ttu-id="1d66a-143">Microsoft. AzureStack. Management. Network. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="1d66a-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="1d66a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d66a-144">NOTES</span></span>

## <span data-ttu-id="1d66a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d66a-145">RELATED LINKS</span></span>
