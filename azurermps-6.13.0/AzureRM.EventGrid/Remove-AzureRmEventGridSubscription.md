---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 82d386fb0834db3de03d5692ad8b7a241b6eed90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546628"
---
# <span data-ttu-id="23cb0-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="23cb0-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="23cb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="23cb0-103">Usuwa subskrypcję zdarzeń w siatce zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="23cb0-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23cb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23cb0-104">SYNTAX</span></span>

### <span data-ttu-id="23cb0-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23cb0-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cb0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="23cb0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cb0-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="23cb0-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cb0-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23cb0-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23cb0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="23cb0-109">DESCRIPTION</span></span>
<span data-ttu-id="23cb0-110">Usuwa subskrypcję zdarzeń w siatce zdarzeń platformy Azure dla tematu siatka zdarzeń Azure, zasób, subskrypcję platformy Azure lub grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="23cb0-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="23cb0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23cb0-111">EXAMPLES</span></span>

### <span data-ttu-id="23cb0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23cb0-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="23cb0-113">Usuwa EventSubscription1 abonamentu \` zdarzeń \` do tematu siatka zdarzeń usługi Azure \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="23cb0-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="23cb0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23cb0-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="23cb0-115">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="23cb0-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="23cb0-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="23cb0-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="23cb0-117">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do domyślnej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="23cb0-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="23cb0-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="23cb0-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="23cb0-119">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do obszaru nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23cb0-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="23cb0-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="23cb0-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="23cb0-121">Usuwa EventSubscription1 subskrypcji zdarzeń \` \` do tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23cb0-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="23cb0-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23cb0-122">PARAMETERS</span></span>

### <span data-ttu-id="23cb0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cb0-123">-DefaultProfile</span></span>
<span data-ttu-id="23cb0-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="23cb0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23cb0-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="23cb0-125">-EventSubscriptionName</span></span>
<span data-ttu-id="23cb0-126">Nazwa subskrypcji zdarzenia, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="23cb0-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb0-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23cb0-127">-InputObject</span></span>
<span data-ttu-id="23cb0-128">Obiekt EventSubscription EventGrid.</span><span class="sxs-lookup"><span data-stu-id="23cb0-128">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23cb0-129">-PassThru</span></span>
<span data-ttu-id="23cb0-130">Zwraca stan operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="23cb0-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="23cb0-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="23cb0-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23cb0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cb0-132">-ResourceGroupName</span></span>
<span data-ttu-id="23cb0-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23cb0-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23cb0-134">-ResourceId</span></span>
<span data-ttu-id="23cb0-135">Identyfikator zasobu, którego abonament zdarzenia należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="23cb0-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb0-136">-Tematname</span><span class="sxs-lookup"><span data-stu-id="23cb0-136">-TopicName</span></span>
<span data-ttu-id="23cb0-137">Nazwa tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23cb0-137">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb0-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23cb0-138">-Confirm</span></span>
<span data-ttu-id="23cb0-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cb0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cb0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cb0-140">-WhatIf</span></span>
<span data-ttu-id="23cb0-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cb0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cb0-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23cb0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cb0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cb0-143">CommonParameters</span></span>
<span data-ttu-id="23cb0-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cb0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cb0-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cb0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cb0-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cb0-146">INPUTS</span></span>

### <span data-ttu-id="23cb0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="23cb0-147">System.String</span></span>

### <span data-ttu-id="23cb0-148">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="23cb0-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="23cb0-149">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23cb0-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="23cb0-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23cb0-150">OUTPUTS</span></span>

### <span data-ttu-id="23cb0-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23cb0-151">System.Boolean</span></span>

## <span data-ttu-id="23cb0-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23cb0-152">NOTES</span></span>

## <span data-ttu-id="23cb0-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cb0-153">RELATED LINKS</span></span>
