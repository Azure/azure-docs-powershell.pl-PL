---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 7ef0d3ce20868c4240abc43278cdc38a33efa5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554052"
---
# <span data-ttu-id="da0c3-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da0c3-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="da0c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="da0c3-103">Tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da0c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da0c3-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-PublicIpPrefix <Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix>]
 [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da0c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="da0c3-106">Polecenie cmdlet **New-AzureRmPublicIpAddress** tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="da0c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da0c3-107">EXAMPLES</span></span>

### <span data-ttu-id="da0c3-108">1: Tworzenie nowego publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="da0c3-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="da0c3-109">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="da0c3-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="da0c3-110">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="da0c3-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="da0c3-111">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="da0c3-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="da0c3-112">2: Tworzenie publicznego adresu IP z odwrotną nazwą FQDN</span><span class="sxs-lookup"><span data-stu-id="da0c3-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="da0c3-113">To polecenie tworzy nowy publiczny zasób adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="da0c3-114">W przypadku parametru-ReverseFqdn platforma Azure tworzy rekord DNS PTR (odwrotne wyszukiwanie) dla publicznego adresu IP przydzielonego temu zasobowi, wskazując $customFqdn określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="da0c3-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="da0c3-115">Jako warunek wstępny $customFqdn (Powiedz webapp.contoso.com) powinien mieć rekord CNAME DNS (do wyszukiwania wstecznego) wskazujący $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="da0c3-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="da0c3-116">3: Tworzenie nowego publicznego adresu IP z IpTag</span><span class="sxs-lookup"><span data-stu-id="da0c3-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="da0c3-117">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="da0c3-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="da0c3-118">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="da0c3-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="da0c3-119">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="da0c3-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="da0c3-120">Do określonych tagów skojarzonych z zasobem jest używana Iptag.</span><span class="sxs-lookup"><span data-stu-id="da0c3-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="da0c3-121">Iptag można określić przy użyciu New-AzureRmPublicIpTag i przekazać jako dane wejściowe za pośrednictwem parametru-IpTags.</span><span class="sxs-lookup"><span data-stu-id="da0c3-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="da0c3-122">4: Tworzenie nowego publicznego adresu IP na podstawie prefiksu</span><span class="sxs-lookup"><span data-stu-id="da0c3-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="da0c3-123">To polecenie tworzy nowy publiczny zasób adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="da0c3-124">Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="da0c3-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="da0c3-125">Publiczny adres IP jest natychmiast przydzielany do tego zasobu z określonego publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="da0c3-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="da0c3-126">Ta opcja jest obsługiwana tylko w przypadku jednostek SKU "Standardowa" i "static" AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="da0c3-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="da0c3-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da0c3-127">PARAMETERS</span></span>

### <span data-ttu-id="da0c3-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="da0c3-128">-AllocationMethod</span></span>
<span data-ttu-id="da0c3-129">Określa metodę przydzielenia publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="da0c3-130">Dopuszczalne wartości tego parametru to: static lub Dynamic.</span><span class="sxs-lookup"><span data-stu-id="da0c3-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="da0c3-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da0c3-131">-AsJob</span></span>
<span data-ttu-id="da0c3-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="da0c3-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da0c3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0c3-133">-DefaultProfile</span></span>
<span data-ttu-id="da0c3-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da0c3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0c3-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="da0c3-135">-DomainNameLabel</span></span>
<span data-ttu-id="da0c3-136">Określa względną nazwę DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="da0c3-137">-Force</span><span class="sxs-lookup"><span data-stu-id="da0c3-137">-Force</span></span>
<span data-ttu-id="da0c3-138">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="da0c3-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da0c3-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="da0c3-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="da0c3-140">Określa limit czasu bezczynności (w minutach).</span><span class="sxs-lookup"><span data-stu-id="da0c3-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="da0c3-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="da0c3-141">-IpAddressVersion</span></span>
<span data-ttu-id="da0c3-142">Określa wersję adresu IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-142">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="da0c3-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="da0c3-143">-IpTag</span></span>
<span data-ttu-id="da0c3-144">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="da0c3-144">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0c3-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="da0c3-145">-Location</span></span>
<span data-ttu-id="da0c3-146">Określa region, w którym ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="da0c3-147">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="da0c3-147">-PublicIpPrefix</span></span>
<span data-ttu-id="da0c3-148">Określa PSPublicIpPrefix, z której należy przydzielić publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-148">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="da0c3-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da0c3-149">-Name</span></span>
<span data-ttu-id="da0c3-150">Określa nazwę publicznego adresu IP tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da0c3-150">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da0c3-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0c3-151">-ResourceGroupName</span></span>
<span data-ttu-id="da0c3-152">Określa nazwę grupy zasobów, w której ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="da0c3-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="da0c3-153">-ReverseFqdn</span></span>
<span data-ttu-id="da0c3-154">Określa odwrotną, w pełni kwalifikowaną nazwę domeny (FQDN).</span><span class="sxs-lookup"><span data-stu-id="da0c3-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="da0c3-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="da0c3-155">-Sku</span></span>
<span data-ttu-id="da0c3-156">Nazwa publicznej jednostki SKU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="da0c3-156">The public IP Sku name.</span></span>

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

### <span data-ttu-id="da0c3-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="da0c3-157">-Tag</span></span>
<span data-ttu-id="da0c3-158">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="da0c3-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="da0c3-159">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="da0c3-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da0c3-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="da0c3-160">-Zone</span></span>
<span data-ttu-id="da0c3-161">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="da0c3-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0c3-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da0c3-162">-Confirm</span></span>
<span data-ttu-id="da0c3-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da0c3-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0c3-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0c3-164">-WhatIf</span></span>
<span data-ttu-id="da0c3-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da0c3-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da0c3-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da0c3-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0c3-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0c3-167">CommonParameters</span></span>
<span data-ttu-id="da0c3-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da0c3-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0c3-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da0c3-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0c3-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da0c3-170">INPUTS</span></span>

### <span data-ttu-id="da0c3-171">System. String</span><span class="sxs-lookup"><span data-stu-id="da0c3-171">System.String</span></span>

### <span data-ttu-id="da0c3-172">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSPublicIpTag; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="da0c3-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="da0c3-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="da0c3-173">System.Int32</span></span>

### <span data-ttu-id="da0c3-174">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="da0c3-174">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="da0c3-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da0c3-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da0c3-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da0c3-176">OUTPUTS</span></span>

### <span data-ttu-id="da0c3-177">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da0c3-177">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="da0c3-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da0c3-178">NOTES</span></span>

## <span data-ttu-id="da0c3-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da0c3-179">RELATED LINKS</span></span>

[<span data-ttu-id="da0c3-180">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da0c3-180">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="da0c3-181">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da0c3-181">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="da0c3-182">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da0c3-182">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
