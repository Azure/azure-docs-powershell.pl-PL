---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 0d7bec7a40ced6ddcd5ffc61f48f233cea115459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009466"
---
# <span data-ttu-id="97161-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="97161-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="97161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97161-102">SYNOPSIS</span></span>
<span data-ttu-id="97161-103">Pobiera zasób ExpressRouteGateway przy użyciu nazw ResourceGroupName i GatewayName LUB wyświetla listę wszystkich bram według nazwy ResourceGroupName lub SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="97161-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="97161-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97161-104">SYNTAX</span></span>

### <span data-ttu-id="97161-105">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="97161-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97161-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97161-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97161-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="97161-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97161-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="97161-108">DESCRIPTION</span></span>
<span data-ttu-id="97161-109">Pobiera zasób ExpressRouteGateway przy użyciu nazw ResourceGroupName i GatewayName LUB wyświetla listę wszystkich bram według nazwy ResourceGroupName lub SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="97161-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="97161-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97161-110">EXAMPLES</span></span>

### <span data-ttu-id="97161-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97161-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="97161-112">Powyższe spowoduje utworzenie grupy zasobów, Virtual WAN, Virtual Network, Virtual Hub w West Central US w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="97161-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="97161-113">Brama usługi ExpressRoute zostanie utworzona w centrum wirtualnym z 2 jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="97161-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="97161-114">Następnie pobiera ona bramę ExpressRouteGateway przy użyciu nazwy grupy zasobów i nazwy bramy.</span><span class="sxs-lookup"><span data-stu-id="97161-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="97161-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="97161-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="97161-116">To polecenie spowoduje, że wszystkie przejścia w uście ExpressRouteGateway, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="97161-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="97161-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97161-117">PARAMETERS</span></span>

### <span data-ttu-id="97161-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97161-118">-DefaultProfile</span></span>
<span data-ttu-id="97161-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97161-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97161-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97161-120">-Name</span></span>
<span data-ttu-id="97161-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="97161-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="97161-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97161-122">-ResourceGroupName</span></span>
<span data-ttu-id="97161-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97161-123">The resource group name.</span></span>

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

### <span data-ttu-id="97161-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97161-124">-ResourceId</span></span>
<span data-ttu-id="97161-125">Identyfikator zasobu Azure dla usługi expressRouteGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="97161-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97161-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97161-126">CommonParameters</span></span>
<span data-ttu-id="97161-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97161-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97161-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97161-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97161-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97161-129">INPUTS</span></span>

### <span data-ttu-id="97161-130">System.String</span><span class="sxs-lookup"><span data-stu-id="97161-130">System.String</span></span>

## <span data-ttu-id="97161-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97161-131">OUTPUTS</span></span>

### <span data-ttu-id="97161-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="97161-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="97161-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97161-133">NOTES</span></span>

## <span data-ttu-id="97161-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97161-134">RELATED LINKS</span></span>
