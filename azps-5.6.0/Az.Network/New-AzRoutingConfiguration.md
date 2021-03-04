---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: b67b37f66e9b13c692b10dbdca54230bc1b0a529
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953882"
---
# <span data-ttu-id="778ad-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="778ad-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="778ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="778ad-102">SYNOPSIS</span></span>
<span data-ttu-id="778ad-103">Tworzy obiekt RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="778ad-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="778ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="778ad-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="778ad-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="778ad-105">DESCRIPTION</span></span>
<span data-ttu-id="778ad-106">Tworzy obiekt RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="778ad-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="778ad-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="778ad-107">EXAMPLES</span></span>

### <span data-ttu-id="778ad-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="778ad-108">Example 1</span></span>
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

<span data-ttu-id="778ad-109">Powyższe polecenie utworzy obiekt RoutingConfiguration, który można następnie dodać do zasobu połączenia.</span><span class="sxs-lookup"><span data-stu-id="778ad-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="778ad-110">Trasy statyczne są dozwolone tylko w przypadku obiektu HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="778ad-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="778ad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="778ad-111">PARAMETERS</span></span>

### <span data-ttu-id="778ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778ad-112">-DefaultProfile</span></span>
<span data-ttu-id="778ad-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="778ad-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="778ad-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="778ad-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="778ad-115">Tabela tras centrum skojarzona z tą konfiguracją routingu.</span><span class="sxs-lookup"><span data-stu-id="778ad-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="778ad-116">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="778ad-116">-Id</span></span>
<span data-ttu-id="778ad-117">Lista identyfikatorów zasobów wszystkich tabel tras centrum w celu anonsowania tras do właściwości PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="778ad-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="778ad-118">— Label</span><span class="sxs-lookup"><span data-stu-id="778ad-118">-Label</span></span>
<span data-ttu-id="778ad-119">Lista etykiet dla właściwości PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="778ad-119">The list of labels for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="778ad-120">- StaticRoute</span><span class="sxs-lookup"><span data-stu-id="778ad-120">-StaticRoute</span></span>
<span data-ttu-id="778ad-121">Lista tras sterujących routingiem z aplikacji VirtualHub do wirtualnego połączenia sieciowego.</span><span class="sxs-lookup"><span data-stu-id="778ad-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

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

### <span data-ttu-id="778ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778ad-122">CommonParameters</span></span>
<span data-ttu-id="778ad-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="778ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778ad-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="778ad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778ad-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="778ad-125">INPUTS</span></span>

### <span data-ttu-id="778ad-126">System.String</span><span class="sxs-lookup"><span data-stu-id="778ad-126">System.String</span></span>

### <span data-ttu-id="778ad-127">Microsoft.Azure.Commands.Network.Models.PS ZSzybkiRoute</span><span class="sxs-lookup"><span data-stu-id="778ad-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="778ad-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="778ad-128">OUTPUTS</span></span>

### <span data-ttu-id="778ad-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="778ad-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="778ad-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="778ad-130">NOTES</span></span>

## <span data-ttu-id="778ad-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="778ad-131">RELATED LINKS</span></span>

[<span data-ttu-id="778ad-132">New-AzFiltrRoute</span><span class="sxs-lookup"><span data-stu-id="778ad-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="778ad-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="778ad-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="778ad-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="778ad-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="778ad-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="778ad-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="778ad-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="778ad-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="778ad-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="778ad-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="778ad-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="778ad-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="778ad-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778ad-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="778ad-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778ad-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)