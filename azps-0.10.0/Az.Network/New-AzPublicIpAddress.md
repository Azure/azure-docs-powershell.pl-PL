---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 308758942a160b95f1a5bea89a476c15a0dcf003
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890441"
---
# <span data-ttu-id="5a81e-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5a81e-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="5a81e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a81e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a81e-103">Tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-103">Creates a public IP address.</span></span>

## <span data-ttu-id="5a81e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a81e-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a81e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a81e-105">DESCRIPTION</span></span>
<span data-ttu-id="5a81e-106">Polecenie cmdlet **New-AzPublicIpAddress** tworzy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="5a81e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a81e-107">EXAMPLES</span></span>

### <span data-ttu-id="5a81e-108">1: Tworzenie nowego publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="5a81e-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="5a81e-109">To polecenie tworzy nowy publiczny zasób adres IP. Dla $dnsPrefix jest tworzony rekord DNS. $location. cloudapp.azure.com wskazujący publiczny adres IP tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="5a81e-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="5a81e-110">Publiczny adres IP jest natychmiast przydzielany do tego zasobu, ponieważ parametr-AllocationMethod jest określony jako "static".</span><span class="sxs-lookup"><span data-stu-id="5a81e-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="5a81e-111">Jeśli jest określony jako "dynamiczny", publiczny adres IP jest przydzielany tylko po uruchomieniu (lub utworzeniu) skojarzonego zasobu (takiego jak maszyna wirtualna lub moduł równoważenia obciążenia).</span><span class="sxs-lookup"><span data-stu-id="5a81e-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="5a81e-112">2: Tworzenie publicznego adresu IP z odwrotną nazwą FQDN</span><span class="sxs-lookup"><span data-stu-id="5a81e-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="5a81e-113">To polecenie tworzy nowy publiczny zasób adres IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="5a81e-114">W przypadku parametru-ReverseFqdn platforma Azure tworzy rekord DNS PTR (odwrotne wyszukiwanie) dla publicznego adresu IP przydzielonego temu zasobowi, wskazując $customFqdn określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="5a81e-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="5a81e-115">Jako warunek wstępny $customFqdn (Powiedz webapp.contoso.com) powinien mieć rekord CNAME DNS (do wyszukiwania wstecznego) wskazujący $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="5a81e-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="5a81e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a81e-116">PARAMETERS</span></span>

### <span data-ttu-id="5a81e-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5a81e-117">-AllocationMethod</span></span>
<span data-ttu-id="5a81e-118">Określa metodę przydzielenia publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="5a81e-119">Dopuszczalne wartości tego parametru to: static lub Dynamic.</span><span class="sxs-lookup"><span data-stu-id="5a81e-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="5a81e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a81e-120">-AsJob</span></span>
<span data-ttu-id="5a81e-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5a81e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a81e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a81e-122">-DefaultProfile</span></span>
<span data-ttu-id="5a81e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a81e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a81e-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5a81e-124">-DomainNameLabel</span></span>
<span data-ttu-id="5a81e-125">Określa względną nazwę DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="5a81e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5a81e-126">-Force</span></span>
<span data-ttu-id="5a81e-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5a81e-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a81e-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5a81e-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5a81e-129">Określa limit czasu bezczynności (w minutach).</span><span class="sxs-lookup"><span data-stu-id="5a81e-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="5a81e-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5a81e-130">-IpAddressVersion</span></span>
<span data-ttu-id="5a81e-131">Określa wersję adresu IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="5a81e-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5a81e-132">-Location</span></span>
<span data-ttu-id="5a81e-133">Określa region, w którym ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="5a81e-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a81e-134">-Name</span></span>
<span data-ttu-id="5a81e-135">Określa nazwę publicznego adresu IP tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a81e-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5a81e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a81e-136">-ResourceGroupName</span></span>
<span data-ttu-id="5a81e-137">Określa nazwę grupy zasobów, w której ma zostać utworzony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="5a81e-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="5a81e-138">-ReverseFqdn</span></span>
<span data-ttu-id="5a81e-139">Określa odwrotną, w pełni kwalifikowaną nazwę domeny (FQDN).</span><span class="sxs-lookup"><span data-stu-id="5a81e-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="5a81e-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="5a81e-140">-Sku</span></span>
<span data-ttu-id="5a81e-141">Nazwa publicznej jednostki SKU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="5a81e-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="5a81e-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a81e-142">-Tag</span></span>
<span data-ttu-id="5a81e-143">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5a81e-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a81e-144">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="5a81e-144">For example:</span></span>

<span data-ttu-id="5a81e-145">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5a81e-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5a81e-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="5a81e-146">-Zone</span></span>
<span data-ttu-id="5a81e-147">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="5a81e-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5a81e-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a81e-148">-Confirm</span></span>
<span data-ttu-id="5a81e-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a81e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a81e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a81e-150">-WhatIf</span></span>
<span data-ttu-id="5a81e-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a81e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a81e-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a81e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a81e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a81e-153">CommonParameters</span></span>
<span data-ttu-id="5a81e-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a81e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a81e-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a81e-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a81e-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a81e-156">INPUTS</span></span>

## <span data-ttu-id="5a81e-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a81e-157">OUTPUTS</span></span>

### <span data-ttu-id="5a81e-158">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5a81e-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="5a81e-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a81e-159">NOTES</span></span>

## <span data-ttu-id="5a81e-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a81e-160">RELATED LINKS</span></span>

[<span data-ttu-id="5a81e-161">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5a81e-161">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="5a81e-162">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5a81e-162">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="5a81e-163">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5a81e-163">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
