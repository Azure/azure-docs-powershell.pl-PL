---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 1670e8549f561f0b1fae12711303bb3e1ac83280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965697"
---
# <span data-ttu-id="12313-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="12313-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="12313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12313-102">SYNOPSIS</span></span>
<span data-ttu-id="12313-103">Pobiera regułę NAT skojarzoną z usługą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="12313-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="12313-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12313-104">SYNTAX</span></span>

### <span data-ttu-id="12313-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="12313-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12313-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="12313-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12313-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="12313-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12313-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="12313-108">DESCRIPTION</span></span>
<span data-ttu-id="12313-109">Pobiera regułę NAT skojarzoną z usługą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="12313-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="12313-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12313-110">EXAMPLES</span></span>

### <span data-ttu-id="12313-111">Przykład</span><span class="sxs-lookup"><span data-stu-id="12313-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule

```

<span data-ttu-id="12313-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i sieci VpnGateway & regułę NAT skojarzoną z siecią Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="12313-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="12313-113">Następnie reguła NAT uzyskuje przy użyciu nazwy reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="12313-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="12313-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12313-114">PARAMETERS</span></span>

### <span data-ttu-id="12313-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12313-115">-DefaultProfile</span></span>
<span data-ttu-id="12313-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="12313-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12313-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="12313-117">-Name</span></span>
<span data-ttu-id="12313-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="12313-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12313-119">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="12313-119">-ParentObject</span></span>
<span data-ttu-id="12313-120">Nadrzędny element VpnGateway dla tego elementu VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="12313-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12313-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="12313-121">-ParentResourceId</span></span>
<span data-ttu-id="12313-122">Identyfikator zasobu nadrzędnej aplikacji VpnGateway dla tego elementu VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="12313-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12313-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="12313-123">-ParentResourceName</span></span>
<span data-ttu-id="12313-124">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="12313-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12313-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12313-125">-ResourceGroupName</span></span>
<span data-ttu-id="12313-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12313-126">The resource group name.</span></span>

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

### <span data-ttu-id="12313-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12313-127">CommonParameters</span></span>
<span data-ttu-id="12313-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12313-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12313-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12313-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12313-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12313-130">INPUTS</span></span>

### <span data-ttu-id="12313-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12313-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="12313-132">System.String</span><span class="sxs-lookup"><span data-stu-id="12313-132">System.String</span></span>

## <span data-ttu-id="12313-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12313-133">OUTPUTS</span></span>

### <span data-ttu-id="12313-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="12313-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="12313-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12313-135">NOTES</span></span>

## <span data-ttu-id="12313-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12313-136">RELATED LINKS</span></span>
