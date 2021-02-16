---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: b38108a9655378349efff44bae3e51efc3ce1f7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186802"
---
# <span data-ttu-id="e369e-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e369e-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="e369e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e369e-102">SYNOPSIS</span></span>
<span data-ttu-id="e369e-103">Aktualizuje skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="e369e-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="e369e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e369e-104">SYNTAX</span></span>

### <span data-ttu-id="e369e-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e369e-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e369e-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e369e-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e369e-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e369e-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e369e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e369e-108">DESCRIPTION</span></span>
<span data-ttu-id="e369e-109">Polecenie **cmdlet Update-AzVpnGateway** aktualizuje skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="e369e-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="e369e-110">Brama Azure VPN to zdefiniowana przez oprogramowanie łączność witryny z witryną w aplikacji VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e369e-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="e369e-111">Ta brama zmienia rozmiar i skaluje na podstawie jednostki skali określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e369e-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="e369e-112">Połączenie można skonfigurować z gałęzi/witryny sieci VPN do skalowalnej bramy.</span><span class="sxs-lookup"><span data-stu-id="e369e-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="e369e-113">Każde połączenie składa się z 2 Active-Active i podkołowych</span><span class="sxs-lookup"><span data-stu-id="e369e-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="e369e-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e369e-114">EXAMPLES</span></span>

### <span data-ttu-id="e369e-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e369e-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="e369e-116">Powyższe spowoduje utworzenie grupy zasobów, Wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e369e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e369e-117">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="e369e-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e369e-118">Po utworzeniu bramy brama używa Update-AzVpnGateway do uaktualnienia bramy do 3 jednostek skali.</span><span class="sxs-lookup"><span data-stu-id="e369e-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="e369e-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e369e-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="e369e-120">Powyższe spowoduje utworzenie grupy zasobów, Wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e369e-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e369e-121">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="e369e-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e369e-122">Po utworzeniu bramy używa ona Set-AzVpnGateway BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="e369e-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="e369e-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e369e-123">PARAMETERS</span></span>

### <span data-ttu-id="e369e-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e369e-124">-AsJob</span></span>
<span data-ttu-id="e369e-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e369e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e369e-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e369e-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="e369e-127">Adresy komunikacji równorzędnej BGP dla tego elementu bgpsettings usługi VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e369e-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e369e-128">-DefaultProfile</span></span>
<span data-ttu-id="e369e-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e369e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e369e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e369e-130">-InputObject</span></span>
<span data-ttu-id="e369e-131">Obiekt bramy sieci vpn, który ma zostać zmodyfikowany</span><span class="sxs-lookup"><span data-stu-id="e369e-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e369e-132">-Name</span></span>
<span data-ttu-id="e369e-133">Nazwa bramy sieci vpn.</span><span class="sxs-lookup"><span data-stu-id="e369e-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e369e-134">-ResourceGroupName</span></span>
<span data-ttu-id="e369e-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e369e-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e369e-136">-ResourceId</span></span>
<span data-ttu-id="e369e-137">Identyfikator zasobu Azure w usłudze VpnGateway do modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="e369e-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-138">— Tag</span><span class="sxs-lookup"><span data-stu-id="e369e-138">-Tag</span></span>
<span data-ttu-id="e369e-139">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e369e-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-140">— VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e369e-140">-VpnConnection</span></span>
<span data-ttu-id="e369e-141">Lista połączeń VpnConnections, które musi mieć ta aplikacja VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e369e-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="e369e-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="e369e-143">Lista elementów VpnGatewayNatRules skojarzonych z tą bramą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e369e-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="e369e-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e369e-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="e369e-145">Jednostka skali dla tej aplikacji VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e369e-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369e-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e369e-146">-Confirm</span></span>
<span data-ttu-id="e369e-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e369e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e369e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e369e-148">-WhatIf</span></span>
<span data-ttu-id="e369e-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e369e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e369e-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e369e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e369e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e369e-151">CommonParameters</span></span>
<span data-ttu-id="e369e-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e369e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e369e-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e369e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e369e-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e369e-154">INPUTS</span></span>

### <span data-ttu-id="e369e-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e369e-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="e369e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="e369e-156">System.String</span></span>

## <span data-ttu-id="e369e-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e369e-157">OUTPUTS</span></span>

### <span data-ttu-id="e369e-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e369e-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="e369e-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e369e-159">NOTES</span></span>

## <span data-ttu-id="e369e-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e369e-160">RELATED LINKS</span></span>

[<span data-ttu-id="e369e-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e369e-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="e369e-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e369e-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="e369e-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e369e-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)