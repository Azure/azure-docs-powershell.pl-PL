---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545364"
---
# <span data-ttu-id="0e382-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0e382-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0e382-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e382-102">SYNOPSIS</span></span>
<span data-ttu-id="0e382-103">Usuwa określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="0e382-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e382-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e382-104">SYNTAX</span></span>

### <span data-ttu-id="0e382-105">ConsumergroupPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e382-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e382-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e382-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e382-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e382-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e382-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0e382-108">DESCRIPTION</span></span>
<span data-ttu-id="0e382-109">Polecenie cmdlet Remove-AzureRmEventHubConsumerGroup usuwa i usuwa określoną grupę klientów z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="0e382-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="0e382-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e382-110">EXAMPLES</span></span>

### <span data-ttu-id="0e382-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e382-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="0e382-112">Usuwa MyConsumerGroupName grupy konsumenckiej \` \` z MyEventHubName centrum zdarzeń \` \` i zakresu do \` obszaru nazw moja przestrzeń nazw \` .</span><span class="sxs-lookup"><span data-stu-id="0e382-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="0e382-113">Przykład 2,1-wejście-za pomocą zmiennej</span><span class="sxs-lookup"><span data-stu-id="0e382-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="0e382-114">Przykład 2,2-Inputobject-przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="0e382-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="0e382-115">Przykład 3,1-ResourceId przy użyciu Vairable</span><span class="sxs-lookup"><span data-stu-id="0e382-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="0e382-116">Przykład 3,2-ResourceId przy użyciu ciągu</span><span class="sxs-lookup"><span data-stu-id="0e382-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="0e382-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e382-117">PARAMETERS</span></span>

### <span data-ttu-id="0e382-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e382-118">-AsJob</span></span>
<span data-ttu-id="0e382-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0e382-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e382-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e382-120">-DefaultProfile</span></span>
<span data-ttu-id="0e382-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e382-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e382-122">— EventHub</span><span class="sxs-lookup"><span data-stu-id="0e382-122">-EventHub</span></span>
<span data-ttu-id="0e382-123">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="0e382-123">EventHub Name</span></span>

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

### <span data-ttu-id="0e382-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e382-124">-InputObject</span></span>
<span data-ttu-id="0e382-125">Obiekt odbiorcy</span><span class="sxs-lookup"><span data-stu-id="0e382-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="0e382-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e382-126">-Name</span></span>
<span data-ttu-id="0e382-127">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="0e382-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="0e382-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e382-128">-Namespace</span></span>
<span data-ttu-id="0e382-129">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0e382-129">Namespace Name</span></span>

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

### <span data-ttu-id="0e382-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e382-130">-PassThru</span></span>
<span data-ttu-id="0e382-131">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="0e382-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0e382-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e382-132">-ResourceGroupName</span></span>
<span data-ttu-id="0e382-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0e382-133">Resource Group Name</span></span>

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

### <span data-ttu-id="0e382-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e382-134">-ResourceId</span></span>
<span data-ttu-id="0e382-135">Identyfikator zasobu w ramach odbiorcy</span><span class="sxs-lookup"><span data-stu-id="0e382-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="0e382-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e382-136">-Confirm</span></span>
<span data-ttu-id="0e382-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e382-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e382-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e382-138">-WhatIf</span></span>
<span data-ttu-id="0e382-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e382-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e382-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e382-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e382-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e382-141">CommonParameters</span></span>
<span data-ttu-id="0e382-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e382-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e382-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e382-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e382-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e382-144">INPUTS</span></span>

### <span data-ttu-id="0e382-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0e382-145">System.String</span></span>

### <span data-ttu-id="0e382-146">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="0e382-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="0e382-147">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0e382-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0e382-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e382-148">OUTPUTS</span></span>

### <span data-ttu-id="0e382-149">System. void</span><span class="sxs-lookup"><span data-stu-id="0e382-149">System.Void</span></span>

## <span data-ttu-id="0e382-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e382-150">NOTES</span></span>

## <span data-ttu-id="0e382-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e382-151">RELATED LINKS</span></span>
