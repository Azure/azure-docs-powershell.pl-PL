---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: 8cbfe51ac9c4a415672bc96e18e61f5a82a454cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705436"
---
# <span data-ttu-id="55134-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="55134-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="55134-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55134-102">SYNOPSIS</span></span>
<span data-ttu-id="55134-103">Usuwa określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="55134-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="55134-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55134-104">SYNTAX</span></span>

### <span data-ttu-id="55134-105">ConsumergroupPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55134-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55134-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55134-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55134-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55134-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55134-108">Opis</span><span class="sxs-lookup"><span data-stu-id="55134-108">DESCRIPTION</span></span>
<span data-ttu-id="55134-109">Polecenie cmdlet Remove-AzEventHubConsumerGroup usuwa i usuwa określoną grupę klientów z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="55134-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="55134-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55134-110">EXAMPLES</span></span>

### <span data-ttu-id="55134-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55134-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="55134-112">Usuwa MyConsumerGroupName grupy konsumenckiej \` \` z MyEventHubName centrum zdarzeń \` \` i zakresu do \` obszaru nazw moja przestrzeń nazw \` .</span><span class="sxs-lookup"><span data-stu-id="55134-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="55134-113">Przykład 2,1-wejście-za pomocą zmiennej</span><span class="sxs-lookup"><span data-stu-id="55134-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="55134-114">Przykład 2,2-Inputobject-przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="55134-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="55134-115">Przykład 3,1-ResourceId używający zmiennej</span><span class="sxs-lookup"><span data-stu-id="55134-115">Example 3.1 - ResourceId Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="55134-116">Przykład 3,2-ResourceId przy użyciu ciągu</span><span class="sxs-lookup"><span data-stu-id="55134-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="55134-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55134-117">PARAMETERS</span></span>

### <span data-ttu-id="55134-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55134-118">-AsJob</span></span>
<span data-ttu-id="55134-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="55134-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55134-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55134-120">-DefaultProfile</span></span>
<span data-ttu-id="55134-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55134-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55134-122">— EventHub</span><span class="sxs-lookup"><span data-stu-id="55134-122">-EventHub</span></span>
<span data-ttu-id="55134-123">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="55134-123">EventHub Name</span></span>

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

### <span data-ttu-id="55134-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55134-124">-InputObject</span></span>
<span data-ttu-id="55134-125">Obiekt odbiorcy</span><span class="sxs-lookup"><span data-stu-id="55134-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="55134-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55134-126">-Name</span></span>
<span data-ttu-id="55134-127">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="55134-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="55134-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="55134-128">-Namespace</span></span>
<span data-ttu-id="55134-129">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="55134-129">Namespace Name</span></span>

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

### <span data-ttu-id="55134-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55134-130">-PassThru</span></span>
<span data-ttu-id="55134-131">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="55134-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="55134-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55134-132">-ResourceGroupName</span></span>
<span data-ttu-id="55134-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55134-133">Resource Group Name</span></span>

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

### <span data-ttu-id="55134-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55134-134">-ResourceId</span></span>
<span data-ttu-id="55134-135">Identyfikator zasobu w ramach odbiorcy</span><span class="sxs-lookup"><span data-stu-id="55134-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="55134-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55134-136">-Confirm</span></span>
<span data-ttu-id="55134-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55134-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55134-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55134-138">-WhatIf</span></span>
<span data-ttu-id="55134-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55134-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55134-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55134-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55134-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55134-141">CommonParameters</span></span>
<span data-ttu-id="55134-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55134-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55134-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55134-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55134-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55134-144">INPUTS</span></span>

### <span data-ttu-id="55134-145">System. String</span><span class="sxs-lookup"><span data-stu-id="55134-145">System.String</span></span>

### <span data-ttu-id="55134-146">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="55134-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="55134-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55134-147">OUTPUTS</span></span>

### <span data-ttu-id="55134-148">System. void</span><span class="sxs-lookup"><span data-stu-id="55134-148">System.Void</span></span>

## <span data-ttu-id="55134-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55134-149">NOTES</span></span>

## <span data-ttu-id="55134-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55134-150">RELATED LINKS</span></span>
