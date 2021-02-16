---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179170"
---
# <span data-ttu-id="e770e-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="e770e-101">New-AzPeeringService</span></span>

## <span data-ttu-id="e770e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e770e-102">SYNOPSIS</span></span>
<span data-ttu-id="e770e-103">Tworzy nową usługę komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e770e-103">Creates a new peering service.</span></span>

## <span data-ttu-id="e770e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e770e-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e770e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e770e-105">DESCRIPTION</span></span>
<span data-ttu-id="e770e-106">Tworzy usługę komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e770e-106">Creates peering service.</span></span>

## <span data-ttu-id="e770e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e770e-107">EXAMPLES</span></span>

### <span data-ttu-id="e770e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e770e-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="e770e-109">Tworzy obiekt usługi komunikacji równorzędnej z dostawcą i lokalizacją komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e770e-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="e770e-110">Używanie w sprzężęcie z `Get-AzPeeringServiceProvider` i `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="e770e-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="e770e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e770e-111">PARAMETERS</span></span>

### <span data-ttu-id="e770e-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e770e-112">-AsJob</span></span>
<span data-ttu-id="e770e-113">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="e770e-113">Run in the background.</span></span>

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

### <span data-ttu-id="e770e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e770e-114">-DefaultProfile</span></span>
<span data-ttu-id="e770e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e770e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e770e-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e770e-116">-Name</span></span>
<span data-ttu-id="e770e-117">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e770e-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e770e-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e770e-118">-PeeringLocation</span></span>
<span data-ttu-id="e770e-119">Lokalizacja fizyczna inna niż region platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e770e-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="e770e-120">Użyj Get-AzPeeringServiceLocation [-Country] <country></span><span class="sxs-lookup"><span data-stu-id="e770e-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="e770e-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="e770e-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="e770e-122">Nazwa usługodawca komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e770e-122">The peering service provider name.</span></span>
<span data-ttu-id="e770e-123">Używanie Get-AzPeeringServiceProvider cmdlet dla listy</span><span class="sxs-lookup"><span data-stu-id="e770e-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e770e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e770e-124">-ResourceGroupName</span></span>
<span data-ttu-id="e770e-125">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e770e-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e770e-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="e770e-126">-Tag</span></span>
<span data-ttu-id="e770e-127">Tagi do skojarzenia z usługą Microsoft InputObject.</span><span class="sxs-lookup"><span data-stu-id="e770e-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e770e-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e770e-128">-Confirm</span></span>
<span data-ttu-id="e770e-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e770e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e770e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e770e-130">-WhatIf</span></span>
<span data-ttu-id="e770e-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e770e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e770e-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e770e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e770e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e770e-133">CommonParameters</span></span>
<span data-ttu-id="e770e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e770e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e770e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e770e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e770e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e770e-136">INPUTS</span></span>

### <span data-ttu-id="e770e-137">Brak</span><span class="sxs-lookup"><span data-stu-id="e770e-137">None</span></span>

## <span data-ttu-id="e770e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e770e-138">OUTPUTS</span></span>

### <span data-ttu-id="e770e-139">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="e770e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="e770e-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e770e-140">NOTES</span></span>

## <span data-ttu-id="e770e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e770e-141">RELATED LINKS</span></span>
