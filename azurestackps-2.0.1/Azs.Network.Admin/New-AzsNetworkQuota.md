---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054211"
---
# <span data-ttu-id="30a74-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="30a74-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="30a74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30a74-102">SYNOPSIS</span></span>
<span data-ttu-id="30a74-103">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="30a74-103">Create or update a quota.</span></span>

## <span data-ttu-id="30a74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30a74-104">SYNTAX</span></span>

### <span data-ttu-id="30a74-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="30a74-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30a74-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="30a74-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30a74-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30a74-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30a74-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="30a74-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30a74-109">Opis</span><span class="sxs-lookup"><span data-stu-id="30a74-109">DESCRIPTION</span></span>
<span data-ttu-id="30a74-110">Tworzenie lub aktualizowanie przydziału.</span><span class="sxs-lookup"><span data-stu-id="30a74-110">Create or update a quota.</span></span>

## <span data-ttu-id="30a74-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30a74-111">EXAMPLES</span></span>

### <span data-ttu-id="30a74-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="30a74-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="30a74-113">Utwórz nowy przydział sieci z wartościami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="30a74-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="30a74-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="30a74-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="30a74-115">Utwórz nowy przydział sieci z wartościami niedomyślnymi przydziału.</span><span class="sxs-lookup"><span data-stu-id="30a74-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="30a74-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30a74-116">PARAMETERS</span></span>

### <span data-ttu-id="30a74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a74-117">-DefaultProfile</span></span>
<span data-ttu-id="30a74-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30a74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a74-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="30a74-119">-InputObject</span></span>
<span data-ttu-id="30a74-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="30a74-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="30a74-121">-Location</span></span>
<span data-ttu-id="30a74-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="30a74-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="30a74-124">Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="30a74-126">Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="30a74-128">Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="30a74-130">Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="30a74-132">Maksymalna liczba połączeń bramy sieci wirtualnej, które mogą być obsługiwane przez subskrypcję dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="30a74-134">Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="30a74-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="30a74-136">Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30a74-137">-Name</span></span>
<span data-ttu-id="30a74-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="30a74-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-139">-Przydział</span><span class="sxs-lookup"><span data-stu-id="30a74-139">-Quota</span></span>
<span data-ttu-id="30a74-140">Zasób przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="30a74-140">Network quota resource.</span></span>
<span data-ttu-id="30a74-141">Aby skonstruować, zobacz sekcję notatki dla właściwości przydziału i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="30a74-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="30a74-142">-SubscriptionId</span></span>
<span data-ttu-id="30a74-143">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30a74-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30a74-144">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="30a74-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="30a74-145">-Tag</span></span>
<span data-ttu-id="30a74-146">Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="30a74-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30a74-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30a74-147">-Confirm</span></span>
<span data-ttu-id="30a74-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a74-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a74-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a74-149">-WhatIf</span></span>
<span data-ttu-id="30a74-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a74-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a74-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30a74-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a74-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a74-152">CommonParameters</span></span>
<span data-ttu-id="30a74-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a74-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a74-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a74-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a74-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a74-155">INPUTS</span></span>

### <span data-ttu-id="30a74-156">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="30a74-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="30a74-157">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="30a74-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="30a74-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30a74-158">OUTPUTS</span></span>

### <span data-ttu-id="30a74-159">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="30a74-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="30a74-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30a74-160">NOTES</span></span>

<span data-ttu-id="30a74-161">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="30a74-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30a74-162">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30a74-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="30a74-163">INPUTobject <INetworkAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="30a74-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30a74-164">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="30a74-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30a74-165">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="30a74-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="30a74-166">`[ResourceName <String>]`: Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="30a74-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="30a74-167">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30a74-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30a74-168">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="30a74-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="30a74-169">PRZYDZIAŁ <IQuota> : zasób przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="30a74-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="30a74-170">`[Tag <IResourceTags>]`: Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="30a74-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="30a74-171">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="30a74-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="30a74-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="30a74-173">`[MaxNicsPerSubscription <Int64?>]`: Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="30a74-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="30a74-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="30a74-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maksymalna liczba połączeń bramy sieci wirtualnej, których może postanowić subskrypcja dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="30a74-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="30a74-178">`[MaxVnetsPerSubscription <Int64?>]`: Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="30a74-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="30a74-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30a74-179">RELATED LINKS</span></span>

