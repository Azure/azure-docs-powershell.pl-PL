---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964721"
---
# <span data-ttu-id="e0614-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e0614-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="e0614-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0614-102">SYNOPSIS</span></span>
<span data-ttu-id="e0614-103">Usuwa domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0614-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="e0614-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0614-104">SYNTAX</span></span>

### <span data-ttu-id="e0614-105">DomainNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e0614-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0614-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0614-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0614-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0614-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0614-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0614-108">DESCRIPTION</span></span>
<span data-ttu-id="e0614-109">Usuwa domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0614-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="e0614-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0614-110">EXAMPLES</span></span>

### <span data-ttu-id="e0614-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0614-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="e0614-112">Usuwa domenę domeny siatki \` zdarzeń (1) w \` grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="e0614-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e0614-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e0614-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="e0614-114">Usuwa domenę domeny siatki \` zdarzeń (1) w \` grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="e0614-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e0614-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0614-115">PARAMETERS</span></span>

### <span data-ttu-id="e0614-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0614-116">-DefaultProfile</span></span>
<span data-ttu-id="e0614-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0614-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0614-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0614-118">-InputObject</span></span>
<span data-ttu-id="e0614-119">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e0614-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0614-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0614-120">-Name</span></span>
<span data-ttu-id="e0614-121">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e0614-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0614-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0614-122">-PassThru</span></span>
<span data-ttu-id="e0614-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e0614-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e0614-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0614-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0614-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0614-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0614-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0614-126">-ResourceId</span></span>
<span data-ttu-id="e0614-127">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e0614-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0614-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0614-128">-Confirm</span></span>
<span data-ttu-id="e0614-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0614-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0614-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0614-130">-WhatIf</span></span>
<span data-ttu-id="e0614-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0614-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0614-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0614-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0614-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0614-133">CommonParameters</span></span>
<span data-ttu-id="e0614-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0614-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0614-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0614-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0614-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0614-136">INPUTS</span></span>

### <span data-ttu-id="e0614-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e0614-137">System.String</span></span>

### <span data-ttu-id="e0614-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="e0614-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="e0614-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0614-139">OUTPUTS</span></span>

### <span data-ttu-id="e0614-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0614-140">System.Boolean</span></span>

## <span data-ttu-id="e0614-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0614-141">NOTES</span></span>

## <span data-ttu-id="e0614-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0614-142">RELATED LINKS</span></span>
