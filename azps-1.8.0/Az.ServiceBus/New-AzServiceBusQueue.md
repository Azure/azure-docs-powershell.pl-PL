---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: b9ad7c729395115845349c1e39f8d90666a4fcb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708148"
---
# <span data-ttu-id="8b0df-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="8b0df-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="8b0df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b0df-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0df-103">Tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="8b0df-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8b0df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b0df-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b0df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b0df-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0df-106">Polecenie cmdlet **New-AzServiceBusQueue** tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="8b0df-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8b0df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b0df-107">EXAMPLES</span></span>

### <span data-ttu-id="8b0df-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b0df-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="8b0df-109">Tworzy nową kolejkę usługi Service Bus `SB-Queue_example1` w określonym obszarze nazw usługi Service Bus `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="8b0df-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="8b0df-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b0df-110">PARAMETERS</span></span>

### <span data-ttu-id="8b0df-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="8b0df-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="8b0df-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego kolejka jest automatycznie usuwana.</span><span class="sxs-lookup"><span data-stu-id="8b0df-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="8b0df-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="8b0df-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="8b0df-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="8b0df-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="8b0df-115">Wiadomości utracone po wygaśnięciu wiadomości</span><span class="sxs-lookup"><span data-stu-id="8b0df-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="8b0df-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="8b0df-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="8b0df-117">Wartość TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="8b0df-117">Timespan to live value.</span></span>
<span data-ttu-id="8b0df-118">Jest to czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="8b0df-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="8b0df-119">Jest to wartość domyślna używana, gdy TimeToLive nie jest ustawiony w wiadomości.</span><span class="sxs-lookup"><span data-stu-id="8b0df-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="8b0df-120">Dla standardu = TimeSpan. Max i Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="8b0df-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="8b0df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0df-121">-DefaultProfile</span></span>
<span data-ttu-id="8b0df-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b0df-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="8b0df-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="8b0df-124">Określa okno czasu historii wykrywania duplikatów, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) określa czas trwania historii wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="8b0df-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="8b0df-125">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="8b0df-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="8b0df-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="8b0df-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="8b0df-127">Włączanie operacji wsadowych — wartość wskazująca, czy są włączone operacje wsadowe po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="8b0df-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="8b0df-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="8b0df-128">-EnableExpress</span></span>
<span data-ttu-id="8b0df-129">EnableExpress-wartość wskazująca, czy jednostki ekspresowe są włączone.</span><span class="sxs-lookup"><span data-stu-id="8b0df-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="8b0df-130">Kolejka ekspresowa przechowuje wiadomość w pamięci, zanim zapisze ją do magazynu trwałego.</span><span class="sxs-lookup"><span data-stu-id="8b0df-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="8b0df-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="8b0df-131">-EnablePartitioning</span></span>
<span data-ttu-id="8b0df-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="8b0df-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="8b0df-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="8b0df-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="8b0df-134">Nazwa kolejki/tematu przesyłającej wiadomość utraconą</span><span class="sxs-lookup"><span data-stu-id="8b0df-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="8b0df-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="8b0df-135">-ForwardTo</span></span>
<span data-ttu-id="8b0df-136">Nazwa kolejki/tematu w celu przesłania dalej wiadomości</span><span class="sxs-lookup"><span data-stu-id="8b0df-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="8b0df-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="8b0df-137">-LockDuration</span></span>
<span data-ttu-id="8b0df-138">Czas trwania blokady</span><span class="sxs-lookup"><span data-stu-id="8b0df-138">Lock Duration</span></span>

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

### <span data-ttu-id="8b0df-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="8b0df-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="8b0df-140">MaxDeliveryCount — Maksymalna liczba dostaw.</span><span class="sxs-lookup"><span data-stu-id="8b0df-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="8b0df-141">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="8b0df-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="8b0df-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="8b0df-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="8b0df-143">MaxSizeInMegabytes — maksymalny rozmiar kolejki w megabajtach, czyli rozmiar pamięci przydzielonej dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="8b0df-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0df-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="8b0df-144">-MessageCount</span></span>
<span data-ttu-id="8b0df-145">MessageCount — liczba wiadomości w kolejce</span><span class="sxs-lookup"><span data-stu-id="8b0df-145">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0df-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b0df-146">-Name</span></span>
<span data-ttu-id="8b0df-147">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="8b0df-147">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0df-148">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8b0df-148">-Namespace</span></span>
<span data-ttu-id="8b0df-149">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="8b0df-149">Namespace Name</span></span>

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

### <span data-ttu-id="8b0df-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="8b0df-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="8b0df-151">RequiresDuplicateDetection-wartość wskazująca, czy kolejka obsługuje koncepcję sesji</span><span class="sxs-lookup"><span data-stu-id="8b0df-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="8b0df-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="8b0df-152">-RequiresSession</span></span>
<span data-ttu-id="8b0df-153">RequiresSession — wartość wskazująca, czy ta Kolejka wymaga wykrywania duplikatów</span><span class="sxs-lookup"><span data-stu-id="8b0df-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="8b0df-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0df-154">-ResourceGroupName</span></span>
<span data-ttu-id="8b0df-155">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8b0df-155">The name of the resource group</span></span>

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

### <span data-ttu-id="8b0df-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="8b0df-156">-SizeInBytes</span></span>
<span data-ttu-id="8b0df-157">SizeInBytes — rozmiar kolejki w bajtach</span><span class="sxs-lookup"><span data-stu-id="8b0df-157">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0df-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b0df-158">-Confirm</span></span>
<span data-ttu-id="8b0df-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b0df-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0df-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0df-160">-WhatIf</span></span>
<span data-ttu-id="8b0df-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b0df-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0df-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b0df-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0df-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0df-163">CommonParameters</span></span>
<span data-ttu-id="8b0df-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0df-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0df-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0df-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0df-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b0df-166">INPUTS</span></span>

### <span data-ttu-id="8b0df-167">System. String</span><span class="sxs-lookup"><span data-stu-id="8b0df-167">System.String</span></span>

### <span data-ttu-id="8b0df-168">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b0df-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b0df-169">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b0df-169">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b0df-170">System. Nullable ' 1 [[System. Int64; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b0df-170">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8b0df-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b0df-171">OUTPUTS</span></span>

### <span data-ttu-id="8b0df-172">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="8b0df-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="8b0df-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b0df-173">NOTES</span></span>

## <span data-ttu-id="8b0df-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b0df-174">RELATED LINKS</span></span>
