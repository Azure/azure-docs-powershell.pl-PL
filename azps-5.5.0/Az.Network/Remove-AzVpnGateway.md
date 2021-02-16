---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191682"
---
# <span data-ttu-id="54fa1-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="54fa1-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="54fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="54fa1-103">Polecenie Remove-AzVpnGateway cmdlet usuwa bramę azure VPN.</span><span class="sxs-lookup"><span data-stu-id="54fa1-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="54fa1-104">Jest to brama specyficzna dla łączności zdefiniowanej przez oprogramowanie Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="54fa1-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="54fa1-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54fa1-105">SYNTAX</span></span>

### <span data-ttu-id="54fa1-106">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="54fa1-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fa1-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="54fa1-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fa1-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="54fa1-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fa1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="54fa1-109">DESCRIPTION</span></span>
<span data-ttu-id="54fa1-110">Polecenie Remove-AzVpnGateway cmdlet usuwa bramę azure VPN.</span><span class="sxs-lookup"><span data-stu-id="54fa1-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="54fa1-111">Jest to brama specyficzna dla łączności zdefiniowanej przez oprogramowanie Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="54fa1-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="54fa1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54fa1-112">EXAMPLES</span></span>

### <span data-ttu-id="54fa1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54fa1-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="54fa1-114">W tym przykładzie jest grupę zasobów ( Wirtualna sieć WAN, wirtualne centrum — skalowalna brama VPN) w centrum Stanów Zjednoczonych, a następnie natychmiast ją usuwa.</span><span class="sxs-lookup"><span data-stu-id="54fa1-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="54fa1-115">Aby pominąć monit podczas usuwania bramy wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="54fa1-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="54fa1-116">Spowoduje to usunięcie dołączonej do niej aplikacji VpnGateway i wszystkich połączonych z nim połączeń VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="54fa1-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="54fa1-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="54fa1-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="54fa1-118">W tym przykładzie jest grupę zasobów ( Wirtualna sieć WAN, wirtualne centrum — skalowalna brama VPN) w centrum Stanów Zjednoczonych, a następnie natychmiast ją usuwa.</span><span class="sxs-lookup"><span data-stu-id="54fa1-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="54fa1-119">To usunięcie odbywa się za pomocą połączenia rurowego programu PowerShell, które korzysta z obiektu VpnGateway zwróconego przez Get-AzVpnGateway połączenia.</span><span class="sxs-lookup"><span data-stu-id="54fa1-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="54fa1-120">Aby pominąć monit podczas usuwania bramy wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="54fa1-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="54fa1-121">Spowoduje to usunięcie dołączonej do niej aplikacji VpnGateway i wszystkich połączonych z nim połączeń VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="54fa1-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="54fa1-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54fa1-122">PARAMETERS</span></span>

### <span data-ttu-id="54fa1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fa1-123">-DefaultProfile</span></span>
<span data-ttu-id="54fa1-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54fa1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54fa1-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="54fa1-125">-Force</span></span>
<span data-ttu-id="54fa1-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="54fa1-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="54fa1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54fa1-127">-InputObject</span></span>
<span data-ttu-id="54fa1-128">Obiekt vpnGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="54fa1-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="54fa1-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="54fa1-129">-Name</span></span>
<span data-ttu-id="54fa1-130">Nazwa vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="54fa1-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fa1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54fa1-131">-PassThru</span></span>
<span data-ttu-id="54fa1-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="54fa1-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54fa1-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="54fa1-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54fa1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fa1-134">-ResourceGroupName</span></span>
<span data-ttu-id="54fa1-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54fa1-135">The resource group name.</span></span>

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

### <span data-ttu-id="54fa1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54fa1-136">-ResourceId</span></span>
<span data-ttu-id="54fa1-137">Identyfikator zasobu Azure dla usługi vpnGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="54fa1-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa1-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54fa1-138">-Confirm</span></span>
<span data-ttu-id="54fa1-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="54fa1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fa1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fa1-140">-WhatIf</span></span>
<span data-ttu-id="54fa1-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54fa1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fa1-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="54fa1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fa1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fa1-143">CommonParameters</span></span>
<span data-ttu-id="54fa1-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54fa1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fa1-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fa1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fa1-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54fa1-146">INPUTS</span></span>

### <span data-ttu-id="54fa1-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="54fa1-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="54fa1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="54fa1-148">System.String</span></span>

## <span data-ttu-id="54fa1-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54fa1-149">OUTPUTS</span></span>

### <span data-ttu-id="54fa1-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54fa1-150">System.Boolean</span></span>

## <span data-ttu-id="54fa1-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54fa1-151">NOTES</span></span>

## <span data-ttu-id="54fa1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54fa1-152">RELATED LINKS</span></span>

[<span data-ttu-id="54fa1-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="54fa1-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="54fa1-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="54fa1-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="54fa1-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="54fa1-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
