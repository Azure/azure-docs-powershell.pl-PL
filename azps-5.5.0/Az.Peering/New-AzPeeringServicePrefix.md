---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240386"
---
# <span data-ttu-id="4abd1-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="4abd1-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="4abd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4abd1-102">SYNOPSIS</span></span>
<span data-ttu-id="4abd1-103">Tworzy prefiks nowej usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="4abd1-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="4abd1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4abd1-104">SYNTAX</span></span>

### <span data-ttu-id="4abd1-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4abd1-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4abd1-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abd1-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4abd1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4abd1-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abd1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4abd1-108">DESCRIPTION</span></span>
<span data-ttu-id="4abd1-109">Tworzy prefiks usługi komunikacji równorzędnej skojarzony z obiektem usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4abd1-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="4abd1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4abd1-110">EXAMPLES</span></span>

### <span data-ttu-id="4abd1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4abd1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="4abd1-112">Tworzy prefiks z obiektu usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4abd1-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="4abd1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4abd1-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="4abd1-114">Tworzy prefiks z identyfikatora zasobu usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4abd1-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="4abd1-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4abd1-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="4abd1-116">Tworzy prefiks z nazwy i nazwy grupy zasobów usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="4abd1-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="4abd1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4abd1-117">PARAMETERS</span></span>

### <span data-ttu-id="4abd1-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4abd1-118">-AsJob</span></span>
<span data-ttu-id="4abd1-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="4abd1-119">Run in the background.</span></span>

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

### <span data-ttu-id="4abd1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abd1-120">-DefaultProfile</span></span>
<span data-ttu-id="4abd1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4abd1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4abd1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4abd1-122">-Name</span></span>
<span data-ttu-id="4abd1-123">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="4abd1-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="4abd1-124">-PeeringServiceId</span></span>
<span data-ttu-id="4abd1-125">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="4abd1-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="4abd1-126">-PeeringServiceName</span></span>
<span data-ttu-id="4abd1-127">Nazwa usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4abd1-127">The peering service name.</span></span>
<span data-ttu-id="4abd1-128">Użyj New-AzPeeringService cmdlet dla nowej usługi komunikacji równorzędnej lub Get-AzPeeringService listy.</span><span class="sxs-lookup"><span data-stu-id="4abd1-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="4abd1-129">-PeeringServiceObject</span></span>
<span data-ttu-id="4abd1-130">Używanie Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="4abd1-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-131">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="4abd1-131">-Prefix</span></span>
<span data-ttu-id="4abd1-132">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="4abd1-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="4abd1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abd1-133">-ResourceGroupName</span></span>
<span data-ttu-id="4abd1-134">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4abd1-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="4abd1-135">-ServiceKey</span></span>
<span data-ttu-id="4abd1-136">Jest to unikatowy identyfikator GUID dostarczany przez usługodawca</span><span class="sxs-lookup"><span data-stu-id="4abd1-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="4abd1-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4abd1-137">-Confirm</span></span>
<span data-ttu-id="4abd1-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4abd1-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abd1-139">-WhatIf</span></span>
<span data-ttu-id="4abd1-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abd1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4abd1-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4abd1-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abd1-142">CommonParameters</span></span>
<span data-ttu-id="4abd1-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abd1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abd1-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4abd1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abd1-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4abd1-145">INPUTS</span></span>

### <span data-ttu-id="4abd1-146">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="4abd1-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="4abd1-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4abd1-147">OUTPUTS</span></span>

### <span data-ttu-id="4abd1-148">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="4abd1-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="4abd1-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4abd1-149">NOTES</span></span>

## <span data-ttu-id="4abd1-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4abd1-150">RELATED LINKS</span></span>
