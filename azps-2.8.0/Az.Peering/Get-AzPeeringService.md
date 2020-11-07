---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: b2ebc3e91f08c2aa33853c8a90c929b31877a014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872391"
---
# <span data-ttu-id="702a3-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="702a3-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="702a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="702a3-102">SYNOPSIS</span></span>
<span data-ttu-id="702a3-103">Uzyskiwanie listy obiektów usługi peer dla pojedynczego obiektu.</span><span class="sxs-lookup"><span data-stu-id="702a3-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="702a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="702a3-104">SYNTAX</span></span>

### <span data-ttu-id="702a3-105">ByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="702a3-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="702a3-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="702a3-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="702a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="702a3-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="702a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="702a3-108">DESCRIPTION</span></span>
<span data-ttu-id="702a3-109">Pobiera usługi komunikacji równorzędnej dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="702a3-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="702a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="702a3-110">EXAMPLES</span></span>

### <span data-ttu-id="702a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="702a3-111">Example 1</span></span>
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

<span data-ttu-id="702a3-112">Pobiera usługę peer dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="702a3-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="702a3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="702a3-113">Example 2</span></span>
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

<span data-ttu-id="702a3-114">Pobiera usługę peer dla grupy zasobów i nazwy</span><span class="sxs-lookup"><span data-stu-id="702a3-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="702a3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="702a3-115">Example 3</span></span>
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

<span data-ttu-id="702a3-116">Pobiera usługę peer dla identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="702a3-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="702a3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="702a3-117">PARAMETERS</span></span>

### <span data-ttu-id="702a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702a3-118">-DefaultProfile</span></span>
<span data-ttu-id="702a3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="702a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="702a3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="702a3-120">-Name</span></span>
<span data-ttu-id="702a3-121">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="702a3-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="702a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="702a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="702a3-123">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="702a3-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="702a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="702a3-124">-ResourceId</span></span>
<span data-ttu-id="702a3-125">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="702a3-125">The resource id string name.</span></span>

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

### <span data-ttu-id="702a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702a3-126">CommonParameters</span></span>
<span data-ttu-id="702a3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="702a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702a3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="702a3-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702a3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="702a3-129">INPUTS</span></span>

### <span data-ttu-id="702a3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="702a3-130">System.String</span></span>

## <span data-ttu-id="702a3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="702a3-131">OUTPUTS</span></span>

### <span data-ttu-id="702a3-132">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="702a3-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="702a3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="702a3-133">NOTES</span></span>

## <span data-ttu-id="702a3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="702a3-134">RELATED LINKS</span></span>
