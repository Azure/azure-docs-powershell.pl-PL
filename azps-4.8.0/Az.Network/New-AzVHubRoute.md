---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219470"
---
# <span data-ttu-id="e0027-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="e0027-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="e0027-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0027-102">SYNOPSIS</span></span>
<span data-ttu-id="e0027-103">Tworzy obiekt VHubRoute, który może zostać przekazany jako parametr do polecenia New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e0027-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="e0027-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0027-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0027-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0027-105">DESCRIPTION</span></span>

<span data-ttu-id="e0027-106">Tworzy obiekt VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="e0027-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="e0027-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0027-107">EXAMPLES</span></span>

### <span data-ttu-id="e0027-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0027-108">Example 1</span></span>

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

<span data-ttu-id="e0027-109">Powyższe polecenie utworzy obiekt VHubRoute z opcją Następny skok jako określoną zaporę, którą można następnie dodać do zasobu VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e0027-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="e0027-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e0027-110">Example 2</span></span>

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

<span data-ttu-id="e0027-111">Powyższe polecenie utworzy obiekt VHubRoute, używając skoku, jako określonego hubVnetConnection, który następnie można dodać do zasobu VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e0027-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="e0027-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0027-112">PARAMETERS</span></span>

### <span data-ttu-id="e0027-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0027-113">-DefaultProfile</span></span>
<span data-ttu-id="e0027-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0027-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0027-115">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="e0027-115">-Destination</span></span>
<span data-ttu-id="e0027-116">Lista miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="e0027-116">List of Destinations.</span></span>

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

### <span data-ttu-id="e0027-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="e0027-117">-DestinationType</span></span>
<span data-ttu-id="e0027-118">Typ lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="e0027-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="e0027-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0027-119">-Name</span></span>
<span data-ttu-id="e0027-120">Nazwa trasy.</span><span class="sxs-lookup"><span data-stu-id="e0027-120">The route name.</span></span>

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

### <span data-ttu-id="e0027-121">-Następny skok</span><span class="sxs-lookup"><span data-stu-id="e0027-121">-NextHop</span></span>
<span data-ttu-id="e0027-122">Następny przeskok.</span><span class="sxs-lookup"><span data-stu-id="e0027-122">The next hop.</span></span>

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

### <span data-ttu-id="e0027-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="e0027-123">-NextHopType</span></span>
<span data-ttu-id="e0027-124">Typ następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="e0027-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="e0027-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0027-125">CommonParameters</span></span>
<span data-ttu-id="e0027-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0027-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0027-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0027-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0027-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0027-128">INPUTS</span></span>

### <span data-ttu-id="e0027-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e0027-129">System.String</span></span>

## <span data-ttu-id="e0027-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0027-130">OUTPUTS</span></span>

### <span data-ttu-id="e0027-131">Microsoft. Azure. Commands. Network. models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="e0027-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="e0027-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0027-132">NOTES</span></span>

## <span data-ttu-id="e0027-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0027-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0027-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0027-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="e0027-135">Nowe — AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0027-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="e0027-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0027-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="e0027-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0027-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)