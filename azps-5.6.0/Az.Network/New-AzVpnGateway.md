---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984376"
---
# <span data-ttu-id="e35d0-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e35d0-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="e35d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e35d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e35d0-103">Tworzy skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="e35d0-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="e35d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e35d0-104">SYNTAX</span></span>

### <span data-ttu-id="e35d0-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e35d0-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e35d0-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e35d0-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e35d0-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e35d0-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e35d0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e35d0-108">DESCRIPTION</span></span>
<span data-ttu-id="e35d0-109">New-AzVpnGateway tworzy skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="e35d0-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="e35d0-110">Jest to zdefiniowana programowo łączność między witrynami w aplikacji VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e35d0-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="e35d0-111">Ta brama zmienia rozmiar i skale na podstawie jednostki skali określonej w tym lub Set-AzVpnGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e35d0-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="e35d0-112">Połączenie jest ustawiane z gałęzi/witryny nazywanej witryną VPN do skalowalnej bramy.</span><span class="sxs-lookup"><span data-stu-id="e35d0-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="e35d0-113">Każde połączenie składa się z 2 Active-Active i podkołowych.</span><span class="sxs-lookup"><span data-stu-id="e35d0-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="e35d0-114">Aplikacja VpnGateway będzie w tej samej lokalizacji co aplikacja VirtualHub, do których się odwołujesz.</span><span class="sxs-lookup"><span data-stu-id="e35d0-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="e35d0-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e35d0-115">EXAMPLES</span></span>

### <span data-ttu-id="e35d0-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e35d0-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="e35d0-117">Powyższe spowoduje utworzenie grupy zasobów, Wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e35d0-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e35d0-118">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="e35d0-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="e35d0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e35d0-119">PARAMETERS</span></span>

### <span data-ttu-id="e35d0-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e35d0-120">-AsJob</span></span>
<span data-ttu-id="e35d0-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e35d0-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35d0-122">-DefaultProfile</span></span>
<span data-ttu-id="e35d0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e35d0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e35d0-124">-Name</span></span>
<span data-ttu-id="e35d0-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e35d0-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="e35d0-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e35d0-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="e35d0-128">-Tag</span></span>
<span data-ttu-id="e35d0-129">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e35d0-129">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-130">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e35d0-130">-VirtualHub</span></span>
<span data-ttu-id="e35d0-131">Z tą bramą VpnGateway musi być skojarzona aplikacja VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e35d0-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-132">- VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="e35d0-132">-VirtualHubId</span></span>
<span data-ttu-id="e35d0-133">Identyfikator aplikacji VirtualHub, z tą bramą VpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="e35d0-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-134">- VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="e35d0-134">-VirtualHubName</span></span>
<span data-ttu-id="e35d0-135">Identyfikator aplikacji VirtualHub, z tą bramą VpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="e35d0-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-136">— VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e35d0-136">-VpnConnection</span></span>
<span data-ttu-id="e35d0-137">Lista połączeń VpnConnections, które musi mieć ta aplikacja VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e35d0-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="e35d0-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="e35d0-139">Lista elementów VpnGatewayNatRules skojarzonych z tą bramą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e35d0-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e35d0-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="e35d0-141">Jednostka skali dla tej aplikacji VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e35d0-141">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d0-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="e35d0-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="e35d0-143">Oflaguj to enable Routing Preference Internet on this VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e35d0-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="e35d0-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e35d0-144">-Confirm</span></span>
<span data-ttu-id="e35d0-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e35d0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e35d0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35d0-146">-WhatIf</span></span>
<span data-ttu-id="e35d0-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e35d0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35d0-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e35d0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e35d0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35d0-149">CommonParameters</span></span>
<span data-ttu-id="e35d0-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35d0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35d0-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e35d0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35d0-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35d0-152">INPUTS</span></span>

### <span data-ttu-id="e35d0-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e35d0-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="e35d0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="e35d0-154">System.String</span></span>
## <span data-ttu-id="e35d0-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35d0-155">OUTPUTS</span></span>

### <span data-ttu-id="e35d0-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e35d0-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="e35d0-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e35d0-157">NOTES</span></span>

## <span data-ttu-id="e35d0-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e35d0-158">RELATED LINKS</span></span>

[<span data-ttu-id="e35d0-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e35d0-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="e35d0-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e35d0-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="e35d0-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e35d0-161">Update-AzVpnGateway</span></span>]()

