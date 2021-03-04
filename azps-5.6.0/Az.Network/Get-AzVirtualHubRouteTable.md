---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: 56f0eb8362cef287cea326ea30a559d7efc70573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953953"
---
# <span data-ttu-id="75058-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="75058-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="75058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75058-102">SYNOPSIS</span></span>
<span data-ttu-id="75058-103">Pobiera tabelę tras wirtualnego centrum w centrum wirtualnym lub wyświetla wszystkie tabele tras w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="75058-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="75058-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75058-104">SYNTAX</span></span>

### <span data-ttu-id="75058-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="75058-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75058-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="75058-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75058-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="75058-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75058-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="75058-108">DESCRIPTION</span></span>
<span data-ttu-id="75058-109">Pobiera tabelę tras wirtualnego centrum w centrum wirtualnym lub wyświetla wszystkie tabele tras w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="75058-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="75058-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75058-110">EXAMPLES</span></span>

### <span data-ttu-id="75058-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="75058-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="75058-112">To polecenie cmdlet pobiera zasób tabeli trasy przy użyciu nazwy grupy zasobów, nazwy centrum i nazwy tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="75058-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="75058-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="75058-113">Example 2</span></span>
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

<span data-ttu-id="75058-114">To polecenie cmdlet wyświetla listę wszystkich tabel tras obecnych w centrum wirtualnym przy użyciu nazwy grupy zasobów i nazwy centrum.</span><span class="sxs-lookup"><span data-stu-id="75058-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="75058-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75058-115">PARAMETERS</span></span>

### <span data-ttu-id="75058-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75058-116">-DefaultProfile</span></span>
<span data-ttu-id="75058-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75058-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75058-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="75058-118">-HubName</span></span>
<span data-ttu-id="75058-119">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="75058-119">The parent resource name.</span></span>

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

### <span data-ttu-id="75058-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75058-120">-Name</span></span>
<span data-ttu-id="75058-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="75058-121">The resource name.</span></span>

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

### <span data-ttu-id="75058-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="75058-122">-ParentResourceId</span></span>
<span data-ttu-id="75058-123">Identyfikator zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="75058-123">The parent resource id.</span></span>

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

### <span data-ttu-id="75058-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75058-124">-ResourceGroupName</span></span>
<span data-ttu-id="75058-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75058-125">The resource group name.</span></span>

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

### <span data-ttu-id="75058-126">— VirtualHub</span><span class="sxs-lookup"><span data-stu-id="75058-126">-VirtualHub</span></span>
<span data-ttu-id="75058-127">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="75058-127">The parent resource.</span></span>

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

### <span data-ttu-id="75058-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75058-128">CommonParameters</span></span>
<span data-ttu-id="75058-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75058-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75058-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75058-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75058-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75058-131">INPUTS</span></span>

### <span data-ttu-id="75058-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="75058-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="75058-133">System.String</span><span class="sxs-lookup"><span data-stu-id="75058-133">System.String</span></span>

## <span data-ttu-id="75058-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75058-134">OUTPUTS</span></span>

### <span data-ttu-id="75058-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="75058-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="75058-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75058-136">NOTES</span></span>

## <span data-ttu-id="75058-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75058-137">RELATED LINKS</span></span>
