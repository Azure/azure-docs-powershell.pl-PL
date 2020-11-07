---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869871"
---
# <span data-ttu-id="4d23b-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4d23b-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="4d23b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d23b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d23b-103">Tworzy usługę linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="4d23b-103">Creates a private link service</span></span>

## <span data-ttu-id="4d23b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d23b-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d23b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d23b-105">DESCRIPTION</span></span>
<span data-ttu-id="4d23b-106">Polecenie cmdlet **New-AzPrivateLinkService** tworzy prywatną usługę link.</span><span class="sxs-lookup"><span data-stu-id="4d23b-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="4d23b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d23b-107">EXAMPLES</span></span>

### <span data-ttu-id="4d23b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d23b-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="4d23b-109">W tym przykładzie jest tworzona usługa linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="4d23b-109">This example creates a private link service.</span></span>

## <span data-ttu-id="4d23b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d23b-110">PARAMETERS</span></span>

### <span data-ttu-id="4d23b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d23b-111">-AsJob</span></span>
<span data-ttu-id="4d23b-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4d23b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d23b-113">-Autozatwierdzanie</span><span class="sxs-lookup"><span data-stu-id="4d23b-113">-AutoApproval</span></span>
<span data-ttu-id="4d23b-114">Automatyczne subskrypcje zatwierdzania usługi linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="4d23b-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="4d23b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d23b-115">-DefaultProfile</span></span>
<span data-ttu-id="4d23b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d23b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d23b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d23b-117">-Force</span></span>
<span data-ttu-id="4d23b-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="4d23b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4d23b-119">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d23b-119">-IpConfiguration</span></span>
<span data-ttu-id="4d23b-120">Konfiguracje adresów IP</span><span class="sxs-lookup"><span data-stu-id="4d23b-120">The ip configurations</span></span>

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

### <span data-ttu-id="4d23b-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d23b-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="4d23b-122">Konfiguracje frontonu IP</span><span class="sxs-lookup"><span data-stu-id="4d23b-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="4d23b-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4d23b-123">-Location</span></span>
<span data-ttu-id="4d23b-124">pozycję.</span><span class="sxs-lookup"><span data-stu-id="4d23b-124">location.</span></span>

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

### <span data-ttu-id="4d23b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d23b-125">-Name</span></span>
<span data-ttu-id="4d23b-126">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="4d23b-126">The name of the service.</span></span>

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

### <span data-ttu-id="4d23b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d23b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d23b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d23b-128">The resource group name.</span></span>

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

### <span data-ttu-id="4d23b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d23b-129">-Tag</span></span>
<span data-ttu-id="4d23b-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4d23b-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d23b-131">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4d23b-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d23b-132">-Widoczność</span><span class="sxs-lookup"><span data-stu-id="4d23b-132">-Visibility</span></span>
<span data-ttu-id="4d23b-133">Abonamenty na widoczność prywatnych usług linków</span><span class="sxs-lookup"><span data-stu-id="4d23b-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="4d23b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d23b-134">-Confirm</span></span>
<span data-ttu-id="4d23b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d23b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d23b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d23b-136">-WhatIf</span></span>
<span data-ttu-id="4d23b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d23b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d23b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d23b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d23b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d23b-139">CommonParameters</span></span>
<span data-ttu-id="4d23b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d23b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d23b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d23b-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d23b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d23b-142">INPUTS</span></span>

### <span data-ttu-id="4d23b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4d23b-143">System.String</span></span>

### <span data-ttu-id="4d23b-144">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4d23b-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="4d23b-145">Microsoft. Azure. Commands. Network. models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4d23b-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="4d23b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d23b-146">OUTPUTS</span></span>

### <span data-ttu-id="4d23b-147">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4d23b-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4d23b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d23b-148">NOTES</span></span>

## <span data-ttu-id="4d23b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d23b-149">RELATED LINKS</span></span>

[<span data-ttu-id="4d23b-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4d23b-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="4d23b-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4d23b-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="4d23b-152">Nowe — AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d23b-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
