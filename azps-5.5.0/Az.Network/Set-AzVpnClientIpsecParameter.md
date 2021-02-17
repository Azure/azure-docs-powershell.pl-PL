---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202415"
---
# <span data-ttu-id="05baa-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="05baa-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="05baa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05baa-102">SYNOPSIS</span></span>
<span data-ttu-id="05baa-103">Ustawia parametry ipsec połączenia vpn dla istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="05baa-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="05baa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05baa-104">SYNTAX</span></span>

### <span data-ttu-id="05baa-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="05baa-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05baa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="05baa-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05baa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05baa-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05baa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="05baa-108">DESCRIPTION</span></span>
<span data-ttu-id="05baa-109">Polecenie **cmdlet Set-AzVpnClientIpsecParameters** ustawia parametry ipsec połączenia vpn dla istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="05baa-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="05baa-110">Podczas tworzenia wirtualnej bramy sieciowej ustawia ona zestaw domyślnych zasad ipsec sieci vpn dla bramy.</span><span class="sxs-lookup"><span data-stu-id="05baa-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="05baa-111">Jeśli użytkownik wskaże witrynę chce używać pewnych niestandardowych zasad ipsec do łączenia się z bramą VPN, musi najpierw ustawić te zasady ipsec dla bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="05baa-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="05baa-112">**Set-AzVpnClientIpsecParameters** umożliwia to.</span><span class="sxs-lookup"><span data-stu-id="05baa-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="05baa-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05baa-113">EXAMPLES</span></span>

### <span data-ttu-id="05baa-114">Przykład 1. Ustawia niestandardowe zasady ipsec sieci vpn na istniejącą bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="05baa-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="05baa-115">W tym przykładzie niestandardowa zasada ipsec sieci vpn jest ustawiana na istniejącą wirtualną bramę sieciową o nazwie ContosoVirtualGateway z grupy Zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="05baa-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="05baa-116">New-AzVpnClientIpsecParameter cmdlet służy do tworzenia obiektu parametrów ipsec sieci vpn w celu użycia wartości przekazywanego jednego lub wszystkich parametrów, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w grupie Zasobów.</span><span class="sxs-lookup"><span data-stu-id="05baa-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="05baa-117">Ten utworzony obiekt VpnClientIPsecParameters jest przekazywany do polecenia Set-AzVpnClientIpsecParameter w celu ustawienia określonych niestandardowych zasad ipsec sieci vpn dla wirtualnej bramy sieciowej, jak pokazano w powyższym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="05baa-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="05baa-118">To polecenie zwraca obiekt VpnClientIPsecParameters, który pokazuje ustawione parametry.</span><span class="sxs-lookup"><span data-stu-id="05baa-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="05baa-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05baa-119">PARAMETERS</span></span>

### <span data-ttu-id="05baa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05baa-120">-DefaultProfile</span></span>
<span data-ttu-id="05baa-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="05baa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05baa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05baa-122">-InputObject</span></span>
<span data-ttu-id="05baa-123">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="05baa-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="05baa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05baa-124">-ResourceGroupName</span></span>
<span data-ttu-id="05baa-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05baa-125">The resource group name.</span></span>

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

### <span data-ttu-id="05baa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05baa-126">-ResourceId</span></span>
<span data-ttu-id="05baa-127">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="05baa-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="05baa-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="05baa-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="05baa-129">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="05baa-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="05baa-130">-VpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="05baa-131">Parametry ipsec klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="05baa-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="05baa-132">Tę wartość parametru można utworzyć przy użyciu polecenia PS let:New-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="05baa-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05baa-133">-Confirm</span></span>
<span data-ttu-id="05baa-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05baa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05baa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05baa-135">-WhatIf</span></span>
<span data-ttu-id="05baa-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05baa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05baa-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="05baa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05baa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-138">CommonParameters</span></span>
<span data-ttu-id="05baa-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05baa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05baa-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05baa-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05baa-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05baa-141">INPUTS</span></span>

### <span data-ttu-id="05baa-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="05baa-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05baa-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="05baa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="05baa-144">System.String</span></span>

## <span data-ttu-id="05baa-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05baa-145">OUTPUTS</span></span>

### <span data-ttu-id="05baa-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="05baa-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05baa-147">NOTES</span></span>

## <span data-ttu-id="05baa-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05baa-148">RELATED LINKS</span></span>

[<span data-ttu-id="05baa-149">Get-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="05baa-150">New-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="05baa-151">Remove-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="05baa-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
