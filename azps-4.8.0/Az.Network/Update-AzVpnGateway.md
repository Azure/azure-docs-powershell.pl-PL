---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223015"
---
# <span data-ttu-id="168d6-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="168d6-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="168d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="168d6-102">SYNOPSIS</span></span>
<span data-ttu-id="168d6-103">Aktualizacja skalowalnej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="168d6-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="168d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="168d6-104">SYNTAX</span></span>

### <span data-ttu-id="168d6-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="168d6-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="168d6-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="168d6-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="168d6-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="168d6-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="168d6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="168d6-108">DESCRIPTION</span></span>
<span data-ttu-id="168d6-109">Polecenie cmdlet **Update-AzVpnGateway** umożliwia zaktualizowanie skalowalnej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="168d6-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="168d6-110">Brama sieci VPN platformy Azure to zdefiniowana w oprogramowaniu łączność z połączeniami z witrynami w VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="168d6-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="168d6-111">Ta brama zmienia rozmiar i skaluje się na podstawie jednostki skali określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="168d6-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="168d6-112">Połączenie można skonfigurować z poziomu gałęzi/witryny nazywanej witryną sieci VPN dla bramy skalowalnej.</span><span class="sxs-lookup"><span data-stu-id="168d6-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="168d6-113">Każde połączenie składa się z 2 Active-Active tuneli</span><span class="sxs-lookup"><span data-stu-id="168d6-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="168d6-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="168d6-114">EXAMPLES</span></span>

### <span data-ttu-id="168d6-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="168d6-115">Example 1</span></span>

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

<span data-ttu-id="168d6-116">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="168d6-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="168d6-117">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="168d6-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="168d6-118">Po utworzeniu bramy używa Update-AzVpnGateway, aby uaktualnić bramę do 3 jednostek skali.</span><span class="sxs-lookup"><span data-stu-id="168d6-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="168d6-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="168d6-119">Example 2</span></span>

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

<span data-ttu-id="168d6-120">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="168d6-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="168d6-121">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="168d6-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="168d6-122">Po utworzeniu bramy Użyj Set-AzVpnGateway, aby zaktualizować BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="168d6-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="168d6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="168d6-123">PARAMETERS</span></span>

### <span data-ttu-id="168d6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="168d6-124">-AsJob</span></span>
<span data-ttu-id="168d6-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="168d6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="168d6-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="168d6-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="168d6-127">Adresy równorzędne BGP dla tego VpnGateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="168d6-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="168d6-128">-Confirm</span></span>
<span data-ttu-id="168d6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="168d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168d6-130">-DefaultProfile</span></span>
<span data-ttu-id="168d6-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="168d6-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="168d6-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="168d6-132">-InputObject</span></span>
<span data-ttu-id="168d6-133">Obiekt bramy sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="168d6-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="168d6-134">-Name</span></span>
<span data-ttu-id="168d6-135">Nazwa bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="168d6-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168d6-136">-ResourceGroupName</span></span>
<span data-ttu-id="168d6-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="168d6-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="168d6-138">-ResourceId</span></span>
<span data-ttu-id="168d6-139">Identyfikator zasobu platformy Azure VpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="168d6-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="168d6-140">-Tag</span></span>
<span data-ttu-id="168d6-141">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="168d6-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="168d6-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="168d6-142">-VpnConnection</span></span>
<span data-ttu-id="168d6-143">Lista VpnConnections, które ta VpnGateway musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="168d6-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="168d6-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="168d6-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="168d6-145">Jednostka skali dla tego VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="168d6-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="168d6-146">-WhatIf</span></span>
<span data-ttu-id="168d6-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="168d6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="168d6-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="168d6-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168d6-149">CommonParameters</span></span>
<span data-ttu-id="168d6-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168d6-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="168d6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168d6-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="168d6-152">INPUTS</span></span>

### <span data-ttu-id="168d6-153">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="168d6-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="168d6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="168d6-154">System.String</span></span>

## <span data-ttu-id="168d6-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="168d6-155">OUTPUTS</span></span>

### <span data-ttu-id="168d6-156">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="168d6-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="168d6-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="168d6-157">NOTES</span></span>

## <span data-ttu-id="168d6-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="168d6-158">RELATED LINKS</span></span>
[<span data-ttu-id="168d6-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="168d6-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="168d6-160">Nowe — AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="168d6-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="168d6-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="168d6-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)