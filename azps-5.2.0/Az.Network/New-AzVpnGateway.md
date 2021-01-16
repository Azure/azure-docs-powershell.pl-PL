---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345154"
---
# <span data-ttu-id="1a923-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1a923-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="1a923-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a923-102">SYNOPSIS</span></span>
<span data-ttu-id="1a923-103">Umożliwia utworzenie skalowalnej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="1a923-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="1a923-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a923-104">SYNTAX</span></span>

### <span data-ttu-id="1a923-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a923-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a923-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="1a923-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a923-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="1a923-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a923-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1a923-108">DESCRIPTION</span></span>

<span data-ttu-id="1a923-109">New-AzVpnGateway tworzy skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="1a923-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="1a923-110">Jest to programowa łączność między oprogramowaniem na potrzeby połączeń z witrynami w VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="1a923-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="1a923-111">Ta brama zmienia rozmiar i skaluje się na podstawie jednostki skali określonej w tym lub Set-AzVpnGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a923-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="1a923-112">Połączenie jest konfigurowane na podstawie filii/witryny nazywanej VPNSite do bramy skalowalnej.</span><span class="sxs-lookup"><span data-stu-id="1a923-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="1a923-113">Każde połączenie składa się z 2 Active-Active tuneli.</span><span class="sxs-lookup"><span data-stu-id="1a923-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="1a923-114">VpnGateway będzie w tym samym miejscu, w którym znajduje się VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="1a923-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="1a923-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a923-115">EXAMPLES</span></span>

### <span data-ttu-id="1a923-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a923-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="1a923-117">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="1a923-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1a923-118">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="1a923-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="1a923-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a923-119">PARAMETERS</span></span>

### <span data-ttu-id="1a923-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a923-120">-AsJob</span></span>
<span data-ttu-id="1a923-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1a923-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a923-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a923-122">-DefaultProfile</span></span>
<span data-ttu-id="1a923-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a923-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a923-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a923-124">-Name</span></span>
<span data-ttu-id="1a923-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1a923-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a923-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a923-126">-ResourceGroupName</span></span>
<span data-ttu-id="1a923-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1a923-127">The resource name.</span></span>

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

### <span data-ttu-id="1a923-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a923-128">-Tag</span></span>
<span data-ttu-id="1a923-129">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a923-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1a923-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="1a923-130">-VirtualHub</span></span>
<span data-ttu-id="1a923-131">VirtualHub, do tego VpnGateway należy skojarzyć.</span><span class="sxs-lookup"><span data-stu-id="1a923-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a923-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="1a923-132">-VirtualHubId</span></span>
<span data-ttu-id="1a923-133">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="1a923-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a923-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="1a923-134">-VirtualHubName</span></span>
<span data-ttu-id="1a923-135">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="1a923-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a923-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1a923-136">-VpnConnection</span></span>
<span data-ttu-id="1a923-137">Lista VpnConnections, które ta VpnGateway musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="1a923-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="1a923-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1a923-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="1a923-139">Jednostka skali dla tego VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="1a923-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a923-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a923-140">-Confirm</span></span>
<span data-ttu-id="1a923-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a923-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a923-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a923-142">-WhatIf</span></span>
<span data-ttu-id="1a923-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a923-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a923-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a923-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a923-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a923-145">CommonParameters</span></span>
<span data-ttu-id="1a923-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a923-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a923-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a923-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a923-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a923-148">INPUTS</span></span>

### <span data-ttu-id="1a923-149">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1a923-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="1a923-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1a923-150">System.String</span></span>

## <span data-ttu-id="1a923-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a923-151">OUTPUTS</span></span>

### <span data-ttu-id="1a923-152">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1a923-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="1a923-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a923-153">NOTES</span></span>

## <span data-ttu-id="1a923-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a923-154">RELATED LINKS</span></span>

[<span data-ttu-id="1a923-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1a923-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="1a923-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1a923-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="1a923-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1a923-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
