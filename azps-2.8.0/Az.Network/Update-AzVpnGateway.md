---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 306bd7262347219afac3ec94ad59dafef579ff94
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872040"
---
# <span data-ttu-id="3a8f2-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8f2-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="3a8f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8f2-103">Aktualizacja skalowalnej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="3a8f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a8f2-104">SYNTAX</span></span>

### <span data-ttu-id="3a8f2-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a8f2-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8f2-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3a8f2-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8f2-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8f2-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a8f2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3a8f2-108">DESCRIPTION</span></span>
<span data-ttu-id="3a8f2-109">Polecenie cmdlet **Update-AzVpnGateway** umożliwia zaktualizowanie skalowalnej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="3a8f2-110">Brama sieci VPN platformy Azure to zdefiniowana w oprogramowaniu łączność z połączeniami z witrynami w VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="3a8f2-111">Ta brama zmienia rozmiar i skaluje się na podstawie jednostki skali określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="3a8f2-112">Połączenie można skonfigurować z poziomu gałęzi/witryny nazywanej witryną sieci VPN dla bramy skalowalnej.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="3a8f2-113">Każde połączenie składa się z 2 Active-Active tuneli</span><span class="sxs-lookup"><span data-stu-id="3a8f2-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="3a8f2-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a8f2-114">EXAMPLES</span></span>

### <span data-ttu-id="3a8f2-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a8f2-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="3a8f2-116">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="3a8f2-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3a8f2-117">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3a8f2-118">Po utworzeniu bramy używa Set-AzVpnGateway, aby uaktualnić bramę do 3 jednostek skali.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="3a8f2-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a8f2-119">PARAMETERS</span></span>

### <span data-ttu-id="3a8f2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a8f2-120">-AsJob</span></span>
<span data-ttu-id="3a8f2-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3a8f2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a8f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8f2-122">-DefaultProfile</span></span>
<span data-ttu-id="3a8f2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a8f2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a8f2-124">-InputObject</span></span>
<span data-ttu-id="3a8f2-125">Obiekt bramy sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="3a8f2-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="3a8f2-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a8f2-126">-Name</span></span>
<span data-ttu-id="3a8f2-127">Nazwa wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="3a8f2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8f2-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a8f2-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-129">The resource group name.</span></span>

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

### <span data-ttu-id="3a8f2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8f2-130">-ResourceId</span></span>
<span data-ttu-id="3a8f2-131">Identyfikator zasobu platformy Azure VpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="3a8f2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a8f2-132">-Tag</span></span>
<span data-ttu-id="3a8f2-133">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3a8f2-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3a8f2-134">-VpnConnection</span></span>
<span data-ttu-id="3a8f2-135">Lista VpnConnections, które ta VpnGateway musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="3a8f2-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="3a8f2-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="3a8f2-137">Jednostka skali dla tego VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="3a8f2-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a8f2-138">-Confirm</span></span>
<span data-ttu-id="3a8f2-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8f2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8f2-140">-WhatIf</span></span>
<span data-ttu-id="3a8f2-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8f2-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8f2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8f2-143">CommonParameters</span></span>
<span data-ttu-id="3a8f2-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8f2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8f2-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a8f2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8f2-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a8f2-146">INPUTS</span></span>

### <span data-ttu-id="3a8f2-147">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8f2-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="3a8f2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3a8f2-148">System.String</span></span>

## <span data-ttu-id="3a8f2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a8f2-149">OUTPUTS</span></span>

### <span data-ttu-id="3a8f2-150">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8f2-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="3a8f2-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a8f2-151">NOTES</span></span>

## <span data-ttu-id="3a8f2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a8f2-152">RELATED LINKS</span></span>

[<span data-ttu-id="3a8f2-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8f2-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="3a8f2-154">Nowe — AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8f2-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="3a8f2-155">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8f2-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
