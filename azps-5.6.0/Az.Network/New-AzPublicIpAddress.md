---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: b3ea1ab3bbe3edbc72b81c25817af40e9e5fc2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958225"
---
# <span data-ttu-id="74ed2-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="74ed2-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="74ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="74ed2-103">Tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-103">Creates a public IP address.</span></span>

## <span data-ttu-id="74ed2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74ed2-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ed2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="74ed2-106">Polecenie **cmdlet New-AzPublicIpAddress** tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="74ed2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="74ed2-108">Przykład 1. Tworzenie nowego publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="74ed2-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="74ed2-109">To polecenie tworzy nowy zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="74ed2-110">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ wartość -AllocationMethod jest określana jako statyczna.</span><span class="sxs-lookup"><span data-stu-id="74ed2-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="74ed2-111">Jeśli zostanie on określony jako "Dynamiczny", publiczny adres IP zostanie przydzielony tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (na przykład maszyny wirtualnej lub równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="74ed2-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="74ed2-112">Przykład 2. Tworzenie publicznego adresu IP z odwrotną domeną FQDN</span><span class="sxs-lookup"><span data-stu-id="74ed2-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="74ed2-113">To polecenie tworzy nowy zasób publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="74ed2-114">W przypadku parametru -ReverseFqdn platforma Azure tworzy rekord PTR DNS (odnośnik odwrotny) dla publicznego adresu IP przydzielonego do tego zasobu, który $customFqdn określony w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="74ed2-115">Jako wymaganie wstępne $customFqdn (na przykład webapp.contoso.com) powinien mieć rekord CNAME DNS (odnośnik do przodu) który wskaże adres $dnsPrefix.$location.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="74ed2-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="74ed2-116">Przykład 3. Tworzenie nowego publicznego adresu IP przy użyciu tagu IpTag</span><span class="sxs-lookup"><span data-stu-id="74ed2-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="74ed2-117">To polecenie tworzy nowy zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="74ed2-118">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ wartość -AllocationMethod jest określana jako statyczna.</span><span class="sxs-lookup"><span data-stu-id="74ed2-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="74ed2-119">Jeśli zostanie on określony jako "Dynamiczny", publiczny adres IP zostanie przydzielony tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (na przykład maszyny wirtualnej lub równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="74ed2-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="74ed2-120">Tag Ip jest używany do oznaczania znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="74ed2-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="74ed2-121">Tag Iptag można określić przy użyciu New-AzPublicIpTag i przekazany jako dane wejściowe za pośrednictwem -IpTags.</span><span class="sxs-lookup"><span data-stu-id="74ed2-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="74ed2-122">Przykład 4. Tworzenie nowego publicznego adresu IP z prefiksem</span><span class="sxs-lookup"><span data-stu-id="74ed2-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="74ed2-123">To polecenie tworzy nowy zasób publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="74ed2-124">Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="74ed2-125">Publiczny adres IP jest natychmiast przydzielany do tego zasobu z określonego publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="74ed2-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="74ed2-126">Ta opcja jest obsługiwana tylko dla standardowej wersji SKU i statycznej metody AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="74ed2-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="74ed2-127">Przykład 5. Tworzenie nowego globalnego publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="74ed2-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="74ed2-128">To polecenie tworzy nowy globalny zasób publicznych adresów IP. Tworzony jest rekord DNS dla domeny $dnsPrefix.$location.cloudapp.azure.com, który wskaże publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="74ed2-129">Do tego zasobu zostanie natychmiast przydzielony globalny publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="74ed2-130">Ta opcja jest obsługiwana tylko dla standardowej wersji SKU i statycznej metody AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="74ed2-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="74ed2-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74ed2-131">PARAMETERS</span></span>

