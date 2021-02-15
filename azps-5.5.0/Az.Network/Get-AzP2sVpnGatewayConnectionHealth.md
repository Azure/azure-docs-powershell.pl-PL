---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193779"
---
# <span data-ttu-id="a25c0-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a25c0-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="a25c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a25c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a25c0-103">Pobiera bieżący, zsumowany punkt na informacje o kondycji połączeń witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a25c0-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="a25c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a25c0-104">SYNTAX</span></span>

### <span data-ttu-id="a25c0-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a25c0-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a25c0-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a25c0-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a25c0-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a25c0-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a25c0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a25c0-108">DESCRIPTION</span></span>
<span data-ttu-id="a25c0-109">Polecenie **cmdlet Get-AzP2sVpnGatewayConnectionHealth** umożliwia uzyskiwanie bieżącej zagregowanej kondycji połączeń witryny z usługi P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a25c0-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="a25c0-110">Zagregowana kondycja pokazuje liczbę punktów klientów witryny połączonych z aplikacją P2SVpnGateway, całkowitą liczbę bajtów punktów przychodzących i wychodzących przesyłanych za pośrednictwem aplikacji P2SVpnGateway i przydzielonych adresów IP do połączonych punktów klientom witryny.</span><span class="sxs-lookup"><span data-stu-id="a25c0-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="a25c0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a25c0-111">EXAMPLES</span></span>

### <span data-ttu-id="a25c0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a25c0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
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

<span data-ttu-id="a25c0-113">Polecenie **cmdlet Get-AzP2sVpnGatewayConnectionHealth** umożliwia uzyskiwanie bieżącej zagregowanej kondycji połączeń witryny z aplikacji P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a25c0-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="a25c0-114">Powyższe polecenie pozwól na kondycję wyników pokazuje, że liczba punktów dla klientów witryny połączonych z aplikacją P2SVpnGateway wynosi 2.</span><span class="sxs-lookup"><span data-stu-id="a25c0-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="a25c0-115">Łączna liczba bajtów ruch wychodzący i wychodzący przetransferowanych przez P2SVpnGateway wynosi odpowiednio 100 i 200.</span><span class="sxs-lookup"><span data-stu-id="a25c0-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="a25c0-116">Adresy IP przypisane do klientów witryny połączonego punktu to :"192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="a25c0-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="a25c0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a25c0-117">PARAMETERS</span></span>

### <span data-ttu-id="a25c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25c0-118">-DefaultProfile</span></span>
<span data-ttu-id="a25c0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a25c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25c0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a25c0-120">-InputObject</span></span>
<span data-ttu-id="a25c0-121">Obiekt bramy sieci vpn p2s do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="a25c0-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a25c0-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a25c0-122">-Name</span></span>
<span data-ttu-id="a25c0-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a25c0-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a25c0-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a25c0-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25c0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a25c0-126">-ResourceId</span></span>
<span data-ttu-id="a25c0-127">Identyfikator zasobu Azure p2SVpnGateway do modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="a25c0-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25c0-128">CommonParameters</span></span>
<span data-ttu-id="a25c0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25c0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25c0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25c0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a25c0-131">INPUTS</span></span>

### <span data-ttu-id="a25c0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a25c0-132">System.String</span></span>
<span data-ttu-id="a25c0-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a25c0-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="a25c0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a25c0-134">OUTPUTS</span></span>

### <span data-ttu-id="a25c0-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a25c0-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="a25c0-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a25c0-136">NOTES</span></span>

## <span data-ttu-id="a25c0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a25c0-137">RELATED LINKS</span></span>
