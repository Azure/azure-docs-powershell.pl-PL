---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717382"
---
# <span data-ttu-id="12fce-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fce-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="12fce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12fce-102">SYNOPSIS</span></span>
<span data-ttu-id="12fce-103">Update-AzureRmVpnGateway aktualizuje skalowalną bramę VPN do odpowiedniego stanu celu.</span><span class="sxs-lookup"><span data-stu-id="12fce-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12fce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12fce-104">SYNTAX</span></span>

### <span data-ttu-id="12fce-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12fce-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fce-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="12fce-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fce-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="12fce-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fce-108">Opis</span><span class="sxs-lookup"><span data-stu-id="12fce-108">DESCRIPTION</span></span>
<span data-ttu-id="12fce-109">Update-AzureRmVpnGateway aktualizuje skalowalną bramę VPN do odpowiedniego stanu celu.</span><span class="sxs-lookup"><span data-stu-id="12fce-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="12fce-110">AzureRmVpnGateway to programowana łączność między witrynami w ramach VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="12fce-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="12fce-111">Ta brama zmienia rozmiar i skaluje się na podstawie jednostki skali określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="12fce-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="12fce-112">Połączenie można skonfigurować z poziomu filii/witryny nazywanej VPNSite do bramy skalowalnej.</span><span class="sxs-lookup"><span data-stu-id="12fce-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="12fce-113">Każde połączenie składa się z 2 Active-Active tuneli</span><span class="sxs-lookup"><span data-stu-id="12fce-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="12fce-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12fce-114">EXAMPLES</span></span>

### <span data-ttu-id="12fce-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12fce-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="12fce-116">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="12fce-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="12fce-117">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="12fce-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="12fce-118">Po utworzeniu bramy używa Set-AzureRmVpnGateway, aby uaktualnić bramę do 3 jednostek skali.</span><span class="sxs-lookup"><span data-stu-id="12fce-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="12fce-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12fce-119">PARAMETERS</span></span>

### <span data-ttu-id="12fce-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12fce-120">-AsJob</span></span>
<span data-ttu-id="12fce-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="12fce-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12fce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fce-122">-DefaultProfile</span></span>
<span data-ttu-id="12fce-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12fce-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fce-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12fce-124">-InputObject</span></span>
<span data-ttu-id="12fce-125">Obiekt bramy sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="12fce-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="12fce-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12fce-126">-Name</span></span>
<span data-ttu-id="12fce-127">Nazwa wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="12fce-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="12fce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fce-128">-ResourceGroupName</span></span>
<span data-ttu-id="12fce-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12fce-129">The resource group name.</span></span>

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

### <span data-ttu-id="12fce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12fce-130">-ResourceId</span></span>
<span data-ttu-id="12fce-131">Identyfikator zasobu platformy Azure VpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="12fce-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="12fce-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="12fce-132">-Tag</span></span>
<span data-ttu-id="12fce-133">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="12fce-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="12fce-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="12fce-134">-VpnConnection</span></span>
<span data-ttu-id="12fce-135">Lista VpnConnections, które ta VpnGateway musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="12fce-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="12fce-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="12fce-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="12fce-137">Jednostka skali dla tego VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="12fce-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="12fce-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12fce-138">-Confirm</span></span>
<span data-ttu-id="12fce-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fce-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12fce-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fce-140">-WhatIf</span></span>
<span data-ttu-id="12fce-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fce-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fce-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12fce-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12fce-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fce-143">CommonParameters</span></span>
<span data-ttu-id="12fce-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fce-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fce-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fce-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fce-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12fce-146">INPUTS</span></span>

### <span data-ttu-id="12fce-147">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fce-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="12fce-148">System. String</span><span class="sxs-lookup"><span data-stu-id="12fce-148">System.String</span></span>

## <span data-ttu-id="12fce-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12fce-149">OUTPUTS</span></span>

### <span data-ttu-id="12fce-150">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fce-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="12fce-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12fce-151">NOTES</span></span>

## <span data-ttu-id="12fce-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12fce-152">RELATED LINKS</span></span>
