---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223330"
---
# <span data-ttu-id="92327-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="92327-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="92327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92327-102">SYNOPSIS</span></span>
<span data-ttu-id="92327-103">Tworzy usługę linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="92327-103">Creates a private link service</span></span>

## <span data-ttu-id="92327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92327-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92327-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92327-105">DESCRIPTION</span></span>
<span data-ttu-id="92327-106">Polecenie cmdlet **New-AzPrivateLinkService** tworzy prywatną usługę link.</span><span class="sxs-lookup"><span data-stu-id="92327-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="92327-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92327-107">EXAMPLES</span></span>

### <span data-ttu-id="92327-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92327-108">Example 1</span></span>

<span data-ttu-id="92327-109">W poniższym przykładzie jest tworzona usługa linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="92327-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="92327-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92327-110">PARAMETERS</span></span>

### <span data-ttu-id="92327-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92327-111">-AsJob</span></span>
<span data-ttu-id="92327-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="92327-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92327-113">-Autozatwierdzanie</span><span class="sxs-lookup"><span data-stu-id="92327-113">-AutoApproval</span></span>
<span data-ttu-id="92327-114">Automatyczne subskrypcje zatwierdzania usługi linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="92327-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="92327-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92327-115">-DefaultProfile</span></span>
<span data-ttu-id="92327-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92327-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92327-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="92327-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="92327-118">Włącz protokół proxy dla usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="92327-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="92327-119">-Force</span><span class="sxs-lookup"><span data-stu-id="92327-119">-Force</span></span>
<span data-ttu-id="92327-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="92327-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="92327-121">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="92327-121">-IpConfiguration</span></span>
<span data-ttu-id="92327-122">Konfiguracje adresów IP</span><span class="sxs-lookup"><span data-stu-id="92327-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92327-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="92327-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="92327-124">Konfiguracje frontonu IP</span><span class="sxs-lookup"><span data-stu-id="92327-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92327-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="92327-125">-Location</span></span>
<span data-ttu-id="92327-126">pozycję.</span><span class="sxs-lookup"><span data-stu-id="92327-126">location.</span></span>

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

### <span data-ttu-id="92327-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92327-127">-Name</span></span>
<span data-ttu-id="92327-128">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="92327-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92327-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92327-129">-ResourceGroupName</span></span>
<span data-ttu-id="92327-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92327-130">The resource group name.</span></span>

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

### <span data-ttu-id="92327-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="92327-131">-Tag</span></span>
<span data-ttu-id="92327-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="92327-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92327-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="92327-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="92327-134">-Widoczność</span><span class="sxs-lookup"><span data-stu-id="92327-134">-Visibility</span></span>
<span data-ttu-id="92327-135">Abonamenty na widoczność prywatnych usług linków</span><span class="sxs-lookup"><span data-stu-id="92327-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="92327-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92327-136">-Confirm</span></span>
<span data-ttu-id="92327-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92327-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92327-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92327-138">-WhatIf</span></span>
<span data-ttu-id="92327-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92327-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92327-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92327-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92327-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92327-141">CommonParameters</span></span>
<span data-ttu-id="92327-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92327-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92327-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92327-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92327-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92327-144">INPUTS</span></span>

### <span data-ttu-id="92327-145">System. String</span><span class="sxs-lookup"><span data-stu-id="92327-145">System.String</span></span>

### <span data-ttu-id="92327-146">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="92327-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="92327-147">Microsoft. Azure. Commands. Network. models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="92327-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="92327-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92327-148">OUTPUTS</span></span>

### <span data-ttu-id="92327-149">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="92327-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="92327-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92327-150">NOTES</span></span>

## <span data-ttu-id="92327-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92327-151">RELATED LINKS</span></span>

[<span data-ttu-id="92327-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="92327-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="92327-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="92327-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="92327-154">Nowe — AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="92327-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
