---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
ms.openlocfilehash: 106e924913af3df113f81c75bf2fa44bc4ee8b5c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189938"
---
# <span data-ttu-id="cb1cc-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cb1cc-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="cb1cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1cc-103">Odłączanie połączonych połączeń klienta vpn za pomocą owej bramy sieci vpn p2s</span><span class="sxs-lookup"><span data-stu-id="cb1cc-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="cb1cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb1cc-104">SYNTAX</span></span>

### <span data-ttu-id="cb1cc-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cb1cc-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="cb1cc-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cb1cc-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="cb1cc-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cb1cc-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="cb1cc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb1cc-108">DESCRIPTION</span></span>
<span data-ttu-id="cb1cc-109">Polecenie cmdlet **Disconnect-AzP2sVpnGatewayVpnConnection** umożliwia odłączenie od aplikacji P2SVpnGateway bieżącego punktu połączenia z witryną.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="cb1cc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb1cc-110">EXAMPLES</span></span>

### <span data-ttu-id="cb1cc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb1cc-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="cb1cc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb1cc-112">PARAMETERS</span></span>

### <span data-ttu-id="cb1cc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb1cc-113">-InputObject</span></span>
<span data-ttu-id="cb1cc-114">Obiekt bramy sieci vpn p2s do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="cb1cc-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1cc-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cb1cc-115">-Name</span></span>
<span data-ttu-id="cb1cc-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1cc-117">- VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="cb1cc-117">-VpnConnectionId</span></span>
<span data-ttu-id="cb1cc-118">Vpn Connection Ida</span><span class="sxs-lookup"><span data-stu-id="cb1cc-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb1cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb1cc-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1cc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb1cc-121">-ResourceId</span></span>
<span data-ttu-id="cb1cc-122">Identyfikator zasobu wirtualnej bramy sieciowej P2s</span><span class="sxs-lookup"><span data-stu-id="cb1cc-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1cc-123">CommonParameters</span></span>
<span data-ttu-id="cb1cc-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1cc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb1cc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1cc-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb1cc-126">INPUTS</span></span>

### <span data-ttu-id="cb1cc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cb1cc-127">System.String</span></span>

## <span data-ttu-id="cb1cc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb1cc-128">OUTPUTS</span></span>

### <span data-ttu-id="cb1cc-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cb1cc-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="cb1cc-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb1cc-130">NOTES</span></span>

## <span data-ttu-id="cb1cc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb1cc-131">RELATED LINKS</span></span>
