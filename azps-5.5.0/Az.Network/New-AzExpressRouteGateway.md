---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184514"
---
# <span data-ttu-id="7c96e-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7c96e-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="7c96e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c96e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c96e-103">Tworzy skalowalną bramę usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c96e-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="7c96e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7c96e-104">SYNTAX</span></span>

### <span data-ttu-id="7c96e-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7c96e-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c96e-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7c96e-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c96e-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7c96e-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c96e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7c96e-108">DESCRIPTION</span></span>

<span data-ttu-id="7c96e-109">New-AzExpressRouteGateway tworzy skalowalną bramę usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c96e-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="7c96e-110">Jest to zdefiniowana programowo łączność lokalna z platformą Azure w aplikacji VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7c96e-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="7c96e-111">Tę bramę można skalować na podstawie jednostki skali określonej w tym lub Set-AzExpressRouteGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c96e-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="7c96e-112">Połączenie jest ustawiane z lokalnego obwodu usługi ExpressRoute do skalowalnej bramy.</span><span class="sxs-lookup"><span data-stu-id="7c96e-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="7c96e-113">Brama usługi ExpressRouteGateway będzie w tej samej lokalizacji, w którym znajduje się odwołanie do aplikacji VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7c96e-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="7c96e-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7c96e-114">EXAMPLES</span></span>

### <span data-ttu-id="7c96e-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c96e-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7c96e-116">Powyższe spowoduje utworzenie grupy zasobów, Wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7c96e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7c96e-117">Brama usługi ExpressRoute zostanie utworzona w centrum wirtualnym z 2 jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="7c96e-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="7c96e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c96e-118">PARAMETERS</span></span>

### <span data-ttu-id="7c96e-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7c96e-119">-AsJob</span></span>
<span data-ttu-id="7c96e-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7c96e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c96e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c96e-121">-DefaultProfile</span></span>
<span data-ttu-id="7c96e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c96e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c96e-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7c96e-123">-MaxScaleUnits</span></span>
<span data-ttu-id="7c96e-124">Maksymalna liczba jednostek skalowania dla tej bramy w uchcie expressroute.</span><span class="sxs-lookup"><span data-stu-id="7c96e-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7c96e-125">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="7c96e-125">Valid range > 2</span></span>

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

### <span data-ttu-id="7c96e-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7c96e-126">-MinScaleUnits</span></span>
<span data-ttu-id="7c96e-127">Minimalna liczba jednostek skali dla tej bramy expressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="7c96e-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7c96e-128">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="7c96e-128">Valid range > 2</span></span>

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

### <span data-ttu-id="7c96e-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7c96e-129">-Name</span></span>
<span data-ttu-id="7c96e-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7c96e-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c96e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c96e-131">-ResourceGroupName</span></span>
<span data-ttu-id="7c96e-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7c96e-132">The resource name.</span></span>

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

### <span data-ttu-id="7c96e-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="7c96e-133">-Tag</span></span>
<span data-ttu-id="7c96e-134">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c96e-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7c96e-135">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7c96e-135">-VirtualHub</span></span>
<span data-ttu-id="7c96e-136">Z tą bramą VpnGateway musi być skojarzona aplikacja VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7c96e-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="7c96e-137">- VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="7c96e-137">-VirtualHubId</span></span>
<span data-ttu-id="7c96e-138">Identyfikator aplikacji VirtualHub, z tą bramą VpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="7c96e-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="7c96e-139">- VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="7c96e-139">-VirtualHubName</span></span>
<span data-ttu-id="7c96e-140">Identyfikator aplikacji VirtualHub, z tą bramą VpnGateway, musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="7c96e-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="7c96e-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c96e-141">-Confirm</span></span>
<span data-ttu-id="7c96e-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c96e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c96e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c96e-143">-WhatIf</span></span>
<span data-ttu-id="7c96e-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c96e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c96e-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7c96e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c96e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c96e-146">CommonParameters</span></span>
<span data-ttu-id="7c96e-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c96e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c96e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c96e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c96e-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c96e-149">INPUTS</span></span>

### <span data-ttu-id="7c96e-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7c96e-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7c96e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7c96e-151">System.String</span></span>

## <span data-ttu-id="7c96e-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c96e-152">OUTPUTS</span></span>

### <span data-ttu-id="7c96e-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7c96e-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="7c96e-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7c96e-154">NOTES</span></span>

## <span data-ttu-id="7c96e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c96e-155">RELATED LINKS</span></span>
