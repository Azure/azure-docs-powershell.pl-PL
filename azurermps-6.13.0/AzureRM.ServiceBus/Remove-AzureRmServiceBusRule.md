---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: dc75d9895d5e56f7cd7915947ff8a63ac54f2a3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546479"
---
# <span data-ttu-id="64f36-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="64f36-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="64f36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64f36-102">SYNOPSIS</span></span>
<span data-ttu-id="64f36-103">Usuwa regułę speficied danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="64f36-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64f36-104">SYNTAX</span></span>

### <span data-ttu-id="64f36-105">RulePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64f36-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f36-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="64f36-106">RuleResourceIdSet</span></span>
```
Remove-AzureRmServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f36-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64f36-107">DESCRIPTION</span></span>
<span data-ttu-id="64f36-108">Polecenie cmdlet **Remove-AzureRmServiceBusRule** usuwa regułę abonamentu danego tematu.</span><span class="sxs-lookup"><span data-stu-id="64f36-108">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="64f36-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64f36-109">EXAMPLES</span></span>

### <span data-ttu-id="64f36-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64f36-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="64f36-111">Usuwa regułę `SBRule` abonamentu `SBSubscription` określonego tematu `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="64f36-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="64f36-112">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="64f36-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="64f36-113">Usuwa regułę dostarczaną za pośrednictwem parametru $inputobject for-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64f36-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="64f36-114">Przykład 2,2-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="64f36-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusRule <params> | Remove-AzureRmServiceBusRule
```

### <span data-ttu-id="64f36-115">Przykład 3,1-ResourceId-używa zmiennej</span><span class="sxs-lookup"><span data-stu-id="64f36-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="64f36-116">Przykład 3,1-ResourceId-używa wartości ciągu</span><span class="sxs-lookup"><span data-stu-id="64f36-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="64f36-117">Usuwa regułę podaną za pomocą identyfikatora ARM w $resourceid parametru/String dla-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="64f36-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="64f36-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64f36-118">PARAMETERS</span></span>

### <span data-ttu-id="64f36-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64f36-119">-AsJob</span></span>
<span data-ttu-id="64f36-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="64f36-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64f36-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f36-121">-DefaultProfile</span></span>
<span data-ttu-id="64f36-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64f36-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64f36-123">-Force</span><span class="sxs-lookup"><span data-stu-id="64f36-123">-Force</span></span>
<span data-ttu-id="64f36-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="64f36-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="64f36-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64f36-125">-InputObject</span></span>
<span data-ttu-id="64f36-126">Obiekt reguły magistrali usług</span><span class="sxs-lookup"><span data-stu-id="64f36-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="64f36-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64f36-127">-Name</span></span>
<span data-ttu-id="64f36-128">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="64f36-128">Rule Name</span></span>

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

### <span data-ttu-id="64f36-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="64f36-129">-Namespace</span></span>
<span data-ttu-id="64f36-130">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="64f36-130">Namespace Name</span></span>

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

### <span data-ttu-id="64f36-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64f36-131">-PassThru</span></span>
<span data-ttu-id="64f36-132">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="64f36-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="64f36-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f36-133">-ResourceGroupName</span></span>
<span data-ttu-id="64f36-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="64f36-134">The name of the resource group</span></span>

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

### <span data-ttu-id="64f36-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64f36-135">-ResourceId</span></span>
<span data-ttu-id="64f36-136">Identyfikator zasobu reguły magistrali usług</span><span class="sxs-lookup"><span data-stu-id="64f36-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="64f36-137">-Subscription</span><span class="sxs-lookup"><span data-stu-id="64f36-137">-Subscription</span></span>
<span data-ttu-id="64f36-138">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="64f36-138">Subscription Name</span></span>

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

### <span data-ttu-id="64f36-139">— Temat</span><span class="sxs-lookup"><span data-stu-id="64f36-139">-Topic</span></span>
<span data-ttu-id="64f36-140">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="64f36-140">Topic Name</span></span>

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

### <span data-ttu-id="64f36-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64f36-141">-Confirm</span></span>
<span data-ttu-id="64f36-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64f36-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f36-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f36-143">-WhatIf</span></span>
<span data-ttu-id="64f36-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64f36-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f36-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64f36-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f36-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f36-146">CommonParameters</span></span>
<span data-ttu-id="64f36-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f36-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f36-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f36-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f36-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64f36-149">INPUTS</span></span>

### <span data-ttu-id="64f36-150">System. String</span><span class="sxs-lookup"><span data-stu-id="64f36-150">System.String</span></span>

### <span data-ttu-id="64f36-151">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="64f36-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="64f36-152">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="64f36-152">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="64f36-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64f36-153">OUTPUTS</span></span>

### <span data-ttu-id="64f36-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64f36-154">System.Boolean</span></span>

## <span data-ttu-id="64f36-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64f36-155">NOTES</span></span>

## <span data-ttu-id="64f36-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64f36-156">RELATED LINKS</span></span>
