---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191771"
---
# <span data-ttu-id="731d5-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="731d5-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="731d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731d5-102">SYNOPSIS</span></span>
<span data-ttu-id="731d5-103">Usuwa usługę ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="731d5-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="731d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="731d5-104">SYNTAX</span></span>

### <span data-ttu-id="731d5-105">ByExpressRouteConnectionName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="731d5-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731d5-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="731d5-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731d5-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="731d5-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731d5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="731d5-108">DESCRIPTION</span></span>
<span data-ttu-id="731d5-109">Usuwa usługę ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="731d5-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="731d5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="731d5-110">EXAMPLES</span></span>

### <span data-ttu-id="731d5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="731d5-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="731d5-112">Powyższe spowoduje utworzenie grupy zasobów, Wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="731d5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="731d5-113">Brama usługi ExpressRoute zostanie utworzona w centrum wirtualnym z 2 jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="731d5-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="731d5-114">Po utworzeniu brama jest połączona z usługą ExpressRouteSite za pomocą New-AzExpressRouteConnection usługi.</span><span class="sxs-lookup"><span data-stu-id="731d5-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="731d5-115">Następnie usunie połączenie przy użyciu nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="731d5-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="731d5-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="731d5-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="731d5-117">Taki sam jak w przykładzie 1, ale teraz usuwa połączenie przy użyciu obiektu potokowego z get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="731d5-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="731d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="731d5-118">PARAMETERS</span></span>

### <span data-ttu-id="731d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731d5-119">-DefaultProfile</span></span>
<span data-ttu-id="731d5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="731d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="731d5-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="731d5-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="731d5-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="731d5-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731d5-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="731d5-123">-Force</span></span>
<span data-ttu-id="731d5-124">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="731d5-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="731d5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="731d5-125">-InputObject</span></span>
<span data-ttu-id="731d5-126">Obiekt ExpressRouteConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="731d5-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731d5-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="731d5-127">-Name</span></span>
<span data-ttu-id="731d5-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="731d5-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731d5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="731d5-129">-PassThru</span></span>
<span data-ttu-id="731d5-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="731d5-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="731d5-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="731d5-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="731d5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731d5-132">-ResourceGroupName</span></span>
<span data-ttu-id="731d5-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="731d5-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731d5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="731d5-134">-ResourceId</span></span>
<span data-ttu-id="731d5-135">Identyfikator zasobu obiektu ExpressRouteConnection do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="731d5-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731d5-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="731d5-136">-Confirm</span></span>
<span data-ttu-id="731d5-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="731d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731d5-138">-WhatIf</span></span>
<span data-ttu-id="731d5-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="731d5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="731d5-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="731d5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731d5-141">CommonParameters</span></span>
<span data-ttu-id="731d5-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731d5-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731d5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731d5-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="731d5-144">INPUTS</span></span>

### <span data-ttu-id="731d5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="731d5-145">System.String</span></span>

### <span data-ttu-id="731d5-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="731d5-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="731d5-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="731d5-147">OUTPUTS</span></span>

### <span data-ttu-id="731d5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="731d5-148">System.Boolean</span></span>

## <span data-ttu-id="731d5-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="731d5-149">NOTES</span></span>

## <span data-ttu-id="731d5-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="731d5-150">RELATED LINKS</span></span>
