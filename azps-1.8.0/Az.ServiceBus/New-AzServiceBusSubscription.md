---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 41231af48ceec0d1e5fba1735eda4d62c9b62cd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708142"
---
# <span data-ttu-id="bd0cd-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bd0cd-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="bd0cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0cd-103">Tworzy subskrypcję określonego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="bd0cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd0cd-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd0cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd0cd-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0cd-106">Polecenie cmdlet **New-AzServiceBusSubscription** tworzy nową subskrypcję określonego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="bd0cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd0cd-107">EXAMPLES</span></span>

### <span data-ttu-id="bd0cd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd0cd-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="bd0cd-109">Tworzy abonament `SB-TopicSubscription-Example1` dla określonego tematu magistrali usług `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="bd0cd-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="bd0cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd0cd-110">PARAMETERS</span></span>

### <span data-ttu-id="bd0cd-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="bd0cd-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="bd0cd-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego abonament jest automatycznie usuwany.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="bd0cd-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="bd0cd-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="bd0cd-115">Wartość wskazująca, czy w ramach subskrypcji jest obsługiwana obsługa listowa z wyjątkami oceny filtru.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="bd0cd-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="bd0cd-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="bd0cd-117">Wiadomości utracone po wygaśnięciu wiadomości</span><span class="sxs-lookup"><span data-stu-id="bd0cd-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="bd0cd-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="bd0cd-119">Wartość TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-119">Timespan to live value.</span></span>
<span data-ttu-id="bd0cd-120">Jest to czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="bd0cd-121">Jest to wartość domyślna używana, gdy TimeToLive nie jest ustawiony w wiadomości.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="bd0cd-122">Dla standardu = TimeSpan. Max i Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="bd0cd-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0cd-123">-DefaultProfile</span></span>
<span data-ttu-id="bd0cd-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0cd-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="bd0cd-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="bd0cd-126">Włączanie operacji wsadowych — wartość wskazująca, czy są włączone operacje wsadowe po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="bd0cd-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="bd0cd-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="bd0cd-128">Nazwa kolejki/tematu przesyłającej wiadomość utraconą</span><span class="sxs-lookup"><span data-stu-id="bd0cd-128">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="bd0cd-129">-ForwardTo</span></span>
<span data-ttu-id="bd0cd-130">Nazwa kolejki/tematu w celu przesłania dalej wiadomości</span><span class="sxs-lookup"><span data-stu-id="bd0cd-130">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="bd0cd-131">-LockDuration</span></span>
<span data-ttu-id="bd0cd-132">Czas trwania blokady</span><span class="sxs-lookup"><span data-stu-id="bd0cd-132">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="bd0cd-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="bd0cd-134">MaxDeliveryCount — Maksymalna liczba dostaw.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="bd0cd-135">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-135">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd0cd-136">-Name</span></span>
<span data-ttu-id="bd0cd-137">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bd0cd-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd0cd-138">-Namespace</span></span>
<span data-ttu-id="bd0cd-139">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="bd0cd-139">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="bd0cd-140">-RequiresSession</span></span>
<span data-ttu-id="bd0cd-141">RequiresSession — wartość wskazująca, czy ta Kolejka wymaga wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0cd-142">-ResourceGroupName</span></span>
<span data-ttu-id="bd0cd-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bd0cd-143">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-144">— Temat</span><span class="sxs-lookup"><span data-stu-id="bd0cd-144">-Topic</span></span>
<span data-ttu-id="bd0cd-145">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="bd0cd-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0cd-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd0cd-146">-Confirm</span></span>
<span data-ttu-id="bd0cd-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd0cd-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd0cd-148">-WhatIf</span></span>
<span data-ttu-id="bd0cd-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd0cd-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd0cd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0cd-151">CommonParameters</span></span>
<span data-ttu-id="bd0cd-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0cd-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd0cd-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0cd-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd0cd-154">INPUTS</span></span>

### <span data-ttu-id="bd0cd-155">System. String</span><span class="sxs-lookup"><span data-stu-id="bd0cd-155">System.String</span></span>

### <span data-ttu-id="bd0cd-156">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd0cd-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bd0cd-157">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd0cd-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bd0cd-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd0cd-158">OUTPUTS</span></span>

### <span data-ttu-id="bd0cd-159">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bd0cd-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bd0cd-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd0cd-160">NOTES</span></span>

## <span data-ttu-id="bd0cd-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd0cd-161">RELATED LINKS</span></span>
