---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 9b8da32a336b0320f8ca69b6f6e09d584315d0d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709256"
---
# <span data-ttu-id="2a728-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a728-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="2a728-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a728-102">SYNOPSIS</span></span>
<span data-ttu-id="2a728-103">Tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-103">Creates a public IP address.</span></span>

## <span data-ttu-id="2a728-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a728-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a728-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a728-105">DESCRIPTION</span></span>
<span data-ttu-id="2a728-106">Polecenie cmdlet **New-AzPublicIpAddress** tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="2a728-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a728-107">EXAMPLES</span></span>

### <span data-ttu-id="2a728-108">1: Tworzenie nowego publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="2a728-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="2a728-109">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a728-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2a728-110">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="2a728-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2a728-111">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="2a728-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="2a728-112">2: Tworzenie publicznego adresu IP z odwrotną nazwą FQDN</span><span class="sxs-lookup"><span data-stu-id="2a728-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="2a728-113">To polecenie tworzy nowy publiczny zasób adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2a728-114">W przypadku parametru-ReverseFqdn platforma Azure tworzy rekord DNS PTR (odwrotne wyszukiwanie) dla publicznego adresu IP przydzielonego temu zasobowi, wskazując $customFqdn określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="2a728-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="2a728-115">Jako warunek wstępny $customFqdn (Powiedz webapp.contoso.com) powinien mieć rekord CNAME DNS (do wyszukiwania wstecznego) wskazujący $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="2a728-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="2a728-116">3: Tworzenie nowego publicznego adresu IP z IpTag</span><span class="sxs-lookup"><span data-stu-id="2a728-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="2a728-117">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a728-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2a728-118">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="2a728-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2a728-119">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="2a728-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="2a728-120">Do określonych tagów skojarzonych z zasobem jest używana Iptag.</span><span class="sxs-lookup"><span data-stu-id="2a728-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="2a728-121">Iptag można określić przy użyciu New-AzPublicIpTag i przekazać jako dane wejściowe za pośrednictwem parametru-IpTags.</span><span class="sxs-lookup"><span data-stu-id="2a728-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="2a728-122">4: Tworzenie nowego publicznego adresu IP na podstawie prefiksu</span><span class="sxs-lookup"><span data-stu-id="2a728-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="2a728-123">To polecenie tworzy nowy publiczny zasób adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2a728-124">Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a728-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2a728-125">Publiczny adres IP jest natychmiast przydzielany do tego zasobu z określonego publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2a728-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="2a728-126">Ta opcja jest obsługiwana tylko w przypadku jednostek SKU "Standardowa" i "static" AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="2a728-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="2a728-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a728-127">PARAMETERS</span></span>

### <span data-ttu-id="2a728-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="2a728-128">-AllocationMethod</span></span>
<span data-ttu-id="2a728-129">Określa metodę przydzielenia publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="2a728-130">Dopuszczalne wartości tego parametru to: static lub Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2a728-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="2a728-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a728-131">-AsJob</span></span>
<span data-ttu-id="2a728-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2a728-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a728-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a728-133">-DefaultProfile</span></span>
<span data-ttu-id="2a728-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a728-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a728-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="2a728-135">-DomainNameLabel</span></span>
<span data-ttu-id="2a728-136">Określa względną nazwę DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="2a728-137">-Force</span><span class="sxs-lookup"><span data-stu-id="2a728-137">-Force</span></span>
<span data-ttu-id="2a728-138">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a728-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a728-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2a728-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2a728-140">Określa limit czasu bezczynności (w minutach).</span><span class="sxs-lookup"><span data-stu-id="2a728-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="2a728-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2a728-141">-IpAddressVersion</span></span>
<span data-ttu-id="2a728-142">Określa wersję adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-142">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="2a728-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="2a728-143">-IpTag</span></span>
<span data-ttu-id="2a728-144">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="2a728-144">IpTag List.</span></span>

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

### <span data-ttu-id="2a728-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2a728-145">-Location</span></span>
<span data-ttu-id="2a728-146">Określa region, w którym ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2a728-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a728-147">-Name</span></span>
<span data-ttu-id="2a728-148">Określa nazwę publicznego adresu IP tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a728-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2a728-149">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a728-149">-PublicIpPrefix</span></span>
<span data-ttu-id="2a728-150">Określa PSPublicIpPrefix, z której należy przydzielić publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="2a728-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a728-151">-ResourceGroupName</span></span>
<span data-ttu-id="2a728-152">Określa nazwę grupy zasobów, w której ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2a728-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="2a728-153">-ReverseFqdn</span></span>
<span data-ttu-id="2a728-154">Określa odwrotną, w pełni kwalifikowaną nazwę domeny (FQDN).</span><span class="sxs-lookup"><span data-stu-id="2a728-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="2a728-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="2a728-155">-Sku</span></span>
<span data-ttu-id="2a728-156">Nazwa publicznej jednostki SKU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2a728-156">The public IP Sku name.</span></span>

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

### <span data-ttu-id="2a728-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a728-157">-Tag</span></span>
<span data-ttu-id="2a728-158">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2a728-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a728-159">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="2a728-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2a728-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="2a728-160">-Zone</span></span>
<span data-ttu-id="2a728-161">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="2a728-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2a728-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a728-162">-Confirm</span></span>
<span data-ttu-id="2a728-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a728-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a728-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a728-164">-WhatIf</span></span>
<span data-ttu-id="2a728-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a728-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a728-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a728-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a728-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a728-167">CommonParameters</span></span>
<span data-ttu-id="2a728-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a728-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a728-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a728-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a728-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a728-170">INPUTS</span></span>

### <span data-ttu-id="2a728-171">System. String</span><span class="sxs-lookup"><span data-stu-id="2a728-171">System.String</span></span>

### <span data-ttu-id="2a728-172">Microsoft. Azure. Commands. Network. models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="2a728-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="2a728-173">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a728-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="2a728-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2a728-174">System.Int32</span></span>

### <span data-ttu-id="2a728-175">System. String []</span><span class="sxs-lookup"><span data-stu-id="2a728-175">System.String[]</span></span>

### <span data-ttu-id="2a728-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a728-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2a728-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a728-177">OUTPUTS</span></span>

### <span data-ttu-id="2a728-178">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a728-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2a728-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a728-179">NOTES</span></span>

## <span data-ttu-id="2a728-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a728-180">RELATED LINKS</span></span>

[<span data-ttu-id="2a728-181">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a728-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="2a728-182">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a728-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="2a728-183">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a728-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)