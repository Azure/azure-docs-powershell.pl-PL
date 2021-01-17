---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384722"
---
# <span data-ttu-id="7a066-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7a066-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="7a066-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a066-102">SYNOPSIS</span></span>
<span data-ttu-id="7a066-103">Tworzy nowy prefiks usługi peer-and.</span><span class="sxs-lookup"><span data-stu-id="7a066-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="7a066-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a066-104">SYNTAX</span></span>

### <span data-ttu-id="7a066-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7a066-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a066-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a066-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a066-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a066-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a066-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7a066-108">DESCRIPTION</span></span>
<span data-ttu-id="7a066-109">Tworzy prefiks usługi peer-and skojarzony z obiektem usługi peer.</span><span class="sxs-lookup"><span data-stu-id="7a066-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="7a066-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a066-110">EXAMPLES</span></span>

### <span data-ttu-id="7a066-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a066-111">Example 1</span></span>
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

<span data-ttu-id="7a066-112">Tworzy prefiks z obiektu usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="7a066-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="7a066-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7a066-113">Example 2</span></span>
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

<span data-ttu-id="7a066-114">Tworzy prefiks na podstawie identyfikatora zasobu usługi peer.</span><span class="sxs-lookup"><span data-stu-id="7a066-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="7a066-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7a066-115">Example 3</span></span>
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

<span data-ttu-id="7a066-116">Tworzy prefiks nazwy i nazwy grupy zasobów usługi peer-Group.</span><span class="sxs-lookup"><span data-stu-id="7a066-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="7a066-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a066-117">PARAMETERS</span></span>

### <span data-ttu-id="7a066-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a066-118">-AsJob</span></span>
<span data-ttu-id="7a066-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="7a066-119">Run in the background.</span></span>

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

### <span data-ttu-id="7a066-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a066-120">-DefaultProfile</span></span>
<span data-ttu-id="7a066-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a066-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a066-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a066-122">-Name</span></span>
<span data-ttu-id="7a066-123">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7a066-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7a066-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="7a066-124">-PeeringServiceId</span></span>
<span data-ttu-id="7a066-125">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a066-125">The resource id string name.</span></span>

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

### <span data-ttu-id="7a066-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="7a066-126">-PeeringServiceName</span></span>
<span data-ttu-id="7a066-127">Nazwa usługi peer.</span><span class="sxs-lookup"><span data-stu-id="7a066-127">The peering service name.</span></span>
<span data-ttu-id="7a066-128">Użyj polecenia cmdlet New-AzPeeringService dla nowej usługi peer lub Get-AzPeeringService listy.</span><span class="sxs-lookup"><span data-stu-id="7a066-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="7a066-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="7a066-129">-PeeringServiceObject</span></span>
<span data-ttu-id="7a066-130">Używanie Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="7a066-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="7a066-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7a066-131">-Prefix</span></span>
<span data-ttu-id="7a066-132">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="7a066-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="7a066-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a066-133">-ResourceGroupName</span></span>
<span data-ttu-id="7a066-134">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a066-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7a066-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="7a066-135">-ServiceKey</span></span>
<span data-ttu-id="7a066-136">Jest to unikatowy identyfikator GUID podany przez dostawcę usługi</span><span class="sxs-lookup"><span data-stu-id="7a066-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="7a066-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a066-137">-Confirm</span></span>
<span data-ttu-id="7a066-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a066-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a066-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a066-139">-WhatIf</span></span>
<span data-ttu-id="7a066-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a066-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a066-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a066-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a066-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a066-142">CommonParameters</span></span>
<span data-ttu-id="7a066-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a066-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a066-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a066-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a066-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a066-145">INPUTS</span></span>

### <span data-ttu-id="7a066-146">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="7a066-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="7a066-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a066-147">OUTPUTS</span></span>

### <span data-ttu-id="7a066-148">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7a066-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="7a066-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a066-149">NOTES</span></span>

## <span data-ttu-id="7a066-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a066-150">RELATED LINKS</span></span>
