---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f5a48ec9ac28e13af7aaa763afe72437bed5fda4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006065"
---
# <span data-ttu-id="96968-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="96968-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="96968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96968-102">SYNOPSIS</span></span>
<span data-ttu-id="96968-103">Polecenie Remove-AzVirtualHubVnetConnection cmdlet usuwa połączenie azure virtual network, które równorzędnie równorzędnie jest zdalną siecią VNET z siecią VNET centrum.</span><span class="sxs-lookup"><span data-stu-id="96968-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="96968-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96968-104">SYNTAX</span></span>

### <span data-ttu-id="96968-105">ByHubVirtualNetworkConnectionName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="96968-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96968-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="96968-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96968-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="96968-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96968-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="96968-108">DESCRIPTION</span></span>
<span data-ttu-id="96968-109">Polecenie Remove-AzVirtualHubVnetConnection cmdlet usuwa połączenie azure virtual network, które równorzędnie równorzędnie jest zdalną siecią VNET z siecią VNET centrum.</span><span class="sxs-lookup"><span data-stu-id="96968-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="96968-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96968-110">EXAMPLES</span></span>

### <span data-ttu-id="96968-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96968-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="96968-112">Powyższe spowoduje utworzenie grupy zasobów, Virtual WAN, Virtual Network, Virtual Hub w centrum centralnym Stanów Zjednoczonych w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="96968-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="96968-113">Po tym czasie zostanie utworzone połączenie sieci wirtualnej, które będzie równorzędne dla sieci wirtualnej z centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="96968-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="96968-114">Po utworzeniu połączenia sieci wirtualnej centrum usuwa ono połączenie z siecią wirtualną centrum, używając nazwy grupy zasobów, nazwy centrum i nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="96968-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="96968-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="96968-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="96968-116">Powyższe spowoduje utworzenie grupy zasobów, Virtual WAN, Virtual Network, Virtual Hub w centrum centralnym Stanów Zjednoczonych w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="96968-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="96968-117">Po tym czasie zostanie utworzone połączenie sieci wirtualnej, które będzie równorzędne dla sieci wirtualnej z centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="96968-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="96968-118">Po utworzeniu połączenia sieci wirtualnej centrum usuwa ono połączenie z siecią wirtualną centrum za pomocą połączeń rurowych programu PowerShell na danych wyjściowych z platformy Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="96968-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="96968-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96968-119">PARAMETERS</span></span>

### <span data-ttu-id="96968-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="96968-120">-AsJob</span></span>
<span data-ttu-id="96968-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="96968-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96968-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96968-122">-DefaultProfile</span></span>
<span data-ttu-id="96968-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="96968-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96968-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="96968-124">-Force</span></span>
<span data-ttu-id="96968-125">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="96968-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="96968-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96968-126">-InputObject</span></span>
<span data-ttu-id="96968-127">Zasób hubvirtualnetworkconnection do modyfikowania.</span><span class="sxs-lookup"><span data-stu-id="96968-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96968-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="96968-128">-Name</span></span>
<span data-ttu-id="96968-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="96968-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96968-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="96968-130">-ParentResourceName</span></span>
<span data-ttu-id="96968-131">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="96968-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96968-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96968-132">-PassThru</span></span>
<span data-ttu-id="96968-133">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="96968-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96968-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="96968-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96968-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96968-135">-ResourceGroupName</span></span>
<span data-ttu-id="96968-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96968-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96968-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96968-137">-ResourceId</span></span>
<span data-ttu-id="96968-138">Identyfikator zasobu hubvirtualnetworkconnection do modyfikowania.</span><span class="sxs-lookup"><span data-stu-id="96968-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96968-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96968-139">-Confirm</span></span>
<span data-ttu-id="96968-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="96968-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96968-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96968-141">-WhatIf</span></span>
<span data-ttu-id="96968-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96968-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96968-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="96968-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96968-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96968-144">CommonParameters</span></span>
<span data-ttu-id="96968-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96968-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96968-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96968-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96968-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96968-147">INPUTS</span></span>

### <span data-ttu-id="96968-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="96968-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="96968-149">System.String</span><span class="sxs-lookup"><span data-stu-id="96968-149">System.String</span></span>

## <span data-ttu-id="96968-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96968-150">OUTPUTS</span></span>

### <span data-ttu-id="96968-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96968-151">System.Boolean</span></span>

## <span data-ttu-id="96968-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96968-152">NOTES</span></span>

## <span data-ttu-id="96968-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96968-153">RELATED LINKS</span></span>

[<span data-ttu-id="96968-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="96968-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="96968-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="96968-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
