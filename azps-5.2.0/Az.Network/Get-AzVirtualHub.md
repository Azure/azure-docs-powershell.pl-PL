---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357562"
---
# <span data-ttu-id="061c5-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="061c5-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="061c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="061c5-102">SYNOPSIS</span></span>
<span data-ttu-id="061c5-103">Pobiera usługę Azure VirtualHub, używając nazwy i ResourceGroupName albo listę wszystkich wirtualnych koncentratorów przez ResourceGroupName/abonament.</span><span class="sxs-lookup"><span data-stu-id="061c5-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="061c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="061c5-104">SYNTAX</span></span>

### <span data-ttu-id="061c5-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="061c5-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="061c5-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061c5-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="061c5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="061c5-107">DESCRIPTION</span></span>
<span data-ttu-id="061c5-108">Pobiera usługę Azure VirtualHub, używając nazwy i ResourceGroupName albo listę wszystkich wirtualnych koncentratorów przez ResourceGroupName/abonament.</span><span class="sxs-lookup"><span data-stu-id="061c5-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="061c5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="061c5-109">EXAMPLES</span></span>

### <span data-ttu-id="061c5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="061c5-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="061c5-111">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="061c5-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="061c5-112">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="061c5-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="061c5-113">Następnie pobiera koncentrator wirtualny przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="061c5-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="061c5-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="061c5-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="061c5-115">To polecenie cmdlet umożliwia pobieranie koncentratora wirtualnego przy użyciu funkcji filtrowania.</span><span class="sxs-lookup"><span data-stu-id="061c5-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="061c5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="061c5-116">PARAMETERS</span></span>

### <span data-ttu-id="061c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061c5-117">-DefaultProfile</span></span>
<span data-ttu-id="061c5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="061c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="061c5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="061c5-119">-Name</span></span>
<span data-ttu-id="061c5-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="061c5-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="061c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="061c5-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="061c5-122">The resource group name.</span></span>

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

### <span data-ttu-id="061c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061c5-123">CommonParameters</span></span>
<span data-ttu-id="061c5-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061c5-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="061c5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061c5-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="061c5-126">INPUTS</span></span>

### <span data-ttu-id="061c5-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="061c5-127">None</span></span>

## <span data-ttu-id="061c5-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="061c5-128">OUTPUTS</span></span>

### <span data-ttu-id="061c5-129">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="061c5-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="061c5-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="061c5-130">NOTES</span></span>

## <span data-ttu-id="061c5-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="061c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="061c5-132">Nowe — AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="061c5-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="061c5-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="061c5-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="061c5-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="061c5-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