### <span data-ttu-id="74ed2-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="74ed2-132">-AllocationMethod</span></span>
<span data-ttu-id="74ed2-133">Określa metodę przydzielania publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="74ed2-134">Dopuszczalne wartości dla tego parametru to: statyczny lub dynamiczny.</span><span class="sxs-lookup"><span data-stu-id="74ed2-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-135">— AsJob</span><span class="sxs-lookup"><span data-stu-id="74ed2-135">-AsJob</span></span>
<span data-ttu-id="74ed2-136">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74ed2-136">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ed2-137">-DefaultProfile</span></span>
<span data-ttu-id="74ed2-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74ed2-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ed2-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="74ed2-139">-DomainNameLabel</span></span>
<span data-ttu-id="74ed2-140">Określa względną nazwę DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-140">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-141">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="74ed2-141">-Force</span></span>
<span data-ttu-id="74ed2-142">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74ed2-142">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="74ed2-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="74ed2-144">Określa czas bezczynności (w minutach).</span><span class="sxs-lookup"><span data-stu-id="74ed2-144">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="74ed2-145">-IpAddressVersion</span></span>
<span data-ttu-id="74ed2-146">Określa wersję adresu IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-146">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="74ed2-147">-IpTag</span></span>
<span data-ttu-id="74ed2-148">Lista tagów IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-148">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-149">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74ed2-149">-Location</span></span>
<span data-ttu-id="74ed2-150">Określa region, w którym ma być tworzyć publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-150">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-151">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74ed2-151">-Name</span></span>
<span data-ttu-id="74ed2-152">Określa nazwę publicznego adresu IP, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ed2-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-153">- PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74ed2-153">-PublicIpPrefix</span></span>
<span data-ttu-id="74ed2-154">Określa ustawienie PSPublicIpPrefix, z którego należy przydzielić publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74ed2-155">-ResourceGroupName</span></span>
<span data-ttu-id="74ed2-156">Określa nazwę grupy zasobów, w której ma być tworzyć publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="74ed2-157">-ReverseFqdn</span></span>
<span data-ttu-id="74ed2-158">Określa w pełni kwalifikowaną nazwę domeny (FQDN).</span><span class="sxs-lookup"><span data-stu-id="74ed2-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-159">- SKU</span><span class="sxs-lookup"><span data-stu-id="74ed2-159">-Sku</span></span>
<span data-ttu-id="74ed2-160">Nazwa publicznej sku adresu IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-160">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-161">— Tag</span><span class="sxs-lookup"><span data-stu-id="74ed2-161">-Tag</span></span>
<span data-ttu-id="74ed2-162">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74ed2-163">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="74ed2-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-164">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="74ed2-164">-Tier</span></span>
<span data-ttu-id="74ed2-165">Publiczna warstwa SKU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="74ed2-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-166">— Strefa</span><span class="sxs-lookup"><span data-stu-id="74ed2-166">-Zone</span></span>
<span data-ttu-id="74ed2-167">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="74ed2-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74ed2-168">-Confirm</span></span>
<span data-ttu-id="74ed2-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74ed2-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ed2-170">-WhatIf</span></span>
<span data-ttu-id="74ed2-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ed2-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ed2-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74ed2-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ed2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ed2-173">CommonParameters</span></span>
<span data-ttu-id="74ed2-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ed2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ed2-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74ed2-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ed2-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74ed2-176">INPUTS</span></span>

### <span data-ttu-id="74ed2-177">System.String</span><span class="sxs-lookup"><span data-stu-id="74ed2-177">System.String</span></span>

### <span data-ttu-id="74ed2-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="74ed2-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="74ed2-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74ed2-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="74ed2-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="74ed2-180">System.Int32</span></span>

### <span data-ttu-id="74ed2-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="74ed2-181">System.String[]</span></span>

### <span data-ttu-id="74ed2-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="74ed2-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="74ed2-183">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74ed2-183">OUTPUTS</span></span>

### <span data-ttu-id="74ed2-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="74ed2-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="74ed2-185">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74ed2-185">NOTES</span></span>

## <span data-ttu-id="74ed2-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74ed2-186">RELATED LINKS</span></span>

[<span data-ttu-id="74ed2-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="74ed2-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="74ed2-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="74ed2-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="74ed2-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="74ed2-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
