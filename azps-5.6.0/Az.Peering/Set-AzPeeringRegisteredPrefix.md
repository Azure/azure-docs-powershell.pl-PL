---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 2990b28e811b21940d51ce8d0fd9c7540feccfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989192"
---
# <span data-ttu-id="d0a7b-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d0a7b-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d0a7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a7b-103">Ustawia lub aktualizuje zarejestrowany prefiks z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="d0a7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0a7b-104">SYNTAX</span></span>

### <span data-ttu-id="d0a7b-105">ByResourceGroupAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d0a7b-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0a7b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d0a7b-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0a7b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a7b-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a7b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0a7b-108">DESCRIPTION</span></span>
<span data-ttu-id="d0a7b-109">Umożliwia aktualizowanie zarejestrowanego prefiksu z nadrzędnego zasobu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="d0a7b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0a7b-110">EXAMPLES</span></span>

### <span data-ttu-id="d0a7b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0a7b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="d0a7b-112">Aktualizuje prefiks według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="d0a7b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0a7b-113">PARAMETERS</span></span>

### <span data-ttu-id="d0a7b-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d0a7b-114">-AsJob</span></span>
<span data-ttu-id="d0a7b-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-115">Run in the background.</span></span>

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

### <span data-ttu-id="d0a7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a7b-116">-DefaultProfile</span></span>
<span data-ttu-id="d0a7b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a7b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0a7b-118">-InputObject</span></span>
<span data-ttu-id="d0a7b-119">Używanie Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d0a7b-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a7b-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d0a7b-120">-Name</span></span>
<span data-ttu-id="d0a7b-121">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a7b-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d0a7b-122">-PeeringName</span></span>
<span data-ttu-id="d0a7b-123">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="d0a7b-124">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="d0a7b-124">-Prefix</span></span>
<span data-ttu-id="d0a7b-125">Prefiks IPv4 sesji</span><span class="sxs-lookup"><span data-stu-id="d0a7b-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="d0a7b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a7b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0a7b-127">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d0a7b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a7b-128">-ResourceId</span></span>
<span data-ttu-id="d0a7b-129">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-129">The resource id string name.</span></span>

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

### <span data-ttu-id="d0a7b-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0a7b-130">-Confirm</span></span>
<span data-ttu-id="d0a7b-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a7b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a7b-132">-WhatIf</span></span>
<span data-ttu-id="d0a7b-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a7b-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a7b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a7b-135">CommonParameters</span></span>
<span data-ttu-id="d0a7b-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a7b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a7b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0a7b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a7b-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a7b-138">INPUTS</span></span>

### <span data-ttu-id="d0a7b-139">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d0a7b-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="d0a7b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d0a7b-140">System.String</span></span>

## <span data-ttu-id="d0a7b-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a7b-141">OUTPUTS</span></span>

### <span data-ttu-id="d0a7b-142">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d0a7b-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d0a7b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0a7b-143">NOTES</span></span>

## <span data-ttu-id="d0a7b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0a7b-144">RELATED LINKS</span></span>
