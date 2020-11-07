---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 46b3c223cebd59d155747b70196288f344a54c6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871139"
---
# <span data-ttu-id="5c46e-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c46e-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="5c46e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c46e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c46e-103">Usuwa VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5c46e-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="5c46e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c46e-104">SYNTAX</span></span>

### <span data-ttu-id="5c46e-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c46e-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c46e-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="5c46e-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c46e-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="5c46e-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c46e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5c46e-108">DESCRIPTION</span></span>
<span data-ttu-id="5c46e-109">Usuwa VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5c46e-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="5c46e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c46e-110">EXAMPLES</span></span>

### <span data-ttu-id="5c46e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c46e-111">Example 1</span></span>
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

<span data-ttu-id="5c46e-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5c46e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5c46e-113">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="5c46e-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5c46e-114">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5c46e-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="5c46e-115">Następnie połączenie zostanie usunięte za pomocą nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="5c46e-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="5c46e-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5c46e-116">Example 2</span></span>

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

<span data-ttu-id="5c46e-117">Taki sam jak przykład 1, ale teraz usuwa połączenie przy użyciu obiektu potokowego z polecenia Get-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5c46e-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="5c46e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c46e-118">PARAMETERS</span></span>

### <span data-ttu-id="5c46e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c46e-119">-DefaultProfile</span></span>
<span data-ttu-id="5c46e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c46e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c46e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5c46e-121">-Force</span></span>
<span data-ttu-id="5c46e-122">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="5c46e-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c46e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5c46e-123">-InputObject</span></span>
<span data-ttu-id="5c46e-124">Obiekt VpnConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="5c46e-124">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="5c46e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c46e-125">-Name</span></span>
<span data-ttu-id="5c46e-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c46e-126">The resource name.</span></span>

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

### <span data-ttu-id="5c46e-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5c46e-127">-ParentResourceName</span></span>
<span data-ttu-id="5c46e-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="5c46e-128">The parent resource name.</span></span>

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

### <span data-ttu-id="5c46e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c46e-129">-PassThru</span></span>
<span data-ttu-id="5c46e-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5c46e-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c46e-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5c46e-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c46e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c46e-132">-ResourceGroupName</span></span>
<span data-ttu-id="5c46e-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c46e-133">The resource group name.</span></span>

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

### <span data-ttu-id="5c46e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c46e-134">-ResourceId</span></span>
<span data-ttu-id="5c46e-135">Identyfikator zasobu obiektu VpnConnection, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5c46e-135">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="5c46e-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c46e-136">-Confirm</span></span>
<span data-ttu-id="5c46e-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c46e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c46e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c46e-138">-WhatIf</span></span>
<span data-ttu-id="5c46e-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c46e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c46e-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c46e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c46e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c46e-141">CommonParameters</span></span>
<span data-ttu-id="5c46e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c46e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c46e-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c46e-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c46e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c46e-144">INPUTS</span></span>

### <span data-ttu-id="5c46e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5c46e-145">System.String</span></span>

### <span data-ttu-id="5c46e-146">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c46e-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="5c46e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c46e-147">OUTPUTS</span></span>

### <span data-ttu-id="5c46e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c46e-148">System.Boolean</span></span>

## <span data-ttu-id="5c46e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c46e-149">NOTES</span></span>

## <span data-ttu-id="5c46e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c46e-150">RELATED LINKS</span></span>

[<span data-ttu-id="5c46e-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c46e-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="5c46e-152">Nowe — AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c46e-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="5c46e-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c46e-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
