---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504473"
---
# <span data-ttu-id="cf55c-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf55c-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="cf55c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf55c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf55c-103">Tworzy obiekt RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf55c-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="cf55c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf55c-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf55c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf55c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf55c-106">Tworzy obiekt RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf55c-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="cf55c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf55c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf55c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf55c-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="cf55c-109">Powyższe polecenie utworzy obiekt RoutingConfiguration, który można następnie dodać do zasobu połączenia.</span><span class="sxs-lookup"><span data-stu-id="cf55c-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="cf55c-110">Trasy statyczne są dozwolone tylko w przypadku obiektu HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="cf55c-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="cf55c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf55c-111">PARAMETERS</span></span>

### <span data-ttu-id="cf55c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf55c-112">-DefaultProfile</span></span>
<span data-ttu-id="cf55c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf55c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf55c-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf55c-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="cf55c-115">Tabela tras centrum skojarzona z tą konfiguracją routingu.</span><span class="sxs-lookup"><span data-stu-id="cf55c-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="cf55c-116">-ID</span><span class="sxs-lookup"><span data-stu-id="cf55c-116">-Id</span></span>
<span data-ttu-id="cf55c-117">Lista identyfikatorów zasobów wszystkich tabel tras centrum, które anonsują trasy do właściwości PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="cf55c-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="cf55c-118">-Label</span><span class="sxs-lookup"><span data-stu-id="cf55c-118">-Label</span></span>
<span data-ttu-id="cf55c-119">Lista etykiet dla właściwości PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="cf55c-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf55c-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="cf55c-120">-StaticRoute</span></span>
<span data-ttu-id="cf55c-121">Lista tras sterujących routingiem od VirtualHub do wirtualnego połączenia sieciowego.</span><span class="sxs-lookup"><span data-stu-id="cf55c-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf55c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf55c-122">CommonParameters</span></span>
<span data-ttu-id="cf55c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf55c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf55c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf55c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf55c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf55c-125">INPUTS</span></span>

### <span data-ttu-id="cf55c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cf55c-126">System.String</span></span>

### <span data-ttu-id="cf55c-127">Microsoft. Azure. Commands. Network. models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="cf55c-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="cf55c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf55c-128">OUTPUTS</span></span>

### <span data-ttu-id="cf55c-129">Microsoft. Azure. Commands. Network. models. PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf55c-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="cf55c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf55c-130">NOTES</span></span>

## <span data-ttu-id="cf55c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf55c-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf55c-132">Nowe — AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="cf55c-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="cf55c-133">Nowe — AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cf55c-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="cf55c-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cf55c-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="cf55c-135">Nowe — AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cf55c-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="cf55c-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cf55c-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="cf55c-137">Nowe — AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cf55c-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="cf55c-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cf55c-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="cf55c-139">Nowe — AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cf55c-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="cf55c-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cf55c-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)