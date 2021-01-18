---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500685"
---
# <span data-ttu-id="d12aa-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d12aa-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="d12aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d12aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d12aa-103">Pobiera zasób ExpressRouteGateway przy użyciu ResourceGroupName i Gatewayname lub wyświetla wszystkie bramy przez ResourceGroupName lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d12aa-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="d12aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d12aa-104">SYNTAX</span></span>

### <span data-ttu-id="d12aa-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d12aa-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12aa-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12aa-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12aa-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d12aa-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12aa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d12aa-108">DESCRIPTION</span></span>
<span data-ttu-id="d12aa-109">Pobiera zasób ExpressRouteGateway przy użyciu ResourceGroupName i Gatewayname lub wyświetla wszystkie bramy przez ResourceGroupName lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d12aa-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="d12aa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d12aa-110">EXAMPLES</span></span>

### <span data-ttu-id="d12aa-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d12aa-111">Example 1</span></span>

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

<span data-ttu-id="d12aa-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych w ramach grupy zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d12aa-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d12aa-113">Brama ExpressRoute zostanie utworzona później w koncentratorze wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="d12aa-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d12aa-114">Następnie pobiera ExpressRouteGateway przy użyciu jego resourceGroupName i nazwy bramy.</span><span class="sxs-lookup"><span data-stu-id="d12aa-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="d12aa-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d12aa-115">Example 2</span></span>

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

<span data-ttu-id="d12aa-116">To polecenie otrzyma wszystkie ExpressRouteGateways, których rozpoczęcie rozpoczyna się od tekstu "test"</span><span class="sxs-lookup"><span data-stu-id="d12aa-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="d12aa-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d12aa-117">PARAMETERS</span></span>

### <span data-ttu-id="d12aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12aa-118">-DefaultProfile</span></span>
<span data-ttu-id="d12aa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d12aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d12aa-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d12aa-120">-Name</span></span>
<span data-ttu-id="d12aa-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d12aa-121">The resource name.</span></span>

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

### <span data-ttu-id="d12aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="d12aa-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d12aa-123">The resource group name.</span></span>

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

### <span data-ttu-id="d12aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d12aa-124">-ResourceId</span></span>
<span data-ttu-id="d12aa-125">Identyfikator zasobu platformy Azure dla expressRouteGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d12aa-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="d12aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12aa-126">CommonParameters</span></span>
<span data-ttu-id="d12aa-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12aa-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d12aa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12aa-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d12aa-129">INPUTS</span></span>

### <span data-ttu-id="d12aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d12aa-130">System.String</span></span>

## <span data-ttu-id="d12aa-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d12aa-131">OUTPUTS</span></span>

### <span data-ttu-id="d12aa-132">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d12aa-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="d12aa-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d12aa-133">NOTES</span></span>

## <span data-ttu-id="d12aa-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d12aa-134">RELATED LINKS</span></span>
