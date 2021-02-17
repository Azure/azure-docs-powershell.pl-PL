---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184378"
---
# <span data-ttu-id="a310b-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a310b-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="a310b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a310b-102">SYNOPSIS</span></span>
<span data-ttu-id="a310b-103">Tworzy prywatną usługę linków</span><span class="sxs-lookup"><span data-stu-id="a310b-103">Creates a private link service</span></span>

## <span data-ttu-id="a310b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a310b-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a310b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a310b-105">DESCRIPTION</span></span>
<span data-ttu-id="a310b-106">Polecenie **cmdlet New-AzPrivateLinkService** tworzy prywatną usługę linków</span><span class="sxs-lookup"><span data-stu-id="a310b-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="a310b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a310b-107">EXAMPLES</span></span>

### <span data-ttu-id="a310b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a310b-108">Example 1</span></span>

<span data-ttu-id="a310b-109">W poniższym przykładzie jest podmiot tworzący prywatną usługę linków.</span><span class="sxs-lookup"><span data-stu-id="a310b-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="a310b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a310b-110">PARAMETERS</span></span>

### <span data-ttu-id="a310b-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a310b-111">-AsJob</span></span>
<span data-ttu-id="a310b-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a310b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a310b-113">- AutoApproval</span><span class="sxs-lookup"><span data-stu-id="a310b-113">-AutoApproval</span></span>
<span data-ttu-id="a310b-114">Automatyczne zatwierdzanie subskrypcji usługi linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="a310b-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="a310b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a310b-115">-DefaultProfile</span></span>
<span data-ttu-id="a310b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a310b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a310b-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="a310b-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="a310b-118">Włącz protokół proxy dla prywatnej usługi łączenia.</span><span class="sxs-lookup"><span data-stu-id="a310b-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="a310b-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a310b-119">-Force</span></span>
<span data-ttu-id="a310b-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="a310b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a310b-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a310b-121">-IpConfiguration</span></span>
<span data-ttu-id="a310b-122">Konfiguracje adresów IP</span><span class="sxs-lookup"><span data-stu-id="a310b-122">The ip configurations</span></span>

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

### <span data-ttu-id="a310b-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a310b-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="a310b-124">Konfiguracje frontoronu ip</span><span class="sxs-lookup"><span data-stu-id="a310b-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="a310b-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a310b-125">-Location</span></span>
<span data-ttu-id="a310b-126">.</span><span class="sxs-lookup"><span data-stu-id="a310b-126">location.</span></span>

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

### <span data-ttu-id="a310b-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a310b-127">-Name</span></span>
<span data-ttu-id="a310b-128">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="a310b-128">The name of the service.</span></span>

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

### <span data-ttu-id="a310b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a310b-129">-ResourceGroupName</span></span>
<span data-ttu-id="a310b-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a310b-130">The resource group name.</span></span>

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

### <span data-ttu-id="a310b-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="a310b-131">-Tag</span></span>
<span data-ttu-id="a310b-132">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="a310b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a310b-133">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a310b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a310b-134">— Widoczność</span><span class="sxs-lookup"><span data-stu-id="a310b-134">-Visibility</span></span>
<span data-ttu-id="a310b-135">Subskrypcje widoczności w prywatnej usłudze linku</span><span class="sxs-lookup"><span data-stu-id="a310b-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="a310b-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a310b-136">-Confirm</span></span>
<span data-ttu-id="a310b-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a310b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a310b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a310b-138">-WhatIf</span></span>
<span data-ttu-id="a310b-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a310b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a310b-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a310b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a310b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a310b-141">CommonParameters</span></span>
<span data-ttu-id="a310b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a310b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a310b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a310b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a310b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a310b-144">INPUTS</span></span>

### <span data-ttu-id="a310b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a310b-145">System.String</span></span>

### <span data-ttu-id="a310b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a310b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="a310b-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a310b-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="a310b-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a310b-148">OUTPUTS</span></span>

### <span data-ttu-id="a310b-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a310b-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="a310b-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a310b-150">NOTES</span></span>

## <span data-ttu-id="a310b-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a310b-151">RELATED LINKS</span></span>

[<span data-ttu-id="a310b-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a310b-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="a310b-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a310b-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="a310b-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a310b-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
