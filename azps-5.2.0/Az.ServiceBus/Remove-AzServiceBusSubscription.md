---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345742"
---
# <span data-ttu-id="594c4-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="594c4-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="594c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="594c4-102">SYNOPSIS</span></span>
<span data-ttu-id="594c4-103">Usuwa subskrypcję tematu z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="594c4-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="594c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="594c4-104">SYNTAX</span></span>

### <span data-ttu-id="594c4-105">SubscriptionPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="594c4-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="594c4-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="594c4-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594c4-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="594c4-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594c4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="594c4-108">DESCRIPTION</span></span>
<span data-ttu-id="594c4-109">Polecenie cmdlet **Remove-AzServiceBusSubscription** usuwa abonament do tematu z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="594c4-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="594c4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="594c4-110">EXAMPLES</span></span>

### <span data-ttu-id="594c4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="594c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="594c4-112">Usuwa subskrypcję `SB-TopicSubscription-Example1` tematu `SB-Topic_exampl1` w określonym obszarze nazw magistrali usług `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="594c4-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="594c4-113">Przykład 2: wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="594c4-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="594c4-114">Przykład 3: wejście-korzystanie z połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="594c4-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="594c4-115">Przykład 4: Identyfikator ResourceId używający zmiennej:</span><span class="sxs-lookup"><span data-stu-id="594c4-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="594c4-116">Przykład 5: Identyfikator zasobu ResourceId przy użyciu wartości ciągu:</span><span class="sxs-lookup"><span data-stu-id="594c4-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="594c4-117">Usuwa abonament podany za pośrednictwem identyfikatora ARM w $resourceid parametru/String dla-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="594c4-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="594c4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="594c4-118">PARAMETERS</span></span>

### <span data-ttu-id="594c4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="594c4-119">-AsJob</span></span>
<span data-ttu-id="594c4-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="594c4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="594c4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594c4-121">-DefaultProfile</span></span>
<span data-ttu-id="594c4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="594c4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594c4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="594c4-123">-InputObject</span></span>
<span data-ttu-id="594c4-124">Obiekt subskrypcji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="594c4-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="594c4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="594c4-125">-Name</span></span>
<span data-ttu-id="594c4-126">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="594c4-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="594c4-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="594c4-127">-Namespace</span></span>
<span data-ttu-id="594c4-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="594c4-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="594c4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="594c4-129">-PassThru</span></span>
<span data-ttu-id="594c4-130">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="594c4-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="594c4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594c4-131">-ResourceGroupName</span></span>
<span data-ttu-id="594c4-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="594c4-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="594c4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="594c4-133">-ResourceId</span></span>
<span data-ttu-id="594c4-134">Identyfikator zasobu subskrypcji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="594c4-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="594c4-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="594c4-135">-Topic</span></span>
<span data-ttu-id="594c4-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="594c4-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="594c4-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="594c4-137">-Confirm</span></span>
<span data-ttu-id="594c4-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="594c4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="594c4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="594c4-139">-WhatIf</span></span>
<span data-ttu-id="594c4-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="594c4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="594c4-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="594c4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="594c4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594c4-142">CommonParameters</span></span>
<span data-ttu-id="594c4-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="594c4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594c4-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="594c4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594c4-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="594c4-145">INPUTS</span></span>

### <span data-ttu-id="594c4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="594c4-146">System.String</span></span>

### <span data-ttu-id="594c4-147">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="594c4-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="594c4-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="594c4-148">OUTPUTS</span></span>

### <span data-ttu-id="594c4-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="594c4-149">System.Boolean</span></span>

## <span data-ttu-id="594c4-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="594c4-150">NOTES</span></span>

## <span data-ttu-id="594c4-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="594c4-151">RELATED LINKS</span></span>
