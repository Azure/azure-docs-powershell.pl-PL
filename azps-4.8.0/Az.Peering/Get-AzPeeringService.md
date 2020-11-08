---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221903"
---
# <span data-ttu-id="0d34b-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="0d34b-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="0d34b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d34b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d34b-103">Uzyskiwanie listy obiektów usługi peer dla pojedynczego obiektu.</span><span class="sxs-lookup"><span data-stu-id="0d34b-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="0d34b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d34b-104">SYNTAX</span></span>

### <span data-ttu-id="0d34b-105">ByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d34b-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d34b-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0d34b-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d34b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d34b-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d34b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d34b-108">DESCRIPTION</span></span>
<span data-ttu-id="0d34b-109">Pobiera usługi komunikacji równorzędnej dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0d34b-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="0d34b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d34b-110">EXAMPLES</span></span>

### <span data-ttu-id="0d34b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d34b-111">Example 1</span></span>
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

<span data-ttu-id="0d34b-112">Pobiera usługę peer dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0d34b-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="0d34b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0d34b-113">Example 2</span></span>
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

<span data-ttu-id="0d34b-114">Pobiera usługę peer dla grupy zasobów i nazwy</span><span class="sxs-lookup"><span data-stu-id="0d34b-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="0d34b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0d34b-115">Example 3</span></span>
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

<span data-ttu-id="0d34b-116">Pobiera usługę peer dla identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="0d34b-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="0d34b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d34b-117">PARAMETERS</span></span>

### <span data-ttu-id="0d34b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d34b-118">-DefaultProfile</span></span>
<span data-ttu-id="0d34b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d34b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d34b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d34b-120">-Name</span></span>
<span data-ttu-id="0d34b-121">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="0d34b-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="0d34b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d34b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d34b-123">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d34b-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="0d34b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d34b-124">-ResourceId</span></span>
<span data-ttu-id="0d34b-125">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d34b-125">The resource id string name.</span></span>

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

### <span data-ttu-id="0d34b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d34b-126">CommonParameters</span></span>
<span data-ttu-id="0d34b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d34b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d34b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d34b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d34b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d34b-129">INPUTS</span></span>

### <span data-ttu-id="0d34b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d34b-130">System.String</span></span>

## <span data-ttu-id="0d34b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d34b-131">OUTPUTS</span></span>

### <span data-ttu-id="0d34b-132">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="0d34b-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="0d34b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d34b-133">NOTES</span></span>

## <span data-ttu-id="0d34b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d34b-134">RELATED LINKS</span></span>
