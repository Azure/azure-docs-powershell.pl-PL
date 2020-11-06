---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
ms.openlocfilehash: 7f4ba2cf4a57eedea41eccb8d5846129a80414d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543711"
---
# <span data-ttu-id="c0247-101">Get-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c0247-101">Get-AzureRmVpnConnection</span></span>

## <span data-ttu-id="c0247-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0247-102">SYNOPSIS</span></span>
<span data-ttu-id="c0247-103">Pobiera połączenie VPN według nazwy lub wyświetla wszystkie połączenia VPN połączone z VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c0247-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0247-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0247-104">SYNTAX</span></span>

### <span data-ttu-id="c0247-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c0247-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0247-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c0247-106">ByVpnGatewayObject</span></span>
```
Get-AzureRmVpnConnection -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0247-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c0247-107">ByVpnGatewayResourceId</span></span>
```
Get-AzureRmVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0247-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c0247-108">DESCRIPTION</span></span>
<span data-ttu-id="c0247-109">Pobiera połączenie VPN według nazwy lub wyświetla wszystkie połączenia VPN połączone z VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c0247-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="c0247-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0247-110">EXAMPLES</span></span>

### <span data-ttu-id="c0247-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0247-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="c0247-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i VpnSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0247-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c0247-113">Brama sieci VPN zostanie następnie utworzona w centrum wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="c0247-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c0247-114">Po utworzeniu bramy jest ona połączona z VpnSite przy użyciu polecenia New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c0247-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="c0247-115">Następnie zostanie nawiązać połączenie przy użyciu nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="c0247-115">Then it gets the connection using the connection name.</span></span>

## <span data-ttu-id="c0247-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0247-116">PARAMETERS</span></span>

### <span data-ttu-id="c0247-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0247-117">-DefaultProfile</span></span>
<span data-ttu-id="c0247-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0247-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0247-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0247-119">-Name</span></span>
<span data-ttu-id="c0247-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c0247-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0247-121">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="c0247-121">-ParentObject</span></span>
<span data-ttu-id="c0247-122">VpnGateway nadrzędny dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="c0247-122">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="c0247-123">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c0247-123">-ParentResourceId</span></span>
<span data-ttu-id="c0247-124">Identyfikator zasobu dla VpnGateway nadrzędnego dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="c0247-124">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="c0247-125">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c0247-125">-ParentResourceName</span></span>
<span data-ttu-id="c0247-126">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="c0247-126">The parent resource name.</span></span>

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

### <span data-ttu-id="c0247-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0247-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0247-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0247-128">The resource group name.</span></span>

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

### <span data-ttu-id="c0247-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0247-129">CommonParameters</span></span>
<span data-ttu-id="c0247-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0247-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0247-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0247-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0247-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0247-132">INPUTS</span></span>

### <span data-ttu-id="c0247-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c0247-133">System.String</span></span>

## <span data-ttu-id="c0247-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0247-134">OUTPUTS</span></span>

### <span data-ttu-id="c0247-135">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c0247-135">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c0247-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0247-136">NOTES</span></span>

## <span data-ttu-id="c0247-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0247-137">RELATED LINKS</span></span>
