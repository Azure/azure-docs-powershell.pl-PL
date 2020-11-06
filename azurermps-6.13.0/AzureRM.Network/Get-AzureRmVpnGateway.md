---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543715"
---
# <span data-ttu-id="fcac2-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcac2-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="fcac2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcac2-102">SYNOPSIS</span></span>
<span data-ttu-id="fcac2-103">Pobiera zasób VpnGateway przy użyciu ResourceGroupName i Gatewayname lub wyświetla wszystkie bramy przez ResourceGroupName lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fcac2-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcac2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcac2-104">SYNTAX</span></span>

### <span data-ttu-id="fcac2-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fcac2-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcac2-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcac2-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcac2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fcac2-107">DESCRIPTION</span></span>
<span data-ttu-id="fcac2-108">Pobiera zasób VpnGateway przy użyciu ResourceGroupName i Gatewayname lub wyświetla wszystkie bramy przez ResourceGroupName lub Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fcac2-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="fcac2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcac2-109">EXAMPLES</span></span>

### <span data-ttu-id="fcac2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fcac2-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

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

<span data-ttu-id="fcac2-111">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="fcac2-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fcac2-112">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="fcac2-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fcac2-113">Następnie pobiera VpnGateway przy użyciu jego resourceGroupName i nazwy bramy.</span><span class="sxs-lookup"><span data-stu-id="fcac2-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="fcac2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcac2-114">PARAMETERS</span></span>

### <span data-ttu-id="fcac2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcac2-115">-DefaultProfile</span></span>
<span data-ttu-id="fcac2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcac2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcac2-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fcac2-117">-Name</span></span>
<span data-ttu-id="fcac2-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fcac2-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcac2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcac2-119">-ResourceGroupName</span></span>
<span data-ttu-id="fcac2-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fcac2-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcac2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcac2-121">CommonParameters</span></span>
<span data-ttu-id="fcac2-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcac2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcac2-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcac2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcac2-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcac2-124">INPUTS</span></span>

### <span data-ttu-id="fcac2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fcac2-125">System.String</span></span>

## <span data-ttu-id="fcac2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcac2-126">OUTPUTS</span></span>

### <span data-ttu-id="fcac2-127">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fcac2-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="fcac2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcac2-128">NOTES</span></span>

## <span data-ttu-id="fcac2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcac2-129">RELATED LINKS</span></span>
