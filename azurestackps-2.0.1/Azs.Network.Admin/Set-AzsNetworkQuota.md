---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054228"
---
# <span data-ttu-id="77efe-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="77efe-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="77efe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77efe-102">SYNOPSIS</span></span>
<span data-ttu-id="77efe-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="77efe-103">Create or update a quota.</span></span>

## <span data-ttu-id="77efe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77efe-104">SYNTAX</span></span>

### <span data-ttu-id="77efe-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77efe-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="77efe-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="77efe-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77efe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77efe-107">DESCRIPTION</span></span>
<span data-ttu-id="77efe-108">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="77efe-108">Create or update a quota.</span></span>

## <span data-ttu-id="77efe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77efe-109">EXAMPLES</span></span>

### <span data-ttu-id="77efe-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="77efe-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="77efe-111">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="77efe-111">Update a network quota by name.</span></span>

### <span data-ttu-id="77efe-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="77efe-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="77efe-113">Zaktualizuj przydział sieciowy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="77efe-113">Update a network quota by name.</span></span>

## <span data-ttu-id="77efe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77efe-114">PARAMETERS</span></span>

### <span data-ttu-id="77efe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77efe-115">-DefaultProfile</span></span>
<span data-ttu-id="77efe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77efe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77efe-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="77efe-117">-Location</span></span>
<span data-ttu-id="77efe-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="77efe-118">Location of the resource.</span></span>

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

### <span data-ttu-id="77efe-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="77efe-120">Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="77efe-122">Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-122">Maximum number of NICs a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="77efe-124">Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="77efe-126">Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-126">Maximum number of security groups a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="77efe-128">Maksymalna liczba połączeń bramy sieci wirtualnej, które mogą być obsługiwane przez subskrypcję dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="77efe-130">Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="77efe-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="77efe-132">Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

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

### <span data-ttu-id="77efe-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77efe-133">-Name</span></span>
<span data-ttu-id="77efe-134">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="77efe-134">Name of the resource.</span></span>

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

### <span data-ttu-id="77efe-135">-Przydział</span><span class="sxs-lookup"><span data-stu-id="77efe-135">-Quota</span></span>
<span data-ttu-id="77efe-136">Zasób przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="77efe-136">Network quota resource.</span></span>
<span data-ttu-id="77efe-137">Aby skonstruować, zobacz sekcję notatki dla właściwości przydziału i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="77efe-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

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

### <span data-ttu-id="77efe-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="77efe-138">-SubscriptionId</span></span>
<span data-ttu-id="77efe-139">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77efe-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="77efe-140">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="77efe-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="77efe-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="77efe-141">-Tag</span></span>
<span data-ttu-id="77efe-142">Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="77efe-142">List of key value pairs.</span></span>

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

### <span data-ttu-id="77efe-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77efe-143">-Confirm</span></span>
<span data-ttu-id="77efe-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77efe-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77efe-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77efe-145">-WhatIf</span></span>
<span data-ttu-id="77efe-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77efe-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77efe-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77efe-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77efe-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77efe-148">CommonParameters</span></span>
<span data-ttu-id="77efe-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77efe-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77efe-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77efe-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77efe-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77efe-151">INPUTS</span></span>

### <span data-ttu-id="77efe-152">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="77efe-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="77efe-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77efe-153">OUTPUTS</span></span>

### <span data-ttu-id="77efe-154">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="77efe-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="77efe-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77efe-155">NOTES</span></span>

<span data-ttu-id="77efe-156">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="77efe-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="77efe-157">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="77efe-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="77efe-158">PRZYDZIAŁ <IQuota> : zasób przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="77efe-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="77efe-159">`[Tag <IResourceTags>]`: Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="77efe-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="77efe-160">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="77efe-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="77efe-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="77efe-162">`[MaxNicsPerSubscription <Int64?>]`: Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="77efe-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="77efe-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="77efe-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maksymalna liczba połączeń bramy sieci wirtualnej, których może postanowić subskrypcja dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="77efe-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="77efe-167">`[MaxVnetsPerSubscription <Int64?>]`: Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="77efe-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="77efe-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77efe-168">RELATED LINKS</span></span>

