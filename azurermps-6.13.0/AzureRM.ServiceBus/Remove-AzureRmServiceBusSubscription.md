---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: b8b2b9f6bb8a082647a14285a907465e8e12348f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546480"
---
# <span data-ttu-id="c14df-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="c14df-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="c14df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c14df-102">SYNOPSIS</span></span>
<span data-ttu-id="c14df-103">Usuwa subskrypcję tematu z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c14df-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c14df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c14df-104">SYNTAX</span></span>

### <span data-ttu-id="c14df-105">SubscriptionPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c14df-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c14df-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c14df-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14df-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c14df-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c14df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c14df-108">DESCRIPTION</span></span>
<span data-ttu-id="c14df-109">Polecenie cmdlet **Remove-AzureRmServiceBusSubscription** usuwa abonament do tematu z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="c14df-109">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c14df-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c14df-110">EXAMPLES</span></span>

### <span data-ttu-id="c14df-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c14df-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="c14df-112">Usuwa subskrypcję `SB-TopicSubscription-Example1` tematu `SB-Topic_exampl1` w określonym obszarze nazw magistrali usług `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c14df-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c14df-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="c14df-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="c14df-114">Przykład 2,2-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="c14df-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzureRmServiceBusSubscription <params> |Remove-AzureRmServiceBusSubscription
```

### <span data-ttu-id="c14df-115">Przykład 3,1-ResourceId-używa zmiennej:</span><span class="sxs-lookup"><span data-stu-id="c14df-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="c14df-116">Przykład 3,2-ResourceId-używa wartości ciągu:</span><span class="sxs-lookup"><span data-stu-id="c14df-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="c14df-117">Usuwa abonament podany za pośrednictwem identyfikatora ARM w $resourceid parametru/String dla-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c14df-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="c14df-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c14df-118">PARAMETERS</span></span>

### <span data-ttu-id="c14df-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c14df-119">-AsJob</span></span>
<span data-ttu-id="c14df-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c14df-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c14df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14df-121">-DefaultProfile</span></span>
<span data-ttu-id="c14df-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c14df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14df-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c14df-123">-InputObject</span></span>
<span data-ttu-id="c14df-124">Obiekt subskrypcji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="c14df-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="c14df-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c14df-125">-Name</span></span>
<span data-ttu-id="c14df-126">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c14df-126">Subscription Name</span></span>

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

### <span data-ttu-id="c14df-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c14df-127">-Namespace</span></span>
<span data-ttu-id="c14df-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c14df-128">Namespace Name</span></span>

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

### <span data-ttu-id="c14df-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c14df-129">-PassThru</span></span>
<span data-ttu-id="c14df-130">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="c14df-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c14df-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14df-131">-ResourceGroupName</span></span>
<span data-ttu-id="c14df-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c14df-132">The name of the resource group</span></span>

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

### <span data-ttu-id="c14df-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c14df-133">-ResourceId</span></span>
<span data-ttu-id="c14df-134">Identyfikator zasobu subskrypcji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="c14df-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="c14df-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="c14df-135">-Topic</span></span>
<span data-ttu-id="c14df-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="c14df-136">Topic Name</span></span>

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

### <span data-ttu-id="c14df-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c14df-137">-Confirm</span></span>
<span data-ttu-id="c14df-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14df-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14df-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14df-139">-WhatIf</span></span>
<span data-ttu-id="c14df-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14df-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14df-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c14df-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14df-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14df-142">CommonParameters</span></span>
<span data-ttu-id="c14df-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14df-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14df-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14df-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14df-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c14df-145">INPUTS</span></span>

### <span data-ttu-id="c14df-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c14df-146">System.String</span></span>

### <span data-ttu-id="c14df-147">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="c14df-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="c14df-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c14df-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c14df-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c14df-149">OUTPUTS</span></span>

### <span data-ttu-id="c14df-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c14df-150">System.Boolean</span></span>

## <span data-ttu-id="c14df-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c14df-151">NOTES</span></span>

## <span data-ttu-id="c14df-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c14df-152">RELATED LINKS</span></span>
