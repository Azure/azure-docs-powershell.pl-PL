---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055835"
---
# <span data-ttu-id="48651-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="48651-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="48651-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48651-102">SYNOPSIS</span></span>
<span data-ttu-id="48651-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="48651-103">Create or update a quota.</span></span>

## <span data-ttu-id="48651-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48651-104">SYNTAX</span></span>

### <span data-ttu-id="48651-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48651-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48651-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="48651-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48651-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48651-107">DESCRIPTION</span></span>
<span data-ttu-id="48651-108">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="48651-108">Create or update a quota.</span></span>

## <span data-ttu-id="48651-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48651-109">EXAMPLES</span></span>

### <span data-ttu-id="48651-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="48651-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="48651-111">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="48651-111">Update a network quota by name.</span></span>

### <span data-ttu-id="48651-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="48651-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="48651-113">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="48651-113">Update a network quota by name.</span></span>

## <span data-ttu-id="48651-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48651-114">PARAMETERS</span></span>

### <span data-ttu-id="48651-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48651-115">-DefaultProfile</span></span>
<span data-ttu-id="48651-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48651-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48651-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="48651-117">-Location</span></span>
<span data-ttu-id="48651-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="48651-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="48651-120">Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="48651-122">Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="48651-124">Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="48651-126">Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="48651-128">Maksymalna liczba połączeń bramy sieci wirtualnej, które mogą być obsługiwane przez subskrypcję dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="48651-130">Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="48651-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="48651-132">Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48651-133">-Name</span></span>
<span data-ttu-id="48651-134">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="48651-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-135">-Przydział</span><span class="sxs-lookup"><span data-stu-id="48651-135">-Quota</span></span>
<span data-ttu-id="48651-136">Zasób przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="48651-136">Network quota resource.</span></span>
<span data-ttu-id="48651-137">Aby skonstruować, zobacz sekcję notatki dla właściwości przydziału i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="48651-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="48651-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="48651-138">-SubscriptionId</span></span>
<span data-ttu-id="48651-139">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48651-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="48651-140">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="48651-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="48651-141">-Tag</span></span>
<span data-ttu-id="48651-142">Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="48651-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48651-143">-Confirm</span></span>
<span data-ttu-id="48651-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48651-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48651-145">-WhatIf</span></span>
<span data-ttu-id="48651-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48651-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48651-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48651-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="48651-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48651-148">CommonParameters</span></span>
<span data-ttu-id="48651-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48651-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48651-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48651-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48651-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48651-151">INPUTS</span></span>

### <span data-ttu-id="48651-152">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="48651-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="48651-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48651-153">OUTPUTS</span></span>

### <span data-ttu-id="48651-154">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="48651-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="48651-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48651-155">NOTES</span></span>

<span data-ttu-id="48651-156">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="48651-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48651-157">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48651-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="48651-158">PRZYDZIAŁ <IQuota> : zasób przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="48651-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="48651-159">`[Tag <IResourceTags>]`: Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="48651-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="48651-160">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="48651-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="48651-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="48651-162">`[MaxNicsPerSubscription <Int64?>]`: Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="48651-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="48651-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="48651-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maksymalna liczba połączeń bramy sieci wirtualnej, których może postanowić subskrypcja dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="48651-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="48651-167">`[MaxVnetsPerSubscription <Int64?>]`: Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="48651-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="48651-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48651-168">RELATED LINKS</span></span>

