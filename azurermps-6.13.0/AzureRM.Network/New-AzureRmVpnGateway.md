---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
ms.openlocfilehash: b29b57ea7d7a5182a25cb05ae05e6d1644a5c18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543668"
---
# <span data-ttu-id="b89ee-101">New-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b89ee-101">New-AzureRmVpnGateway</span></span>

## <span data-ttu-id="b89ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b89ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b89ee-103">Umożliwia utworzenie skalowalnej bramy sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="b89ee-103">Creates a Scalable VPN Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b89ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b89ee-104">SYNTAX</span></span>

### <span data-ttu-id="b89ee-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b89ee-105">ByVirtualHubName (Default)</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89ee-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b89ee-106">ByVirtualHubObject</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89ee-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b89ee-107">ByVirtualHubResourceId</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b89ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b89ee-108">DESCRIPTION</span></span>

<span data-ttu-id="b89ee-109">New-AzureRmVpnGateway tworzy skalowalną bramę VPN.</span><span class="sxs-lookup"><span data-stu-id="b89ee-109">New-AzureRmVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="b89ee-110">Jest to programowa łączność między oprogramowaniem na potrzeby połączeń z witrynami w VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b89ee-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="b89ee-111">Ta brama zmienia rozmiar i skaluje się na podstawie jednostki skali określonej w tym lub Set-AzureRmVpnGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89ee-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzureRmVpnGateway cmdlet.</span></span> 

<span data-ttu-id="b89ee-112">Połączenie jest konfigurowane na podstawie filii/witryny nazywanej VPNSite do bramy skalowalnej.</span><span class="sxs-lookup"><span data-stu-id="b89ee-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="b89ee-113">Każde połączenie składa się z 2 Active-Active tuneli.</span><span class="sxs-lookup"><span data-stu-id="b89ee-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="b89ee-114">VpnGateway będzie w tym samym miejscu, w którym znajduje się VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b89ee-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="b89ee-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b89ee-115">EXAMPLES</span></span>

### <span data-ttu-id="b89ee-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b89ee-116">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="b89ee-117">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="b89ee-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b89ee-118">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="b89ee-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="b89ee-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b89ee-119">PARAMETERS</span></span>

### <span data-ttu-id="b89ee-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b89ee-120">-AsJob</span></span>
<span data-ttu-id="b89ee-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b89ee-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b89ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89ee-122">-DefaultProfile</span></span>
<span data-ttu-id="b89ee-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b89ee-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b89ee-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b89ee-124">-Name</span></span>
<span data-ttu-id="b89ee-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b89ee-125">The resource name.</span></span>

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

### <span data-ttu-id="b89ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="b89ee-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b89ee-127">The resource name.</span></span>

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

### <span data-ttu-id="b89ee-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="b89ee-128">-Tag</span></span>
<span data-ttu-id="b89ee-129">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="b89ee-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b89ee-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b89ee-130">-VirtualHub</span></span>
<span data-ttu-id="b89ee-131">VirtualHub, do tego VpnGateway należy skojarzyć.</span><span class="sxs-lookup"><span data-stu-id="b89ee-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="b89ee-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="b89ee-132">-VirtualHubId</span></span>
<span data-ttu-id="b89ee-133">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="b89ee-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="b89ee-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="b89ee-134">-VirtualHubName</span></span>
<span data-ttu-id="b89ee-135">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="b89ee-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="b89ee-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b89ee-136">-VpnConnection</span></span>
<span data-ttu-id="b89ee-137">Lista VpnConnections, które ta VpnGateway musi posiadać.</span><span class="sxs-lookup"><span data-stu-id="b89ee-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="b89ee-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b89ee-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="b89ee-139">Jednostka skali dla tego VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b89ee-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="b89ee-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b89ee-140">-Confirm</span></span>
<span data-ttu-id="b89ee-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89ee-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89ee-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89ee-142">-WhatIf</span></span>
<span data-ttu-id="b89ee-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89ee-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b89ee-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b89ee-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89ee-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89ee-145">CommonParameters</span></span>
<span data-ttu-id="b89ee-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89ee-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89ee-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89ee-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89ee-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b89ee-148">INPUTS</span></span>

### <span data-ttu-id="b89ee-149">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b89ee-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b89ee-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b89ee-150">System.String</span></span>

## <span data-ttu-id="b89ee-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b89ee-151">OUTPUTS</span></span>

### <span data-ttu-id="b89ee-152">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b89ee-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="b89ee-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b89ee-153">NOTES</span></span>

## <span data-ttu-id="b89ee-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b89ee-154">RELATED LINKS</span></span>
