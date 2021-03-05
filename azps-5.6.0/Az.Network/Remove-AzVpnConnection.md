---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 5b728195c34db0261bd27525f0916c634cf3d9e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003546"
---
# <span data-ttu-id="f25b4-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f25b4-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="f25b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f25b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f25b4-103">Usuwa połączenie VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="f25b4-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="f25b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f25b4-104">SYNTAX</span></span>

### <span data-ttu-id="f25b4-105">ByVpnConnectionName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f25b4-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f25b4-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f25b4-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f25b4-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f25b4-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f25b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f25b4-108">DESCRIPTION</span></span>
<span data-ttu-id="f25b4-109">Usuwa połączenie VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="f25b4-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="f25b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f25b4-110">EXAMPLES</span></span>

### <span data-ttu-id="f25b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f25b4-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="f25b4-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f25b4-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f25b4-113">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="f25b4-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f25b4-114">Po utworzeniu brama jest połączona z lokacją VpnSite za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="f25b4-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="f25b4-115">Następnie usuwa połączenie za pomocą nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="f25b4-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="f25b4-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f25b4-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="f25b4-117">Taki sam jak w przykładzie 1, ale teraz usuwa połączenie przy użyciu obiektu potokowego z Get-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="f25b4-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="f25b4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f25b4-118">PARAMETERS</span></span>

### <span data-ttu-id="f25b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25b4-119">-DefaultProfile</span></span>
<span data-ttu-id="f25b4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f25b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f25b4-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f25b4-121">-Force</span></span>
<span data-ttu-id="f25b4-122">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="f25b4-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f25b4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f25b4-123">-InputObject</span></span>
<span data-ttu-id="f25b4-124">Obiekt VpnConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f25b4-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f25b4-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f25b4-125">-Name</span></span>
<span data-ttu-id="f25b4-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f25b4-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25b4-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f25b4-127">-ParentResourceName</span></span>
<span data-ttu-id="f25b4-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f25b4-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25b4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f25b4-129">-PassThru</span></span>
<span data-ttu-id="f25b4-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f25b4-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f25b4-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f25b4-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f25b4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25b4-132">-ResourceGroupName</span></span>
<span data-ttu-id="f25b4-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f25b4-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25b4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f25b4-134">-ResourceId</span></span>
<span data-ttu-id="f25b4-135">Identyfikator zasobu obiektu VpnConnection do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f25b4-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f25b4-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f25b4-136">-Confirm</span></span>
<span data-ttu-id="f25b4-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f25b4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f25b4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f25b4-138">-WhatIf</span></span>
<span data-ttu-id="f25b4-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f25b4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f25b4-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f25b4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f25b4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25b4-141">CommonParameters</span></span>
<span data-ttu-id="f25b4-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25b4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25b4-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f25b4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25b4-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f25b4-144">INPUTS</span></span>

### <span data-ttu-id="f25b4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f25b4-145">System.String</span></span>

### <span data-ttu-id="f25b4-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f25b4-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="f25b4-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f25b4-147">OUTPUTS</span></span>

### <span data-ttu-id="f25b4-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f25b4-148">System.Boolean</span></span>

## <span data-ttu-id="f25b4-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f25b4-149">NOTES</span></span>

## <span data-ttu-id="f25b4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f25b4-150">RELATED LINKS</span></span>

[<span data-ttu-id="f25b4-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f25b4-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="f25b4-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f25b4-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="f25b4-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f25b4-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
