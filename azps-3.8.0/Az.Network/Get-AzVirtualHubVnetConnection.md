---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1f04b47889f334f095c8c3163bc601a3b1950c82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052246"
---
# <span data-ttu-id="a405f-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a405f-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="a405f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a405f-102">SYNOPSIS</span></span>
<span data-ttu-id="a405f-103">Pobiera wirtualne połączenie sieciowe w wirtualnym koncentratorze lub zawiera listę wszystkich wirtualnych połączeń sieciowych w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="a405f-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="a405f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a405f-104">SYNTAX</span></span>

### <span data-ttu-id="a405f-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a405f-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a405f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a405f-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a405f-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a405f-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a405f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a405f-108">DESCRIPTION</span></span>
<span data-ttu-id="a405f-109">Pobiera wirtualne połączenie sieciowe w wirtualnym koncentratorze lub zawiera listę wszystkich wirtualnych połączeń sieciowych w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="a405f-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="a405f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a405f-110">EXAMPLES</span></span>

### <span data-ttu-id="a405f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a405f-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="a405f-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a405f-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="a405f-113">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a405f-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="a405f-114">Po utworzeniu połączenia z siecią wirtualną centralą zostanie wykorzystana wirtualna sieć centralnego połączenia z siecią, na której znajduje się nazwa grupy zasobów, nazwa centrum i nazwa połączenia.</span><span class="sxs-lookup"><span data-stu-id="a405f-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="a405f-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a405f-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="a405f-116">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a405f-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="a405f-117">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a405f-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="a405f-118">Po utworzeniu połączenia z siecią wirtualną centralą jest wyświetlane wszystkie wirtualne połączenie sieciowe z centrum, w którym jest używana nazwa grupy zasobów i nazwa centrum.</span><span class="sxs-lookup"><span data-stu-id="a405f-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="a405f-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a405f-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="a405f-120">To polecenie cmdlet wyświetla listę wszystkich wirtualnych połączeń sieciowych, rozpoczynając od "test" przy użyciu nazwy grupy zasobów i nazwy centrum.</span><span class="sxs-lookup"><span data-stu-id="a405f-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="a405f-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a405f-121">PARAMETERS</span></span>

### <span data-ttu-id="a405f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a405f-122">-DefaultProfile</span></span>
<span data-ttu-id="a405f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a405f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a405f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a405f-124">-Name</span></span>
<span data-ttu-id="a405f-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a405f-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a405f-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a405f-126">-ParentObject</span></span>
<span data-ttu-id="a405f-127">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="a405f-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a405f-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a405f-128">-ParentResourceId</span></span>
<span data-ttu-id="a405f-129">Identyfikator zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="a405f-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a405f-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a405f-130">-ParentResourceName</span></span>
<span data-ttu-id="a405f-131">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="a405f-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a405f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a405f-132">-ResourceGroupName</span></span>
<span data-ttu-id="a405f-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a405f-133">The resource group name.</span></span>

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

### <span data-ttu-id="a405f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a405f-134">CommonParameters</span></span>
<span data-ttu-id="a405f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a405f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a405f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a405f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a405f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a405f-137">INPUTS</span></span>

### <span data-ttu-id="a405f-138">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a405f-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="a405f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a405f-139">System.String</span></span>

## <span data-ttu-id="a405f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a405f-140">OUTPUTS</span></span>

### <span data-ttu-id="a405f-141">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="a405f-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="a405f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a405f-142">NOTES</span></span>

## <span data-ttu-id="a405f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a405f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a405f-144">Nowe — AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a405f-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="a405f-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a405f-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
