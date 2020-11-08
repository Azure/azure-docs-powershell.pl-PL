---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224221"
---
# <span data-ttu-id="424f0-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="424f0-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="424f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="424f0-102">SYNOPSIS</span></span>
<span data-ttu-id="424f0-103">Usuwa określoną regułę dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="424f0-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="424f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="424f0-104">SYNTAX</span></span>

### <span data-ttu-id="424f0-105">RulePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="424f0-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424f0-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="424f0-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="424f0-107">DESCRIPTION</span></span>
<span data-ttu-id="424f0-108">Polecenie cmdlet **Remove-AzServiceBusRule** usuwa regułę abonamentu danego tematu.</span><span class="sxs-lookup"><span data-stu-id="424f0-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="424f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="424f0-109">EXAMPLES</span></span>

### <span data-ttu-id="424f0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="424f0-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="424f0-111">Usuwa regułę `SBRule` abonamentu `SBSubscription` określonego tematu `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="424f0-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="424f0-112">Przykład 2: wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="424f0-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="424f0-113">Usuwa regułę dostarczaną za pośrednictwem parametru $inputobject for-Inputobject</span><span class="sxs-lookup"><span data-stu-id="424f0-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="424f0-114">Przykład 3: wejście-korzystanie z połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="424f0-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="424f0-115">Przykład 4: ResourceId — używanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="424f0-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="424f0-116">Przykład 5: ResourceId — używanie wartości ciągu</span><span class="sxs-lookup"><span data-stu-id="424f0-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="424f0-117">Usuwa regułę podaną za pomocą identyfikatora ARM w $resourceid parametru/String dla-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="424f0-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="424f0-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="424f0-118">PARAMETERS</span></span>

### <span data-ttu-id="424f0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="424f0-119">-AsJob</span></span>
<span data-ttu-id="424f0-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="424f0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="424f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424f0-121">-DefaultProfile</span></span>
<span data-ttu-id="424f0-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="424f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424f0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="424f0-123">-Force</span></span>
<span data-ttu-id="424f0-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="424f0-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="424f0-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="424f0-125">-InputObject</span></span>
<span data-ttu-id="424f0-126">Obiekt reguły magistrali usług</span><span class="sxs-lookup"><span data-stu-id="424f0-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="424f0-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="424f0-127">-Name</span></span>
<span data-ttu-id="424f0-128">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="424f0-128">Rule Name</span></span>

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

### <span data-ttu-id="424f0-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="424f0-129">-Namespace</span></span>
<span data-ttu-id="424f0-130">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="424f0-130">Namespace Name</span></span>

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

### <span data-ttu-id="424f0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="424f0-131">-PassThru</span></span>
<span data-ttu-id="424f0-132">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="424f0-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="424f0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424f0-133">-ResourceGroupName</span></span>
<span data-ttu-id="424f0-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="424f0-134">The name of the resource group</span></span>

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

### <span data-ttu-id="424f0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="424f0-135">-ResourceId</span></span>
<span data-ttu-id="424f0-136">Identyfikator zasobu reguły magistrali usług</span><span class="sxs-lookup"><span data-stu-id="424f0-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="424f0-137">-Subscription</span><span class="sxs-lookup"><span data-stu-id="424f0-137">-Subscription</span></span>
<span data-ttu-id="424f0-138">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="424f0-138">Subscription Name</span></span>

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

### <span data-ttu-id="424f0-139">— Temat</span><span class="sxs-lookup"><span data-stu-id="424f0-139">-Topic</span></span>
<span data-ttu-id="424f0-140">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="424f0-140">Topic Name</span></span>

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

### <span data-ttu-id="424f0-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="424f0-141">-Confirm</span></span>
<span data-ttu-id="424f0-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424f0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424f0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424f0-143">-WhatIf</span></span>
<span data-ttu-id="424f0-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424f0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424f0-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="424f0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424f0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424f0-146">CommonParameters</span></span>
<span data-ttu-id="424f0-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424f0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424f0-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424f0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424f0-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="424f0-149">INPUTS</span></span>

### <span data-ttu-id="424f0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="424f0-150">System.String</span></span>

### <span data-ttu-id="424f0-151">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="424f0-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="424f0-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="424f0-152">OUTPUTS</span></span>

### <span data-ttu-id="424f0-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="424f0-153">System.Boolean</span></span>

## <span data-ttu-id="424f0-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="424f0-154">NOTES</span></span>

## <span data-ttu-id="424f0-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="424f0-155">RELATED LINKS</span></span>
