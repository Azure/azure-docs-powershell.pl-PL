---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: e488baacb4e9412cb4e3e5be2b6a595629495b16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051728"
---
# <span data-ttu-id="169f5-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="169f5-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="169f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="169f5-102">SYNOPSIS</span></span>
<span data-ttu-id="169f5-103">Tworzy nowy prefiks usługi peer-and.</span><span class="sxs-lookup"><span data-stu-id="169f5-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="169f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="169f5-104">SYNTAX</span></span>

### <span data-ttu-id="169f5-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="169f5-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="169f5-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169f5-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="169f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="169f5-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="169f5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="169f5-108">DESCRIPTION</span></span>
<span data-ttu-id="169f5-109">Tworzy prefiks usługi peer-and skojarzony z obiektem usługi peer.</span><span class="sxs-lookup"><span data-stu-id="169f5-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="169f5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="169f5-110">EXAMPLES</span></span>

### <span data-ttu-id="169f5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="169f5-111">Example 1</span></span>
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

<span data-ttu-id="169f5-112">Tworzy prefiks z obiektu usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="169f5-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="169f5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="169f5-113">Example 2</span></span>
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

<span data-ttu-id="169f5-114">Tworzy prefiks na podstawie identyfikatora zasobu usługi peer.</span><span class="sxs-lookup"><span data-stu-id="169f5-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="169f5-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="169f5-115">Example 3</span></span>
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

<span data-ttu-id="169f5-116">Tworzy prefiks nazwy i nazwy grupy zasobów usługi peer-Group.</span><span class="sxs-lookup"><span data-stu-id="169f5-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="169f5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="169f5-117">PARAMETERS</span></span>

### <span data-ttu-id="169f5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="169f5-118">-AsJob</span></span>
<span data-ttu-id="169f5-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="169f5-119">Run in the background.</span></span>

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

### <span data-ttu-id="169f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169f5-120">-DefaultProfile</span></span>
<span data-ttu-id="169f5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="169f5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169f5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="169f5-122">-Name</span></span>
<span data-ttu-id="169f5-123">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="169f5-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="169f5-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="169f5-124">-PeeringServiceId</span></span>
<span data-ttu-id="169f5-125">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="169f5-125">The resource id string name.</span></span>

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

### <span data-ttu-id="169f5-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="169f5-126">-PeeringServiceName</span></span>
<span data-ttu-id="169f5-127">Nazwa usługi peer.</span><span class="sxs-lookup"><span data-stu-id="169f5-127">The peering service name.</span></span>
<span data-ttu-id="169f5-128">Użyj polecenia cmdlet New-AzPeeringService dla nowej usługi peer lub Get-AzPeeringService listy.</span><span class="sxs-lookup"><span data-stu-id="169f5-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="169f5-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="169f5-129">-PeeringServiceObject</span></span>
<span data-ttu-id="169f5-130">Używanie Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="169f5-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="169f5-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="169f5-131">-Prefix</span></span>
<span data-ttu-id="169f5-132">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="169f5-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="169f5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169f5-133">-ResourceGroupName</span></span>
<span data-ttu-id="169f5-134">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="169f5-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="169f5-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="169f5-135">-Confirm</span></span>
<span data-ttu-id="169f5-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="169f5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="169f5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="169f5-137">-WhatIf</span></span>
<span data-ttu-id="169f5-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="169f5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="169f5-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="169f5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="169f5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169f5-140">CommonParameters</span></span>
<span data-ttu-id="169f5-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169f5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169f5-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="169f5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169f5-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="169f5-143">INPUTS</span></span>

### <span data-ttu-id="169f5-144">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="169f5-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="169f5-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="169f5-145">OUTPUTS</span></span>

### <span data-ttu-id="169f5-146">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="169f5-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="169f5-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="169f5-147">NOTES</span></span>

## <span data-ttu-id="169f5-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="169f5-148">RELATED LINKS</span></span>
