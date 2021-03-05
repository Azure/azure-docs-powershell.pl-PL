---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 517044655ee1af7748906e2f9e9787c99813c6a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991201"
---
# <span data-ttu-id="e3e39-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e3e39-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="e3e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e39-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e39-103">Usuwa temat domeny siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e39-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="e3e39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3e39-104">SYNTAX</span></span>

### <span data-ttu-id="e3e39-105">DomainTopicNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e3e39-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e39-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e39-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e39-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e39-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e39-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3e39-108">DESCRIPTION</span></span>
<span data-ttu-id="e3e39-109">Usuwa temat domeny siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e39-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="e3e39-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3e39-110">EXAMPLES</span></span>

### <span data-ttu-id="e3e39-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3e39-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="e3e39-112">Usuwa temat domeny siatki zdarzeń \` (temat1) w \` obszarze Domain \` Domain1 \` (Domena domeny1) w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="e3e39-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e3e39-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e3e39-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="e3e39-114">Usuwa temat domeny siatki zdarzeń \` (temat1) w \` obszarze Domain \` Domain1 \` (Domena domeny1) w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="e3e39-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e3e39-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3e39-115">PARAMETERS</span></span>

### <span data-ttu-id="e3e39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e39-116">-DefaultProfile</span></span>
<span data-ttu-id="e3e39-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e39-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e3e39-118">-DomainName</span></span>
<span data-ttu-id="e3e39-119">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e3e39-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e39-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3e39-120">-InputObject</span></span>
<span data-ttu-id="e3e39-121">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e3e39-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e39-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3e39-122">-Name</span></span>
<span data-ttu-id="e3e39-123">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e3e39-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e39-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3e39-124">-PassThru</span></span>
<span data-ttu-id="e3e39-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e3e39-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e3e39-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e39-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3e39-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3e39-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e39-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e39-128">-ResourceId</span></span>
<span data-ttu-id="e3e39-129">Identyfikator zasobu reprezentujący temat domeny siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e3e39-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e39-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3e39-130">-Confirm</span></span>
<span data-ttu-id="e3e39-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3e39-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e39-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e39-132">-WhatIf</span></span>
<span data-ttu-id="e3e39-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3e39-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e39-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e3e39-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e39-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e39-135">CommonParameters</span></span>
<span data-ttu-id="e3e39-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e39-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e39-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3e39-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e39-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3e39-138">INPUTS</span></span>

### <span data-ttu-id="e3e39-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e3e39-139">System.String</span></span>

### <span data-ttu-id="e3e39-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e3e39-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="e3e39-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3e39-141">OUTPUTS</span></span>

### <span data-ttu-id="e3e39-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3e39-142">System.Boolean</span></span>

## <span data-ttu-id="e3e39-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3e39-143">NOTES</span></span>

## <span data-ttu-id="e3e39-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3e39-144">RELATED LINKS</span></span>
