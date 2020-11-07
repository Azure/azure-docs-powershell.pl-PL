---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: fa91ce991a109c91b27560b0b969d1af0f4342d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709411"
---
# <span data-ttu-id="46854-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46854-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="46854-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46854-102">SYNOPSIS</span></span>
<span data-ttu-id="46854-103">Pobiera zasób VpnGateway przy użyciu ResourceGroupName i Gatewayname lub wyświetla wszystkie bramy przez ResourceGroupName lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46854-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="46854-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46854-104">SYNTAX</span></span>

### <span data-ttu-id="46854-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="46854-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46854-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46854-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46854-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46854-107">DESCRIPTION</span></span>
<span data-ttu-id="46854-108">Pobiera zasób VpnGateway przy użyciu ResourceGroupName i Gatewayname lub wyświetla wszystkie bramy przez ResourceGroupName lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46854-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="46854-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46854-109">EXAMPLES</span></span>

### <span data-ttu-id="46854-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46854-110">Example 1</span></span>

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
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="46854-111">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="46854-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="46854-112">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="46854-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="46854-113">Następnie pobiera VpnGateway przy użyciu jego resourceGroupName i nazwy bramy.</span><span class="sxs-lookup"><span data-stu-id="46854-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="46854-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="46854-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="46854-115">To polecenie cmdlet umożliwia pobieranie wszystkich bram, które zaczynają się od "test".</span><span class="sxs-lookup"><span data-stu-id="46854-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="46854-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46854-116">PARAMETERS</span></span>

### <span data-ttu-id="46854-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46854-117">-DefaultProfile</span></span>
<span data-ttu-id="46854-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46854-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46854-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46854-119">-Name</span></span>
<span data-ttu-id="46854-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="46854-120">The resource name.</span></span>

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

### <span data-ttu-id="46854-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46854-121">-ResourceGroupName</span></span>
<span data-ttu-id="46854-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46854-122">The resource group name.</span></span>

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

### <span data-ttu-id="46854-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46854-123">CommonParameters</span></span>
<span data-ttu-id="46854-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46854-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46854-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46854-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46854-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46854-126">INPUTS</span></span>

### <span data-ttu-id="46854-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="46854-127">None</span></span>

## <span data-ttu-id="46854-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46854-128">OUTPUTS</span></span>

### <span data-ttu-id="46854-129">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46854-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="46854-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46854-130">NOTES</span></span>

## <span data-ttu-id="46854-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46854-131">RELATED LINKS</span></span>

[<span data-ttu-id="46854-132">Nowe — AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46854-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="46854-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46854-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="46854-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46854-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)