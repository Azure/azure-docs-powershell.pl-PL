---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 8b62189848583d11738a39555bc80ed0a52776fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989472"
---
# <span data-ttu-id="18475-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="18475-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="18475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18475-102">SYNOPSIS</span></span>
<span data-ttu-id="18475-103">Pobiera listę prefiksów usługi komunikacji równorzędnej dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="18475-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="18475-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18475-104">SYNTAX</span></span>

### <span data-ttu-id="18475-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="18475-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18475-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="18475-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18475-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="18475-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18475-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="18475-108">DESCRIPTION</span></span>
<span data-ttu-id="18475-109">Lista prefiksów usługi komunikacji równorzędnej dla obiektów usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="18475-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="18475-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18475-110">EXAMPLES</span></span>

### <span data-ttu-id="18475-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18475-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="18475-112">Pobiera prefiksy dla usługi komunikacji równorzędnej na podstawie poleceń rurowych.</span><span class="sxs-lookup"><span data-stu-id="18475-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="18475-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="18475-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="18475-114">Otrzymuje określony prefiks dla usługi komunikacji równorzędnej według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="18475-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="18475-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="18475-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="18475-116">Otrzymuje określony prefiks dla usługi komunikacji równorzędnej według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="18475-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="18475-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="18475-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="18475-118">Pobiera określony prefiks dla usługi komunikacji równorzędnej z rozwiniętymi atrybutami</span><span class="sxs-lookup"><span data-stu-id="18475-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="18475-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18475-119">PARAMETERS</span></span>

### <span data-ttu-id="18475-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18475-120">-DefaultProfile</span></span>
<span data-ttu-id="18475-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18475-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18475-122">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="18475-122">-Expand</span></span>
<span data-ttu-id="18475-123">Wyświetlanie zdarzeń dla prefiksu usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="18475-123">View the events for a peering service prefix</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18475-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="18475-124">-Name</span></span>
<span data-ttu-id="18475-125">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="18475-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18475-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="18475-126">-PeeringServiceName</span></span>
<span data-ttu-id="18475-127">Nazwa usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="18475-127">The peering service name.</span></span> <span data-ttu-id="18475-128">Użyj New-AzPeeringService cmdlet dla nowej usługi komunikacji równorzędnej lub Get-AzPeeringService listy.</span><span class="sxs-lookup"><span data-stu-id="18475-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18475-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="18475-129">-PeeringServiceObject</span></span>
<span data-ttu-id="18475-130">Używanie Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="18475-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18475-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18475-131">-ResourceGroupName</span></span>
<span data-ttu-id="18475-132">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18475-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="18475-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18475-133">-ResourceId</span></span>
<span data-ttu-id="18475-134">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="18475-134">The resource id string name.</span></span>

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

### <span data-ttu-id="18475-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18475-135">CommonParameters</span></span>
<span data-ttu-id="18475-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18475-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18475-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18475-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18475-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18475-138">INPUTS</span></span>

### <span data-ttu-id="18475-139">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="18475-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="18475-140">System.String</span><span class="sxs-lookup"><span data-stu-id="18475-140">System.String</span></span>

## <span data-ttu-id="18475-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18475-141">OUTPUTS</span></span>

### <span data-ttu-id="18475-142">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="18475-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="18475-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18475-143">NOTES</span></span>

## <span data-ttu-id="18475-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18475-144">RELATED LINKS</span></span>
