---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 630e0a6759e278e4da2d6d56cf34bb5fa5812595
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954001"
---
# <span data-ttu-id="34a39-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="34a39-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="34a39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a39-102">SYNOPSIS</span></span>
<span data-ttu-id="34a39-103">Pobiera usługę Azure VirtualHub według nazwy i nazwy ResourceGroupName lub wyświetla wszystkie koncentratory wirtualne według nazwa_grupy zasobów/subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34a39-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="34a39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34a39-104">SYNTAX</span></span>

### <span data-ttu-id="34a39-105">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="34a39-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34a39-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a39-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34a39-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="34a39-107">DESCRIPTION</span></span>
<span data-ttu-id="34a39-108">Pobiera usługę Azure VirtualHub według nazwy i nazwy ResourceGroupName lub wyświetla wszystkie koncentratory wirtualne według nazwa_grupy zasobów/subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34a39-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="34a39-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34a39-109">EXAMPLES</span></span>

### <span data-ttu-id="34a39-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34a39-110">Example 1</span></span>

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

<span data-ttu-id="34a39-111">Powyższe spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i centrum wirtualnego w Zachód w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="34a39-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="34a39-112">Centrum wirtualne będzie mieć przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="34a39-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="34a39-113">Następnie otrzymuje ono centrum wirtualne za pomocą nazwy ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="34a39-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="34a39-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="34a39-114">Example 2</span></span>

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

<span data-ttu-id="34a39-115">To polecenie cmdlet pobiera centrum wirtualne za pomocą filtrowania.</span><span class="sxs-lookup"><span data-stu-id="34a39-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="34a39-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a39-116">PARAMETERS</span></span>

### <span data-ttu-id="34a39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a39-117">-DefaultProfile</span></span>
<span data-ttu-id="34a39-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34a39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a39-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34a39-119">-Name</span></span>
<span data-ttu-id="34a39-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="34a39-120">The resource name.</span></span>

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

### <span data-ttu-id="34a39-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a39-121">-ResourceGroupName</span></span>
<span data-ttu-id="34a39-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34a39-122">The resource group name.</span></span>

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

### <span data-ttu-id="34a39-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a39-123">CommonParameters</span></span>
<span data-ttu-id="34a39-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a39-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a39-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34a39-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a39-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34a39-126">INPUTS</span></span>

### <span data-ttu-id="34a39-127">Brak</span><span class="sxs-lookup"><span data-stu-id="34a39-127">None</span></span>

## <span data-ttu-id="34a39-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34a39-128">OUTPUTS</span></span>

### <span data-ttu-id="34a39-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="34a39-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="34a39-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34a39-130">NOTES</span></span>

## <span data-ttu-id="34a39-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34a39-131">RELATED LINKS</span></span>

[<span data-ttu-id="34a39-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="34a39-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="34a39-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="34a39-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="34a39-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="34a39-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
