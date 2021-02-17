---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188475"
---
# <span data-ttu-id="ddd34-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ddd34-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="ddd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd34-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd34-103">Usuwa temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd34-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ddd34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddd34-104">SYNTAX</span></span>

### <span data-ttu-id="ddd34-105">TopicNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ddd34-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd34-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd34-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd34-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd34-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd34-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddd34-108">DESCRIPTION</span></span>
<span data-ttu-id="ddd34-109">Usuwa temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd34-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ddd34-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddd34-110">EXAMPLES</span></span>

### <span data-ttu-id="ddd34-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ddd34-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="ddd34-112">Usuwa temat Siatka zdarzeń \` ( \` Temat1) w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="ddd34-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ddd34-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ddd34-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="ddd34-114">Usuwa temat Siatka zdarzeń \` ( \` Temat1) w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="ddd34-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ddd34-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddd34-115">PARAMETERS</span></span>

### <span data-ttu-id="ddd34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd34-116">-DefaultProfile</span></span>
<span data-ttu-id="ddd34-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ddd34-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddd34-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddd34-118">-InputObject</span></span>
<span data-ttu-id="ddd34-119">Obiekt tematu aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ddd34-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd34-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddd34-120">-Name</span></span>
<span data-ttu-id="ddd34-121">Nazwa tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ddd34-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd34-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddd34-122">-PassThru</span></span>
<span data-ttu-id="ddd34-123">Zwraca stan operacji Usuń.</span><span class="sxs-lookup"><span data-stu-id="ddd34-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ddd34-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ddd34-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ddd34-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd34-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddd34-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ddd34-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd34-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd34-127">-ResourceId</span></span>
<span data-ttu-id="ddd34-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ddd34-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="ddd34-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddd34-129">-Confirm</span></span>
<span data-ttu-id="ddd34-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddd34-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd34-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd34-131">-WhatIf</span></span>
<span data-ttu-id="ddd34-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd34-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd34-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddd34-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd34-134">CommonParameters</span></span>
<span data-ttu-id="ddd34-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd34-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddd34-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd34-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddd34-137">INPUTS</span></span>

### <span data-ttu-id="ddd34-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ddd34-138">System.String</span></span>

### <span data-ttu-id="ddd34-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="ddd34-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ddd34-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddd34-140">OUTPUTS</span></span>

### <span data-ttu-id="ddd34-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd34-141">System.Boolean</span></span>

## <span data-ttu-id="ddd34-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddd34-142">NOTES</span></span>

## <span data-ttu-id="ddd34-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddd34-143">RELATED LINKS</span></span>
