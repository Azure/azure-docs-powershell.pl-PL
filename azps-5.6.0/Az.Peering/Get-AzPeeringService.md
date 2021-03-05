---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989493"
---
# <span data-ttu-id="e7ddc-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="e7ddc-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="e7ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ddc-103">Uzyskiwanie listy obiektów usługi komunikacji równorzędnej pojedynczego obiektu.</span><span class="sxs-lookup"><span data-stu-id="e7ddc-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="e7ddc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7ddc-104">SYNTAX</span></span>

### <span data-ttu-id="e7ddc-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="e7ddc-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ddc-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="e7ddc-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ddc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ddc-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7ddc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7ddc-108">DESCRIPTION</span></span>
<span data-ttu-id="e7ddc-109">Pobiera usługi komunikacji równorzędnej dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e7ddc-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="e7ddc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7ddc-110">EXAMPLES</span></span>

### <span data-ttu-id="e7ddc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7ddc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="e7ddc-112">Pobiera usługę komunikacji równorzędnej dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e7ddc-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="e7ddc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7ddc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="e7ddc-114">Pobiera usługę komunikacji równorzędnej dla grupy zasobów i nazwy</span><span class="sxs-lookup"><span data-stu-id="e7ddc-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="e7ddc-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e7ddc-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="e7ddc-116">Pobiera usługę komunikacji równorzędnej według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e7ddc-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="e7ddc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7ddc-117">PARAMETERS</span></span>

### <span data-ttu-id="e7ddc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ddc-118">-DefaultProfile</span></span>
<span data-ttu-id="e7ddc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ddc-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7ddc-120">-Name</span></span>
<span data-ttu-id="e7ddc-121">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e7ddc-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ddc-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7ddc-123">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7ddc-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ddc-124">-ResourceId</span></span>
<span data-ttu-id="e7ddc-125">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7ddc-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ddc-126">CommonParameters</span></span>
<span data-ttu-id="e7ddc-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ddc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ddc-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7ddc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ddc-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7ddc-129">INPUTS</span></span>

### <span data-ttu-id="e7ddc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e7ddc-130">System.String</span></span>

## <span data-ttu-id="e7ddc-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7ddc-131">OUTPUTS</span></span>

### <span data-ttu-id="e7ddc-132">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="e7ddc-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="e7ddc-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7ddc-133">NOTES</span></span>

## <span data-ttu-id="e7ddc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7ddc-134">RELATED LINKS</span></span>
