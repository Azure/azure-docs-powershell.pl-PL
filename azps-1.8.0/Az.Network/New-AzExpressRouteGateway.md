---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 6aabba5154e14f3af0ccfff20569c0cdc51a2578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709315"
---
# <span data-ttu-id="89f77-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="89f77-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="89f77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89f77-102">SYNOPSIS</span></span>
<span data-ttu-id="89f77-103">Tworzy skalowalną bramę ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="89f77-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="89f77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89f77-104">SYNTAX</span></span>

### <span data-ttu-id="89f77-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89f77-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f77-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="89f77-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f77-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="89f77-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f77-108">Opis</span><span class="sxs-lookup"><span data-stu-id="89f77-108">DESCRIPTION</span></span>

<span data-ttu-id="89f77-109">New-AzExpressRouteGateway tworzy skalowalną bramę ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="89f77-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="89f77-110">Jest to funkcja połączeń z oprogramowaniem na platformie Azure w VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="89f77-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="89f77-111">Tę bramę można skalować na podstawie określonej jednostki skali lub polecenia cmdlet Set-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="89f77-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="89f77-112">Połączenie jest skonfigurowane na podstawie obwodu ExpressRoute lokalnego do bramy skalowalnej.</span><span class="sxs-lookup"><span data-stu-id="89f77-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="89f77-113">ExpressRouteGateway będzie w tym samym miejscu, w którym znajduje się VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="89f77-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="89f77-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89f77-114">EXAMPLES</span></span>

### <span data-ttu-id="89f77-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89f77-115">Example 1</span></span>

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

<span data-ttu-id="89f77-116">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="89f77-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="89f77-117">Brama ExpressRoute zostanie utworzona później w koncentratorze wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="89f77-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="89f77-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89f77-118">PARAMETERS</span></span>

### <span data-ttu-id="89f77-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89f77-119">-AsJob</span></span>
<span data-ttu-id="89f77-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="89f77-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89f77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f77-121">-DefaultProfile</span></span>
<span data-ttu-id="89f77-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89f77-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f77-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="89f77-123">-MaxScaleUnits</span></span>
<span data-ttu-id="89f77-124">Maksymalna liczba jednostek skali dla tego ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="89f77-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="89f77-125">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="89f77-125">Valid range > 2</span></span>

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

### <span data-ttu-id="89f77-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="89f77-126">-MinScaleUnits</span></span>
<span data-ttu-id="89f77-127">Minimalna liczba jednostek skali dla tego ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="89f77-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="89f77-128">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="89f77-128">Valid range > 2</span></span>

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

### <span data-ttu-id="89f77-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89f77-129">-Name</span></span>
<span data-ttu-id="89f77-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="89f77-130">The resource name.</span></span>

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

### <span data-ttu-id="89f77-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f77-131">-ResourceGroupName</span></span>
<span data-ttu-id="89f77-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="89f77-132">The resource name.</span></span>

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

### <span data-ttu-id="89f77-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="89f77-133">-Tag</span></span>
<span data-ttu-id="89f77-134">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="89f77-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="89f77-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="89f77-135">-VirtualHub</span></span>
<span data-ttu-id="89f77-136">VirtualHub, do tego VpnGateway należy skojarzyć.</span><span class="sxs-lookup"><span data-stu-id="89f77-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="89f77-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="89f77-137">-VirtualHubId</span></span>
<span data-ttu-id="89f77-138">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="89f77-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="89f77-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="89f77-139">-VirtualHubName</span></span>
<span data-ttu-id="89f77-140">Identyfikator VirtualHub, do którego należy ten VpnGateway musi być skojarzony.</span><span class="sxs-lookup"><span data-stu-id="89f77-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="89f77-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89f77-141">-Confirm</span></span>
<span data-ttu-id="89f77-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f77-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f77-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f77-143">-WhatIf</span></span>
<span data-ttu-id="89f77-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f77-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f77-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89f77-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f77-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f77-146">CommonParameters</span></span>
<span data-ttu-id="89f77-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f77-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f77-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f77-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f77-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89f77-149">INPUTS</span></span>

### <span data-ttu-id="89f77-150">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89f77-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="89f77-151">System. String</span><span class="sxs-lookup"><span data-stu-id="89f77-151">System.String</span></span>

## <span data-ttu-id="89f77-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89f77-152">OUTPUTS</span></span>

### <span data-ttu-id="89f77-153">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="89f77-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="89f77-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89f77-154">NOTES</span></span>

## <span data-ttu-id="89f77-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89f77-155">RELATED LINKS</span></span>
