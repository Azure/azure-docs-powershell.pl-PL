---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499949"
---
# <span data-ttu-id="8a07e-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="8a07e-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="8a07e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a07e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a07e-103">Pobiera listę nierozwiązanych zależności.</span><span class="sxs-lookup"><span data-stu-id="8a07e-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="8a07e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a07e-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a07e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a07e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a07e-106">Pobiera listę nierozwiązanych zależności.</span><span class="sxs-lookup"><span data-stu-id="8a07e-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="8a07e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a07e-107">EXAMPLES</span></span>

### <span data-ttu-id="8a07e-108">Przykład 1: Pobieranie listy nierozwiązanych zasobów zależnych</span><span class="sxs-lookup"><span data-stu-id="8a07e-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="8a07e-109">Pobieranie listy nierozwiązanych zasobów zależnych dla kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="8a07e-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="8a07e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a07e-110">PARAMETERS</span></span>

### <span data-ttu-id="8a07e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a07e-111">-DefaultProfile</span></span>
<span data-ttu-id="8a07e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a07e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a07e-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8a07e-113">-MoveCollectionName</span></span>
<span data-ttu-id="8a07e-114">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8a07e-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8a07e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a07e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a07e-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a07e-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8a07e-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8a07e-117">-SubscriptionId</span></span>
<span data-ttu-id="8a07e-118">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8a07e-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="8a07e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a07e-119">CommonParameters</span></span>
<span data-ttu-id="8a07e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a07e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a07e-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a07e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a07e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a07e-122">INPUTS</span></span>

## <span data-ttu-id="8a07e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a07e-123">OUTPUTS</span></span>

### <span data-ttu-id="8a07e-124">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="8a07e-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="8a07e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a07e-125">NOTES</span></span>

<span data-ttu-id="8a07e-126">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8a07e-126">ALIASES</span></span>

## <span data-ttu-id="8a07e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a07e-127">RELATED LINKS</span></span>

