---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063289"
---
# <span data-ttu-id="8d19b-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d19b-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8d19b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d19b-102">SYNOPSIS</span></span>
<span data-ttu-id="8d19b-103">Ustawia parametry protokołu IPsec sieci VPN dla istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d19b-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="8d19b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d19b-104">SYNTAX</span></span>

### <span data-ttu-id="8d19b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d19b-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d19b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8d19b-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d19b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d19b-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d19b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8d19b-108">DESCRIPTION</span></span>
<span data-ttu-id="8d19b-109">Polecenie cmdlet **Set-AzVpnClientIpsecParameter** ustawia parametry protokołu IPsec sieci VPN dla istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d19b-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="8d19b-110">Po utworzeniu bramy sieci wirtualnej ustawia ona zestaw domyślnych zasad IPSec sieci VPN w bramie.</span><span class="sxs-lookup"><span data-stu-id="8d19b-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="8d19b-111">W przypadku wskazywania, że użytkownik witryny chce użyć pewnych niestandardowych zasad IPSec do łączenia się z bramą VPN, użytkownik musi najpierw ustawić zasady IPSec w bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="8d19b-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="8d19b-112">**Set-AzVpnClientIpsecParameter** umożliwia wykonanie tej czynności.</span><span class="sxs-lookup"><span data-stu-id="8d19b-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="8d19b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d19b-113">EXAMPLES</span></span>

### <span data-ttu-id="8d19b-114">Przykład 1: ustawia niestandardową zasadę IPSec sieci VPN na istniejącą bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d19b-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="8d19b-115">W tym przykładzie ustawiono niestandardowe zasady IPSec sieci VPN do istniejącej bramy sieci wirtualnej o nazwie ContosoVirtualGateway z grupy zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8d19b-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="8d19b-116">Polecenie cmdlet New-AzVpnClientIpsecParameter służy do tworzenia obiektu parametry IPsec sieci VPN z użyciem wartości przekazanych jeden lub wszystkie parametry, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w obszarze zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d19b-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="8d19b-117">Ten obiekt VpnClientIPsecParameters został przekazany do polecenia Set-AzVpnClientIpsecParameter w celu ustawienia określonych zasad niestandardowych IPSec VPN w bramie sieci wirtualnej, jak pokazano na przykładzie powyżej.</span><span class="sxs-lookup"><span data-stu-id="8d19b-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="8d19b-118">To polecenie zwraca obiekt VpnClientIPsecParameters, w którym pokazano parametry Set.</span><span class="sxs-lookup"><span data-stu-id="8d19b-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="8d19b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d19b-119">PARAMETERS</span></span>

### <span data-ttu-id="8d19b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d19b-120">-DefaultProfile</span></span>
<span data-ttu-id="8d19b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d19b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d19b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d19b-122">-InputObject</span></span>
<span data-ttu-id="8d19b-123">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8d19b-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d19b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d19b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d19b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d19b-125">The resource group name.</span></span>

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

### <span data-ttu-id="8d19b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d19b-126">-ResourceId</span></span>
<span data-ttu-id="8d19b-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d19b-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d19b-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8d19b-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8d19b-129">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d19b-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="8d19b-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d19b-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="8d19b-131">Parametry protokołu IPSec klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="8d19b-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="8d19b-132">Ta wartość parametru może być konstruowana za pomocą polecenia PS Let: New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d19b-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d19b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d19b-133">-Confirm</span></span>
<span data-ttu-id="8d19b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d19b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d19b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d19b-135">-WhatIf</span></span>
<span data-ttu-id="8d19b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d19b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d19b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d19b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d19b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d19b-138">CommonParameters</span></span>
<span data-ttu-id="8d19b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d19b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d19b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d19b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d19b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d19b-141">INPUTS</span></span>

### <span data-ttu-id="8d19b-142">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8d19b-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="8d19b-143">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8d19b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8d19b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8d19b-144">System.String</span></span>

## <span data-ttu-id="8d19b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d19b-145">OUTPUTS</span></span>

### <span data-ttu-id="8d19b-146">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8d19b-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8d19b-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d19b-147">NOTES</span></span>

## <span data-ttu-id="8d19b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d19b-148">RELATED LINKS</span></span>

[<span data-ttu-id="8d19b-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d19b-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8d19b-150">Nowe — AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d19b-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8d19b-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8d19b-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
