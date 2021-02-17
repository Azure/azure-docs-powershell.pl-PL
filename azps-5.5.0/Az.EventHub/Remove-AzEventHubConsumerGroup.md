---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188435"
---
# <span data-ttu-id="164af-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="164af-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="164af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="164af-102">SYNOPSIS</span></span>
<span data-ttu-id="164af-103">Usuwa określoną grupę klientów centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="164af-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="164af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="164af-104">SYNTAX</span></span>

### <span data-ttu-id="164af-105">ConsumergroupPropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="164af-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="164af-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="164af-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="164af-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="164af-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="164af-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="164af-108">DESCRIPTION</span></span>
<span data-ttu-id="164af-109">Polecenie Remove-AzEventHubConsumerGroup cmdlet usuwa określoną grupę klientów z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="164af-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="164af-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="164af-110">EXAMPLES</span></span>

### <span data-ttu-id="164af-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="164af-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="164af-112">Usuwa grupę konsumencką \` MyConsumerGroupName z centrum zdarzeń \` \` MyEventHubName (nazwa_ obszaru nazw \` \` MyNamespaceName). \`</span><span class="sxs-lookup"><span data-stu-id="164af-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="164af-113">Przykład 2. InputObject — używanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="164af-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="164af-114">Przykład 3. InputObject — używanie funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="164af-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="164af-115">Przykład 4. Użycie zmiennej ResourceId</span><span class="sxs-lookup"><span data-stu-id="164af-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="164af-116">Przykład 5. Użycie ciągu ResourceId</span><span class="sxs-lookup"><span data-stu-id="164af-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="164af-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="164af-117">PARAMETERS</span></span>

### <span data-ttu-id="164af-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="164af-118">-AsJob</span></span>
<span data-ttu-id="164af-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="164af-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="164af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164af-120">-DefaultProfile</span></span>
<span data-ttu-id="164af-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="164af-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="164af-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="164af-122">-EventHub</span></span>
<span data-ttu-id="164af-123">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="164af-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164af-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="164af-124">-InputObject</span></span>
<span data-ttu-id="164af-125">Obiekt ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="164af-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="164af-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="164af-126">-Name</span></span>
<span data-ttu-id="164af-127">Nazwa grupy konsumenckiej</span><span class="sxs-lookup"><span data-stu-id="164af-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164af-128">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="164af-128">-Namespace</span></span>
<span data-ttu-id="164af-129">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="164af-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164af-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="164af-130">-PassThru</span></span>
<span data-ttu-id="164af-131">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="164af-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="164af-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="164af-132">-ResourceGroupName</span></span>
<span data-ttu-id="164af-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="164af-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164af-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="164af-134">-ResourceId</span></span>
<span data-ttu-id="164af-135">Identyfikator zasobu ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="164af-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="164af-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="164af-136">-Confirm</span></span>
<span data-ttu-id="164af-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="164af-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="164af-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="164af-138">-WhatIf</span></span>
<span data-ttu-id="164af-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="164af-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="164af-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="164af-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="164af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164af-141">CommonParameters</span></span>
<span data-ttu-id="164af-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="164af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164af-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="164af-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164af-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="164af-144">INPUTS</span></span>

### <span data-ttu-id="164af-145">System.String</span><span class="sxs-lookup"><span data-stu-id="164af-145">System.String</span></span>

### <span data-ttu-id="164af-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="164af-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="164af-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="164af-147">OUTPUTS</span></span>

### <span data-ttu-id="164af-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="164af-148">System.Void</span></span>

## <span data-ttu-id="164af-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="164af-149">NOTES</span></span>

## <span data-ttu-id="164af-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="164af-150">RELATED LINKS</span></span>
