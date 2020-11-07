---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 16a17ed437194963f3cfd715a6e5364c8f4348c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709079"
---
# <span data-ttu-id="bca44-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bca44-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="bca44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bca44-102">SYNOPSIS</span></span>
<span data-ttu-id="bca44-103">Polecenie cmdlet Remove-AzVirtualHubVnetConnection usuwa połączenie wirtualnej sieci Azure, które są równorzędne ze zdalną siecią wirtualną do sieci wirtualnej centrali.</span><span class="sxs-lookup"><span data-stu-id="bca44-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="bca44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bca44-104">SYNTAX</span></span>

### <span data-ttu-id="bca44-105">ByHubVirtualNetworkConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bca44-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bca44-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="bca44-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bca44-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="bca44-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bca44-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bca44-108">DESCRIPTION</span></span>
<span data-ttu-id="bca44-109">Polecenie cmdlet Remove-AzVirtualHubVnetConnection usuwa połączenie wirtualnej sieci Azure, które są równorzędne ze zdalną siecią wirtualną do sieci wirtualnej centrali.</span><span class="sxs-lookup"><span data-stu-id="bca44-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="bca44-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bca44-110">EXAMPLES</span></span>

### <span data-ttu-id="bca44-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bca44-111">Example 1</span></span>

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

<span data-ttu-id="bca44-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bca44-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="bca44-113">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bca44-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="bca44-114">Po utworzeniu połączenia z siecią wirtualną centrum usuwa wirtualne połączenie sieciowe z centrum przy użyciu nazwy grupy zasobów, nazwy centrum i nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="bca44-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="bca44-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bca44-115">Example 2</span></span>

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

<span data-ttu-id="bca44-116">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="bca44-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="bca44-117">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bca44-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="bca44-118">Po utworzeniu połączenia z siecią wirtualną centrum usuwa wirtualne połączenie sieciowe z centrum przy użyciu połączeń rurowych programu PowerShell w danych wyjściowych polecenia Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="bca44-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="bca44-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bca44-119">PARAMETERS</span></span>

### <span data-ttu-id="bca44-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bca44-120">-AsJob</span></span>
<span data-ttu-id="bca44-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bca44-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bca44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca44-122">-DefaultProfile</span></span>
<span data-ttu-id="bca44-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bca44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca44-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bca44-124">-Force</span></span>
<span data-ttu-id="bca44-125">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="bca44-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bca44-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bca44-126">-InputObject</span></span>
<span data-ttu-id="bca44-127">Zasób hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="bca44-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="bca44-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bca44-128">-Name</span></span>
<span data-ttu-id="bca44-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bca44-129">The resource name.</span></span>

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

### <span data-ttu-id="bca44-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bca44-130">-ParentResourceName</span></span>
<span data-ttu-id="bca44-131">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="bca44-131">The parent resource name.</span></span>

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

### <span data-ttu-id="bca44-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bca44-132">-PassThru</span></span>
<span data-ttu-id="bca44-133">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bca44-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bca44-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bca44-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bca44-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca44-135">-ResourceGroupName</span></span>
<span data-ttu-id="bca44-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bca44-136">The resource group name.</span></span>

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

### <span data-ttu-id="bca44-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bca44-137">-ResourceId</span></span>
<span data-ttu-id="bca44-138">Identyfikator zasobu zasobu hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="bca44-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="bca44-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bca44-139">-Confirm</span></span>
<span data-ttu-id="bca44-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bca44-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bca44-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bca44-141">-WhatIf</span></span>
<span data-ttu-id="bca44-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bca44-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bca44-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bca44-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bca44-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca44-144">CommonParameters</span></span>
<span data-ttu-id="bca44-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca44-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca44-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca44-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca44-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bca44-147">INPUTS</span></span>

### <span data-ttu-id="bca44-148">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="bca44-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="bca44-149">System. String</span><span class="sxs-lookup"><span data-stu-id="bca44-149">System.String</span></span>

## <span data-ttu-id="bca44-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bca44-150">OUTPUTS</span></span>

### <span data-ttu-id="bca44-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bca44-151">System.Boolean</span></span>

## <span data-ttu-id="bca44-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bca44-152">NOTES</span></span>

## <span data-ttu-id="bca44-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bca44-153">RELATED LINKS</span></span>

[<span data-ttu-id="bca44-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bca44-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="bca44-155">Nowe — AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bca44-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
