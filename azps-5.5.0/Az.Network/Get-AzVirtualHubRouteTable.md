---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193722"
---
# <span data-ttu-id="019bb-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="019bb-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="019bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="019bb-102">SYNOPSIS</span></span>
<span data-ttu-id="019bb-103">Pobiera tabelę tras wirtualnego centrum w centrum wirtualnym lub wyświetla wszystkie tabele tras w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="019bb-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="019bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="019bb-104">SYNTAX</span></span>

### <span data-ttu-id="019bb-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="019bb-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="019bb-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="019bb-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="019bb-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="019bb-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="019bb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="019bb-108">DESCRIPTION</span></span>
<span data-ttu-id="019bb-109">Pobiera tabelę tras wirtualnego centrum w centrum wirtualnym lub wyświetla wszystkie tabele tras w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="019bb-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="019bb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="019bb-110">EXAMPLES</span></span>

### <span data-ttu-id="019bb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="019bb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="019bb-112">To polecenie cmdlet pobiera zasób tabeli trasy przy użyciu nazwy grupy zasobów, nazwy centrum i nazwy tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="019bb-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="019bb-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="019bb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="019bb-114">To polecenie cmdlet wyświetla listę wszystkich tabel tras obecnych w centrum wirtualnym przy użyciu nazwy grupy zasobów i nazwy centrum.</span><span class="sxs-lookup"><span data-stu-id="019bb-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="019bb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="019bb-115">PARAMETERS</span></span>

### <span data-ttu-id="019bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019bb-116">-DefaultProfile</span></span>
<span data-ttu-id="019bb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="019bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="019bb-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="019bb-118">-HubName</span></span>
<span data-ttu-id="019bb-119">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="019bb-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019bb-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="019bb-120">-Name</span></span>
<span data-ttu-id="019bb-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="019bb-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019bb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="019bb-122">-ParentResourceId</span></span>
<span data-ttu-id="019bb-123">Identyfikator zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="019bb-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="019bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="019bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="019bb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="019bb-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019bb-126">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="019bb-126">-VirtualHub</span></span>
<span data-ttu-id="019bb-127">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="019bb-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="019bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019bb-128">CommonParameters</span></span>
<span data-ttu-id="019bb-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019bb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="019bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019bb-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="019bb-131">INPUTS</span></span>

### <span data-ttu-id="019bb-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="019bb-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="019bb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="019bb-133">System.String</span></span>

## <span data-ttu-id="019bb-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="019bb-134">OUTPUTS</span></span>

### <span data-ttu-id="019bb-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="019bb-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="019bb-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="019bb-136">NOTES</span></span>

## <span data-ttu-id="019bb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="019bb-137">RELATED LINKS</span></span>
