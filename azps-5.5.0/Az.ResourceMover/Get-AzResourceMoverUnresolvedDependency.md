---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201899"
---
# <span data-ttu-id="2f318-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="2f318-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="2f318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f318-102">SYNOPSIS</span></span>
<span data-ttu-id="2f318-103">Pobiera listę nierozpoznanych zależności.</span><span class="sxs-lookup"><span data-stu-id="2f318-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="2f318-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f318-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2f318-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f318-105">DESCRIPTION</span></span>
<span data-ttu-id="2f318-106">Pobiera listę nierozpoznanych zależności.</span><span class="sxs-lookup"><span data-stu-id="2f318-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="2f318-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f318-107">EXAMPLES</span></span>

### <span data-ttu-id="2f318-108">Przykład 1. Uzyskiwanie listy nierozpoznanych zasobów zależnych</span><span class="sxs-lookup"><span data-stu-id="2f318-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="2f318-109">Pobierz listę nierozpoznanych zasobów zależnych dla kolekcji przenoszenie.</span><span class="sxs-lookup"><span data-stu-id="2f318-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="2f318-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f318-110">PARAMETERS</span></span>

### <span data-ttu-id="2f318-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f318-111">-DefaultProfile</span></span>
<span data-ttu-id="2f318-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f318-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f318-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2f318-113">-MoveCollectionName</span></span>
<span data-ttu-id="2f318-114">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="2f318-114">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f318-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f318-115">-ResourceGroupName</span></span>
<span data-ttu-id="2f318-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f318-116">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f318-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f318-117">-SubscriptionId</span></span>
<span data-ttu-id="2f318-118">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2f318-118">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f318-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f318-119">CommonParameters</span></span>
<span data-ttu-id="2f318-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f318-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f318-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f318-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f318-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f318-122">INPUTS</span></span>

## <span data-ttu-id="2f318-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f318-123">OUTPUTS</span></span>

### <span data-ttu-id="2f318-124">Microsoft.Azure.PowerShell.Cmdlet.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="2f318-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="2f318-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f318-125">NOTES</span></span>

<span data-ttu-id="2f318-126">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2f318-126">ALIASES</span></span>

## <span data-ttu-id="2f318-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f318-127">RELATED LINKS</span></span>

