---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552880"
---
# <span data-ttu-id="f8325-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8325-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="f8325-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8325-102">SYNOPSIS</span></span>
<span data-ttu-id="f8325-103">Tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8325-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8325-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8325-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8325-105">DESCRIPTION</span></span>
<span data-ttu-id="f8325-106">Polecenie cmdlet **New-AzureRmPublicIpAddress** tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="f8325-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8325-107">EXAMPLES</span></span>

### <span data-ttu-id="f8325-108">1: Tworzenie nowego publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="f8325-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="f8325-109">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="f8325-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f8325-110">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="f8325-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f8325-111">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="f8325-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="f8325-112">2: Tworzenie publicznego adresu IP z odwrotną nazwą FQDN</span><span class="sxs-lookup"><span data-stu-id="f8325-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="f8325-113">To polecenie tworzy nowy publiczny zasób adres IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="f8325-114">W przypadku parametru-ReverseFqdn platforma Azure tworzy rekord DNS PTR (odwrotne wyszukiwanie) dla publicznego adresu IP przydzielonego temu zasobowi, wskazując $customFqdn określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="f8325-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="f8325-115">Jako warunek wstępny $customFqdn (Powiedz webapp.contoso.com) powinien mieć rekord CNAME DNS (do wyszukiwania wstecznego) wskazujący $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="f8325-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="f8325-116">3: Tworzenie nowego publicznego adresu IP z IpTag</span><span class="sxs-lookup"><span data-stu-id="f8325-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="f8325-117">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="f8325-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f8325-118">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="f8325-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f8325-119">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="f8325-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="f8325-120">Do określonych tagów skojarzonych z zasobem jest używana Iptag.</span><span class="sxs-lookup"><span data-stu-id="f8325-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="f8325-121">Iptag można określić przy użyciu New-AzureRmPublicIpTag i przekazać jako dane wejściowe za pośrednictwem parametru-IpTags.</span><span class="sxs-lookup"><span data-stu-id="f8325-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="f8325-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8325-122">PARAMETERS</span></span>

### <span data-ttu-id="f8325-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f8325-123">-AllocationMethod</span></span>
<span data-ttu-id="f8325-124">Określa metodę przydzielenia publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="f8325-125">Dopuszczalne wartości tego parametru to: static lub Dynamic.</span><span class="sxs-lookup"><span data-stu-id="f8325-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8325-126">-AsJob</span></span>
<span data-ttu-id="f8325-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8325-127">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8325-128">-DefaultProfile</span></span>
<span data-ttu-id="f8325-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8325-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f8325-130">-DomainNameLabel</span></span>
<span data-ttu-id="f8325-131">Określa względną nazwę DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-131">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f8325-132">-Force</span></span>
<span data-ttu-id="f8325-133">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8325-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f8325-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f8325-135">Określa limit czasu bezczynności (w minutach).</span><span class="sxs-lookup"><span data-stu-id="f8325-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f8325-136">-IpAddressVersion</span></span>
<span data-ttu-id="f8325-137">Określa wersję adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="f8325-138">-IpTag</span></span>
<span data-ttu-id="f8325-139">Lista IpTag.</span><span class="sxs-lookup"><span data-stu-id="f8325-139">IpTag List.</span></span>

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

### <span data-ttu-id="f8325-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f8325-140">-Location</span></span>
<span data-ttu-id="f8325-141">Określa region, w którym ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-141">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8325-142">-Name</span></span>
<span data-ttu-id="f8325-143">Określa nazwę publicznego adresu IP tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8325-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8325-144">-ResourceGroupName</span></span>
<span data-ttu-id="f8325-145">Określa nazwę grupy zasobów, w której ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="f8325-146">-ReverseFqdn</span></span>
<span data-ttu-id="f8325-147">Określa odwrotną, w pełni kwalifikowaną nazwę domeny (FQDN).</span><span class="sxs-lookup"><span data-stu-id="f8325-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="f8325-148">-Sku</span></span>
<span data-ttu-id="f8325-149">Nazwa publicznej jednostki SKU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f8325-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8325-150">-Tag</span></span>
<span data-ttu-id="f8325-151">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f8325-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f8325-152">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f8325-152">For example:</span></span>

<span data-ttu-id="f8325-153">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f8325-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="f8325-154">-Zone</span></span>
<span data-ttu-id="f8325-155">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="f8325-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f8325-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8325-156">-Confirm</span></span>
<span data-ttu-id="f8325-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8325-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8325-158">-WhatIf</span></span>
<span data-ttu-id="f8325-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8325-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8325-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8325-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8325-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8325-161">CommonParameters</span></span>
<span data-ttu-id="f8325-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8325-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8325-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8325-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8325-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8325-164">INPUTS</span></span>

### <span data-ttu-id="f8325-165">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8325-165">None</span></span>
<span data-ttu-id="f8325-166">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f8325-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8325-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8325-167">OUTPUTS</span></span>

### <span data-ttu-id="f8325-168">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8325-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f8325-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8325-169">NOTES</span></span>

## <span data-ttu-id="f8325-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8325-170">RELATED LINKS</span></span>

[<span data-ttu-id="f8325-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8325-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f8325-172">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8325-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f8325-173">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8325-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
