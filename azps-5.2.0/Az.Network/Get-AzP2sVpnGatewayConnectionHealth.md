---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354910"
---
# <span data-ttu-id="32463-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="32463-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="32463-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32463-102">SYNOPSIS</span></span>
<span data-ttu-id="32463-103">Pobiera bieżący aggregared informacji o kondycji połączeń witryny z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="32463-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="32463-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32463-104">SYNTAX</span></span>

### <span data-ttu-id="32463-105">ByP2SVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="32463-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32463-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="32463-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32463-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="32463-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32463-108">Opis</span><span class="sxs-lookup"><span data-stu-id="32463-108">DESCRIPTION</span></span>
<span data-ttu-id="32463-109">Polecenie cmdlet **Get-AzP2sVpnGatewayConnectionHealth** umożliwia uzyskiwanie aktualnego zagregowanego poziomu kondycji połączeń witryny z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="32463-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="32463-110">Zagregowane kondycja przedstawia liczbę punktów wskazujących klientów witryn połączonych z P2SVpnGateway, całkowite bajty wejściowe i wyjściowe przekazywane przez P2SVpnGateway i przydzielone adresy IP dla połączeń z klientami witryny.</span><span class="sxs-lookup"><span data-stu-id="32463-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="32463-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32463-111">EXAMPLES</span></span>

### <span data-ttu-id="32463-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32463-112">Example 1</span></span>
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

<span data-ttu-id="32463-113">Polecenie cmdlet **Get-AzP2sVpnGatewayConnectionHealth** umożliwia uzyskiwanie aktualnego zagregowanego poziomu kondycji połączeń witryny z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="32463-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="32463-114">Powyższe polecenie Zezwalaj na kondycję wyjściową wskazuje, że liczba wskazujących klientów witryny połączonych z P2SVpnGateway to 2.</span><span class="sxs-lookup"><span data-stu-id="32463-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="32463-115">Całkowite bajty wejściowe i wyjściowe przenoszone przez P2SVpnGateway są odpowiednio 100 i 200.</span><span class="sxs-lookup"><span data-stu-id="32463-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="32463-116">Przydzielone adresy IP dla połączeń wskazują klientom witryny "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="32463-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="32463-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32463-117">PARAMETERS</span></span>

### <span data-ttu-id="32463-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32463-118">-DefaultProfile</span></span>
<span data-ttu-id="32463-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32463-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32463-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32463-120">-InputObject</span></span>
<span data-ttu-id="32463-121">Obiekt bramy sieci VPN P2S, który ma zostać zmodyfikowany</span><span class="sxs-lookup"><span data-stu-id="32463-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="32463-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="32463-122">-Name</span></span>
<span data-ttu-id="32463-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="32463-123">The resource name.</span></span>

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

### <span data-ttu-id="32463-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32463-124">-ResourceGroupName</span></span>
<span data-ttu-id="32463-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32463-125">The resource group name.</span></span>

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

### <span data-ttu-id="32463-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32463-126">-ResourceId</span></span>
<span data-ttu-id="32463-127">Identyfikator zasobu platformy Azure P2SVpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="32463-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="32463-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32463-128">CommonParameters</span></span>
<span data-ttu-id="32463-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32463-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32463-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32463-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32463-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32463-131">INPUTS</span></span>

### <span data-ttu-id="32463-132">System. String</span><span class="sxs-lookup"><span data-stu-id="32463-132">System.String</span></span>
<span data-ttu-id="32463-133">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="32463-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="32463-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32463-134">OUTPUTS</span></span>

### <span data-ttu-id="32463-135">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="32463-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="32463-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32463-136">NOTES</span></span>

## <span data-ttu-id="32463-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32463-137">RELATED LINKS</span></span>
