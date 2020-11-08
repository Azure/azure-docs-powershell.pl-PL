---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232775"
---
# <span data-ttu-id="f37e2-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f37e2-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f37e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f37e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f37e2-103">Polecenie cmdlet Remove-AzVirtualHubVnetConnection usuwa połączenie wirtualnej sieci Azure, które są równorzędne ze zdalną siecią wirtualną do sieci wirtualnej centrali.</span><span class="sxs-lookup"><span data-stu-id="f37e2-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f37e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f37e2-104">SYNTAX</span></span>

### <span data-ttu-id="f37e2-105">ByHubVirtualNetworkConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f37e2-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f37e2-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f37e2-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f37e2-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f37e2-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f37e2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f37e2-108">DESCRIPTION</span></span>
<span data-ttu-id="f37e2-109">Polecenie cmdlet Remove-AzVirtualHubVnetConnection usuwa połączenie wirtualnej sieci Azure, które są równorzędne ze zdalną siecią wirtualną do sieci wirtualnej centrali.</span><span class="sxs-lookup"><span data-stu-id="f37e2-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f37e2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f37e2-110">EXAMPLES</span></span>

### <span data-ttu-id="f37e2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f37e2-111">Example 1</span></span>

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

<span data-ttu-id="f37e2-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f37e2-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f37e2-113">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f37e2-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f37e2-114">Po utworzeniu połączenia z siecią wirtualną centrum usuwa wirtualne połączenie sieciowe z centrum przy użyciu nazwy grupy zasobów, nazwy centrum i nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="f37e2-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="f37e2-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f37e2-115">Example 2</span></span>

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

<span data-ttu-id="f37e2-116">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f37e2-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f37e2-117">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f37e2-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f37e2-118">Po utworzeniu połączenia z siecią wirtualną centrum usuwa wirtualne połączenie sieciowe z centrum przy użyciu połączeń rurowych programu PowerShell w danych wyjściowych polecenia Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="f37e2-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="f37e2-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f37e2-119">PARAMETERS</span></span>

### <span data-ttu-id="f37e2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f37e2-120">-AsJob</span></span>
<span data-ttu-id="f37e2-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f37e2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f37e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37e2-122">-DefaultProfile</span></span>
<span data-ttu-id="f37e2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f37e2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f37e2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f37e2-124">-Force</span></span>
<span data-ttu-id="f37e2-125">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="f37e2-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f37e2-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f37e2-126">-InputObject</span></span>
<span data-ttu-id="f37e2-127">Zasób hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="f37e2-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f37e2-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f37e2-128">-Name</span></span>
<span data-ttu-id="f37e2-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f37e2-129">The resource name.</span></span>

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

### <span data-ttu-id="f37e2-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f37e2-130">-ParentResourceName</span></span>
<span data-ttu-id="f37e2-131">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f37e2-131">The parent resource name.</span></span>

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

### <span data-ttu-id="f37e2-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f37e2-132">-PassThru</span></span>
<span data-ttu-id="f37e2-133">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f37e2-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f37e2-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f37e2-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f37e2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f37e2-135">-ResourceGroupName</span></span>
<span data-ttu-id="f37e2-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f37e2-136">The resource group name.</span></span>

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

### <span data-ttu-id="f37e2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f37e2-137">-ResourceId</span></span>
<span data-ttu-id="f37e2-138">Identyfikator zasobu zasobu hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="f37e2-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f37e2-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f37e2-139">-Confirm</span></span>
<span data-ttu-id="f37e2-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f37e2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f37e2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f37e2-141">-WhatIf</span></span>
<span data-ttu-id="f37e2-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f37e2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f37e2-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f37e2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f37e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37e2-144">CommonParameters</span></span>
<span data-ttu-id="f37e2-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f37e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37e2-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f37e2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37e2-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f37e2-147">INPUTS</span></span>

### <span data-ttu-id="f37e2-148">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f37e2-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="f37e2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f37e2-149">System.String</span></span>

## <span data-ttu-id="f37e2-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f37e2-150">OUTPUTS</span></span>

### <span data-ttu-id="f37e2-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f37e2-151">System.Boolean</span></span>

## <span data-ttu-id="f37e2-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f37e2-152">NOTES</span></span>

## <span data-ttu-id="f37e2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f37e2-153">RELATED LINKS</span></span>

[<span data-ttu-id="f37e2-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f37e2-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f37e2-155">Nowe — AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f37e2-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
