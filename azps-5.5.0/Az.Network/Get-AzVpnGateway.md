---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187098"
---
# <span data-ttu-id="47b93-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47b93-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="47b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b93-102">SYNOPSIS</span></span>
<span data-ttu-id="47b93-103">Pobiera zasób VpnGateway przy użyciu nazw ResourceGroupName i GatewayName OR wyświetla listę wszystkich bram według nazwy ResourceGroupName lub SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="47b93-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="47b93-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47b93-104">SYNTAX</span></span>

### <span data-ttu-id="47b93-105">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="47b93-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b93-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b93-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47b93-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="47b93-107">DESCRIPTION</span></span>
<span data-ttu-id="47b93-108">Pobiera zasób VpnGateway przy użyciu nazw ResourceGroupName i GatewayName OR wyświetla listę wszystkich bram według nazwy ResourceGroupName lub SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="47b93-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="47b93-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47b93-109">EXAMPLES</span></span>

### <span data-ttu-id="47b93-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47b93-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="47b93-111">Powyższe spowoduje utworzenie grupy zasobów, Wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="47b93-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="47b93-112">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="47b93-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="47b93-113">Następnie aplikacja VpnGateway pobiera ją przy użyciu nazwy resourceGroupName i nazwy bramy.</span><span class="sxs-lookup"><span data-stu-id="47b93-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="47b93-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="47b93-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="47b93-115">To polecenie cmdlet pobiera wszystkie bramy, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="47b93-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="47b93-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b93-116">PARAMETERS</span></span>

### <span data-ttu-id="47b93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b93-117">-DefaultProfile</span></span>
<span data-ttu-id="47b93-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47b93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b93-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47b93-119">-Name</span></span>
<span data-ttu-id="47b93-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="47b93-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="47b93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b93-121">-ResourceGroupName</span></span>
<span data-ttu-id="47b93-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47b93-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="47b93-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b93-123">CommonParameters</span></span>
<span data-ttu-id="47b93-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b93-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b93-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47b93-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b93-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47b93-126">INPUTS</span></span>

### <span data-ttu-id="47b93-127">Brak</span><span class="sxs-lookup"><span data-stu-id="47b93-127">None</span></span>

## <span data-ttu-id="47b93-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47b93-128">OUTPUTS</span></span>

### <span data-ttu-id="47b93-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47b93-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="47b93-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47b93-130">NOTES</span></span>

## <span data-ttu-id="47b93-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47b93-131">RELATED LINKS</span></span>

[<span data-ttu-id="47b93-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47b93-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="47b93-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47b93-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="47b93-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="47b93-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
