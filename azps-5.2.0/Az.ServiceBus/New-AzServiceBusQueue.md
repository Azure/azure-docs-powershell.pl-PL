---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368025"
---
# <span data-ttu-id="84fff-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="84fff-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="84fff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84fff-102">SYNOPSIS</span></span>
<span data-ttu-id="84fff-103">Tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="84fff-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84fff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84fff-104">SYNTAX</span></span>

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

## <span data-ttu-id="84fff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84fff-105">DESCRIPTION</span></span>
<span data-ttu-id="84fff-106">Polecenie cmdlet **New-AzServiceBusQueue** tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="84fff-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84fff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84fff-107">EXAMPLES</span></span>

### <span data-ttu-id="84fff-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84fff-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="84fff-109">Tworzy nową kolejkę usługi Service Bus `SB-Queue_example1` w określonym obszarze nazw usługi Service Bus `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="84fff-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="84fff-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="84fff-110">Example 2</span></span>

<span data-ttu-id="84fff-111">Tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="84fff-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="84fff-112">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="84fff-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="84fff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84fff-113">PARAMETERS</span></span>

### <span data-ttu-id="84fff-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="84fff-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="84fff-115">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego kolejka jest automatycznie usuwana.</span><span class="sxs-lookup"><span data-stu-id="84fff-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="84fff-116">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="84fff-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="84fff-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="84fff-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="84fff-118">Wiadomości utracone po wygaśnięciu wiadomości</span><span class="sxs-lookup"><span data-stu-id="84fff-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="84fff-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="84fff-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="84fff-120">Wartość TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="84fff-120">Timespan to live value.</span></span>
<span data-ttu-id="84fff-121">Jest to czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="84fff-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="84fff-122">Jest to wartość domyślna używana, gdy TimeToLive nie jest ustawiony w wiadomości.</span><span class="sxs-lookup"><span data-stu-id="84fff-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="84fff-123">Standardowy = TimeSpan. Max i Basic = 14 dni</span><span class="sxs-lookup"><span data-stu-id="84fff-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="84fff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84fff-124">-DefaultProfile</span></span>
<span data-ttu-id="84fff-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84fff-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84fff-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="84fff-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="84fff-127">Określa okno czasu historii wykrywania duplikatów — wartość [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) określająca czas trwania historii wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="84fff-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="84fff-128">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="84fff-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="84fff-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="84fff-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="84fff-130">Włączanie operacji wsadowych — wartość wskazująca, czy są włączone operacje wsadowe po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="84fff-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="84fff-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="84fff-131">-EnableExpress</span></span>
<span data-ttu-id="84fff-132">EnableExpress-wartość wskazująca, czy jednostki ekspresowe są włączone.</span><span class="sxs-lookup"><span data-stu-id="84fff-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="84fff-133">Kolejka ekspresowa przechowuje wiadomość w pamięci, zanim zapisze ją do magazynu trwałego.</span><span class="sxs-lookup"><span data-stu-id="84fff-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="84fff-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="84fff-134">-EnablePartitioning</span></span>
<span data-ttu-id="84fff-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="84fff-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="84fff-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="84fff-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="84fff-137">Nazwa kolejki/tematu przesyłającej wiadomość utraconą</span><span class="sxs-lookup"><span data-stu-id="84fff-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="84fff-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="84fff-138">-ForwardTo</span></span>
<span data-ttu-id="84fff-139">Nazwa kolejki/tematu w celu przesłania dalej wiadomości</span><span class="sxs-lookup"><span data-stu-id="84fff-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="84fff-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="84fff-140">-LockDuration</span></span>
<span data-ttu-id="84fff-141">Czas trwania blokady</span><span class="sxs-lookup"><span data-stu-id="84fff-141">Lock Duration</span></span>

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

### <span data-ttu-id="84fff-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="84fff-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="84fff-143">MaxDeliveryCount — Maksymalna liczba dostaw.</span><span class="sxs-lookup"><span data-stu-id="84fff-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="84fff-144">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="84fff-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="84fff-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="84fff-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="84fff-146">MaxSizeInMegabytes — maksymalny rozmiar kolejki w megabajtach, czyli rozmiar pamięci przydzielonej dla kolejki. Wartość domyślna to 1024.</span><span class="sxs-lookup"><span data-stu-id="84fff-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="84fff-147">Max dla standardowej wersji SKU to 5120, a dla SKU Premium jest 81920, dozwolone wartości: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="84fff-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="84fff-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="84fff-148">-MessageCount</span></span>
<span data-ttu-id="84fff-149">MessageCount — liczba wiadomości w kolejce</span><span class="sxs-lookup"><span data-stu-id="84fff-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="84fff-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84fff-150">-Name</span></span>
<span data-ttu-id="84fff-151">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="84fff-151">Queue Name</span></span>

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

### <span data-ttu-id="84fff-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84fff-152">-Namespace</span></span>
<span data-ttu-id="84fff-153">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="84fff-153">Namespace Name</span></span>

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

### <span data-ttu-id="84fff-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="84fff-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="84fff-155">RequiresDuplicateDetection-wartość wskazująca, czy kolejka obsługuje koncepcję sesji</span><span class="sxs-lookup"><span data-stu-id="84fff-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="84fff-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="84fff-156">-RequiresSession</span></span>
<span data-ttu-id="84fff-157">RequiresSession — wartość wskazująca, czy ta Kolejka używa sesji</span><span class="sxs-lookup"><span data-stu-id="84fff-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="84fff-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84fff-158">-ResourceGroupName</span></span>
<span data-ttu-id="84fff-159">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="84fff-159">The name of the resource group</span></span>

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

### <span data-ttu-id="84fff-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="84fff-160">-SizeInBytes</span></span>
<span data-ttu-id="84fff-161">SizeInBytes — rozmiar kolejki w bajtach</span><span class="sxs-lookup"><span data-stu-id="84fff-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="84fff-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84fff-162">-Confirm</span></span>
<span data-ttu-id="84fff-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84fff-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84fff-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84fff-164">-WhatIf</span></span>
<span data-ttu-id="84fff-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84fff-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84fff-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84fff-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84fff-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fff-167">CommonParameters</span></span>
<span data-ttu-id="84fff-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84fff-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84fff-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84fff-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fff-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84fff-170">INPUTS</span></span>

### <span data-ttu-id="84fff-171">System. String</span><span class="sxs-lookup"><span data-stu-id="84fff-171">System.String</span></span>

### <span data-ttu-id="84fff-172">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84fff-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84fff-173">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84fff-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84fff-174">System. Nullable ' 1 [[System. Int64; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84fff-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="84fff-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84fff-175">OUTPUTS</span></span>

### <span data-ttu-id="84fff-176">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="84fff-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="84fff-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84fff-177">NOTES</span></span>

## <span data-ttu-id="84fff-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84fff-178">RELATED LINKS</span></span>
