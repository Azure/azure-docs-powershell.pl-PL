---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015898"
---
# <span data-ttu-id="1aa97-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="1aa97-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="1aa97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa97-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa97-103">Usuwa określoną regułę danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1aa97-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="1aa97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1aa97-104">SYNTAX</span></span>

### <span data-ttu-id="1aa97-105">RulePropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="1aa97-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa97-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1aa97-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa97-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1aa97-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa97-108">Polecenie **cmdlet Remove-AzServiceBusRule** usuwa regułę subskrypcji danego tematu.</span><span class="sxs-lookup"><span data-stu-id="1aa97-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="1aa97-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1aa97-109">EXAMPLES</span></span>

### <span data-ttu-id="1aa97-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1aa97-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="1aa97-111">Usuwa regułę `SBRule` subskrypcji `SBSubscription` określonego `SBTopic` tematu.</span><span class="sxs-lookup"><span data-stu-id="1aa97-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="1aa97-112">Przykład 2. InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="1aa97-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="1aa97-113">Usuwa regułę podaną za pośrednictwem $inputobject parametru -InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa97-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="1aa97-114">Przykład 3. InputObject — używanie funkcji rurowych:</span><span class="sxs-lookup"><span data-stu-id="1aa97-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="1aa97-115">Przykład 4. ResourceId — używanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="1aa97-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="1aa97-116">Przykład 5. ZasóbId — używanie wartości ciągu</span><span class="sxs-lookup"><span data-stu-id="1aa97-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="1aa97-117">Usuwa regułę z identyfikatora ARM w ciągu $resourceid/string dla parametru -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa97-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="1aa97-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aa97-118">PARAMETERS</span></span>

### <span data-ttu-id="1aa97-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1aa97-119">-AsJob</span></span>
<span data-ttu-id="1aa97-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1aa97-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1aa97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa97-121">-DefaultProfile</span></span>
<span data-ttu-id="1aa97-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1aa97-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa97-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1aa97-123">-Force</span></span>
<span data-ttu-id="1aa97-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1aa97-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1aa97-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa97-125">-InputObject</span></span>
<span data-ttu-id="1aa97-126">Obiekt Service Bus Rule</span><span class="sxs-lookup"><span data-stu-id="1aa97-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1aa97-127">-Name</span></span>
<span data-ttu-id="1aa97-128">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="1aa97-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-129">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="1aa97-129">-Namespace</span></span>
<span data-ttu-id="1aa97-130">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="1aa97-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aa97-131">-PassThru</span></span>
<span data-ttu-id="1aa97-132">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="1aa97-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1aa97-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa97-133">-ResourceGroupName</span></span>
<span data-ttu-id="1aa97-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1aa97-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa97-135">-ResourceId</span></span>
<span data-ttu-id="1aa97-136">Identyfikator zasobu reguły autobusu usługowego</span><span class="sxs-lookup"><span data-stu-id="1aa97-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-137">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="1aa97-137">-Subscription</span></span>
<span data-ttu-id="1aa97-138">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1aa97-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-139">— Temat</span><span class="sxs-lookup"><span data-stu-id="1aa97-139">-Topic</span></span>
<span data-ttu-id="1aa97-140">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="1aa97-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa97-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1aa97-141">-Confirm</span></span>
<span data-ttu-id="1aa97-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1aa97-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa97-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa97-143">-WhatIf</span></span>
<span data-ttu-id="1aa97-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aa97-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa97-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1aa97-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa97-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa97-146">CommonParameters</span></span>
<span data-ttu-id="1aa97-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa97-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa97-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa97-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa97-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aa97-149">INPUTS</span></span>

### <span data-ttu-id="1aa97-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1aa97-150">System.String</span></span>

### <span data-ttu-id="1aa97-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="1aa97-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1aa97-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aa97-152">OUTPUTS</span></span>

### <span data-ttu-id="1aa97-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1aa97-153">System.Boolean</span></span>

## <span data-ttu-id="1aa97-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1aa97-154">NOTES</span></span>

## <span data-ttu-id="1aa97-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1aa97-155">RELATED LINKS</span></span>
