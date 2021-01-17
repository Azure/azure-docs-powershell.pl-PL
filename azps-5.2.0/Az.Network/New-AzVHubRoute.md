---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330613"
---
# <span data-ttu-id="f5ef2-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f5ef2-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="f5ef2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ef2-103">Tworzy obiekt VHubRoute, który może zostać przekazany jako parametr do polecenia New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="f5ef2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5ef2-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ef2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5ef2-105">DESCRIPTION</span></span>

<span data-ttu-id="f5ef2-106">Tworzy obiekt VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="f5ef2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5ef2-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ef2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5ef2-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="f5ef2-109">Powyższe polecenie utworzy obiekt VHubRoute z opcją Następny skok jako określoną zaporę, którą można następnie dodać do zasobu VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="f5ef2-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f5ef2-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="f5ef2-111">Powyższe polecenie utworzy obiekt VHubRoute, używając skoku, jako określonego hubVnetConnection, który następnie można dodać do zasobu VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="f5ef2-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f5ef2-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="f5ef2-113">Powyższe polecenia otrzymają RoutingConfiguration już istniejący AzVHubRoute, a następnie dodają trasę statyczną w połączeniu.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="f5ef2-114">Możesz również w przypadku, gdy mamy nadzieję, by utworzyć nowe połączenie z trasą statyczną, zapoznaj się z przykładem 1 [.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f5ef2-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="f5ef2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5ef2-115">PARAMETERS</span></span>

### <span data-ttu-id="f5ef2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ef2-116">-DefaultProfile</span></span>
<span data-ttu-id="f5ef2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ef2-118">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="f5ef2-118">-Destination</span></span>
<span data-ttu-id="f5ef2-119">Lista miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-119">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef2-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="f5ef2-120">-DestinationType</span></span>
<span data-ttu-id="f5ef2-121">Typ lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-121">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5ef2-122">-Name</span></span>
<span data-ttu-id="f5ef2-123">Nazwa trasy.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef2-124">-Następny skok</span><span class="sxs-lookup"><span data-stu-id="f5ef2-124">-NextHop</span></span>
<span data-ttu-id="f5ef2-125">Następny przeskok.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-125">The next hop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef2-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f5ef2-126">-NextHopType</span></span>
<span data-ttu-id="f5ef2-127">Typ następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-127">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ef2-128">CommonParameters</span></span>
<span data-ttu-id="f5ef2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ef2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ef2-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5ef2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ef2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5ef2-131">INPUTS</span></span>

### <span data-ttu-id="f5ef2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f5ef2-132">System.String</span></span>

## <span data-ttu-id="f5ef2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5ef2-133">OUTPUTS</span></span>

### <span data-ttu-id="f5ef2-134">Microsoft. Azure. Commands. Network. models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f5ef2-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="f5ef2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5ef2-135">NOTES</span></span>

## <span data-ttu-id="f5ef2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5ef2-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5ef2-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5ef2-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="f5ef2-138">Nowe — AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5ef2-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="f5ef2-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5ef2-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="f5ef2-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5ef2-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)