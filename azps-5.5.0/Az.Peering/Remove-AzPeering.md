---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202258"
---
# <span data-ttu-id="e08ab-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e08ab-101">Remove-AzPeering</span></span>

## <span data-ttu-id="e08ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e08ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e08ab-103">Usuwanie lub usuwanie komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e08ab-103">Delete or remove a peering.</span></span> <span data-ttu-id="e08ab-104">Spowoduje to usunięcie wszystkich zasobów dzieci lub alertów o zasobie.</span><span class="sxs-lookup"><span data-stu-id="e08ab-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="e08ab-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e08ab-105">SYNTAX</span></span>

### <span data-ttu-id="e08ab-106">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="e08ab-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ab-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e08ab-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ab-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e08ab-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08ab-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e08ab-109">DESCRIPTION</span></span>
<span data-ttu-id="e08ab-110">Perminentnie usuń zasób komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e08ab-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="e08ab-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e08ab-111">EXAMPLES</span></span>

### <span data-ttu-id="e08ab-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e08ab-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="e08ab-113">Usuwanie komunikacji równorzędnej według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="e08ab-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="e08ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e08ab-114">PARAMETERS</span></span>

### <span data-ttu-id="e08ab-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e08ab-115">-AsJob</span></span>
<span data-ttu-id="e08ab-116">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="e08ab-116">Run in the background.</span></span>

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

### <span data-ttu-id="e08ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08ab-117">-DefaultProfile</span></span>
<span data-ttu-id="e08ab-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e08ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e08ab-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e08ab-119">-Force</span></span>
<span data-ttu-id="e08ab-120">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="e08ab-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="e08ab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e08ab-121">-InputObject</span></span>
<span data-ttu-id="e08ab-122">Użyj Get-AzPeering, aby pobrać ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="e08ab-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e08ab-123">-Name</span></span>
<span data-ttu-id="e08ab-124">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e08ab-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e08ab-125">-PassThru</span></span>
<span data-ttu-id="e08ab-126">Zwracanie wartości prawda, jeśli są ukończone</span><span class="sxs-lookup"><span data-stu-id="e08ab-126">Return true if complete</span></span>

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

### <span data-ttu-id="e08ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="e08ab-128">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e08ab-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e08ab-129">-ResourceId</span></span>
<span data-ttu-id="e08ab-130">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="e08ab-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e08ab-131">-Confirm</span></span>
<span data-ttu-id="e08ab-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e08ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08ab-133">-WhatIf</span></span>
<span data-ttu-id="e08ab-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e08ab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e08ab-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e08ab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08ab-136">CommonParameters</span></span>
<span data-ttu-id="e08ab-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e08ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08ab-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e08ab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08ab-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e08ab-139">INPUTS</span></span>

### <span data-ttu-id="e08ab-140">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e08ab-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e08ab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e08ab-141">System.String</span></span>

## <span data-ttu-id="e08ab-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e08ab-142">OUTPUTS</span></span>

### <span data-ttu-id="e08ab-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e08ab-143">System.Boolean</span></span>

## <span data-ttu-id="e08ab-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e08ab-144">NOTES</span></span>

## <span data-ttu-id="e08ab-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e08ab-145">RELATED LINKS</span></span>
