---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502897"
---
# <span data-ttu-id="12d3f-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="12d3f-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="12d3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="12d3f-103">Tworzy subskrypcję określonego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="12d3f-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="12d3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12d3f-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="12d3f-106">Polecenie cmdlet **New-AzServiceBusSubscription** tworzy nową subskrypcję określonego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="12d3f-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="12d3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="12d3f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12d3f-108">Example 1</span></span>
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

<span data-ttu-id="12d3f-109">Tworzy abonament `SB-TopicSubscription-Example1` dla określonego tematu magistrali usług `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="12d3f-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="12d3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="12d3f-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="12d3f-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="12d3f-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego abonament jest automatycznie usuwany.</span><span class="sxs-lookup"><span data-stu-id="12d3f-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="12d3f-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="12d3f-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="12d3f-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="12d3f-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="12d3f-115">Wartość wskazująca, czy w ramach subskrypcji jest obsługiwana obsługa listowa z wyjątkami oceny filtru.</span><span class="sxs-lookup"><span data-stu-id="12d3f-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="12d3f-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="12d3f-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="12d3f-117">Wiadomości utracone po wygaśnięciu wiadomości</span><span class="sxs-lookup"><span data-stu-id="12d3f-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="12d3f-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="12d3f-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="12d3f-119">Wartość TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="12d3f-119">Timespan to live value.</span></span>
<span data-ttu-id="12d3f-120">Jest to czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="12d3f-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="12d3f-121">Jest to wartość domyślna używana, gdy TimeToLive nie jest ustawiony w wiadomości.</span><span class="sxs-lookup"><span data-stu-id="12d3f-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="12d3f-122">Standardowy = TimeSpan. Max i Basic = 14 dni</span><span class="sxs-lookup"><span data-stu-id="12d3f-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="12d3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d3f-123">-DefaultProfile</span></span>
<span data-ttu-id="12d3f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12d3f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d3f-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="12d3f-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="12d3f-126">Włączanie operacji wsadowych — wartość wskazująca, czy są włączone operacje wsadowe po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="12d3f-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="12d3f-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="12d3f-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="12d3f-128">Nazwa kolejki/tematu przesyłającej wiadomość utraconą</span><span class="sxs-lookup"><span data-stu-id="12d3f-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="12d3f-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="12d3f-129">-ForwardTo</span></span>
<span data-ttu-id="12d3f-130">Nazwa kolejki/tematu w celu przesłania dalej wiadomości</span><span class="sxs-lookup"><span data-stu-id="12d3f-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="12d3f-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="12d3f-131">-LockDuration</span></span>
<span data-ttu-id="12d3f-132">Czas trwania blokady</span><span class="sxs-lookup"><span data-stu-id="12d3f-132">Lock Duration</span></span>

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

### <span data-ttu-id="12d3f-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="12d3f-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="12d3f-134">MaxDeliveryCount — Maksymalna liczba dostaw.</span><span class="sxs-lookup"><span data-stu-id="12d3f-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="12d3f-135">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="12d3f-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="12d3f-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12d3f-136">-Name</span></span>
<span data-ttu-id="12d3f-137">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d3f-137">Subscription Name</span></span>

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

### <span data-ttu-id="12d3f-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12d3f-138">-Namespace</span></span>
<span data-ttu-id="12d3f-139">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="12d3f-139">Namespace Name</span></span>

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

### <span data-ttu-id="12d3f-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="12d3f-140">-RequiresSession</span></span>
<span data-ttu-id="12d3f-141">RequiresSession — wartość wskazująca, czy ta Kolejka wymaga wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="12d3f-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="12d3f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d3f-142">-ResourceGroupName</span></span>
<span data-ttu-id="12d3f-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="12d3f-143">The name of the resource group</span></span>

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

### <span data-ttu-id="12d3f-144">— Temat</span><span class="sxs-lookup"><span data-stu-id="12d3f-144">-Topic</span></span>
<span data-ttu-id="12d3f-145">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="12d3f-145">Topic Name</span></span>

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

### <span data-ttu-id="12d3f-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12d3f-146">-Confirm</span></span>
<span data-ttu-id="12d3f-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d3f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d3f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d3f-148">-WhatIf</span></span>
<span data-ttu-id="12d3f-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d3f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d3f-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12d3f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d3f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d3f-151">CommonParameters</span></span>
<span data-ttu-id="12d3f-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d3f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d3f-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d3f-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d3f-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12d3f-154">INPUTS</span></span>

### <span data-ttu-id="12d3f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="12d3f-155">System.String</span></span>

### <span data-ttu-id="12d3f-156">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12d3f-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="12d3f-157">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12d3f-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="12d3f-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12d3f-158">OUTPUTS</span></span>

### <span data-ttu-id="12d3f-159">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="12d3f-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="12d3f-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12d3f-160">NOTES</span></span>

## <span data-ttu-id="12d3f-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12d3f-161">RELATED LINKS</span></span>
