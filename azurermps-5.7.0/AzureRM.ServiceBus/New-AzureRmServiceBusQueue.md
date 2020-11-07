---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717688"
---
# <span data-ttu-id="9cc53-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="9cc53-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="9cc53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cc53-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc53-103">Tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9cc53-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cc53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cc53-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cc53-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc53-106">Polecenie cmdlet **New-AzureRmServiceBusQueue** tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9cc53-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9cc53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cc53-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc53-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cc53-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="9cc53-109">Tworzy nową kolejkę usługi Service Bus `SB-Queue_exampl1` w określonym obszarze nazw usługi Service Bus `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="9cc53-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="9cc53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cc53-110">PARAMETERS</span></span>

### <span data-ttu-id="9cc53-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="9cc53-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="9cc53-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego kolejka jest automatycznie usuwana.</span><span class="sxs-lookup"><span data-stu-id="9cc53-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="9cc53-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="9cc53-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cc53-114">-Confirm</span></span>
<span data-ttu-id="9cc53-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cc53-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="9cc53-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="9cc53-117">Wiadomości utracone po wygaśnięciu wiadomości</span><span class="sxs-lookup"><span data-stu-id="9cc53-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="9cc53-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="9cc53-119">Wartość TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="9cc53-119">Timespan to live value.</span></span>
<span data-ttu-id="9cc53-120">Jest to czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9cc53-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="9cc53-121">Jest to wartość domyślna używana, gdy TimeToLive nie jest ustawiony w wiadomości.</span><span class="sxs-lookup"><span data-stu-id="9cc53-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="9cc53-122">Dla standardu = TimeSpan. Max i Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="9cc53-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc53-123">-DefaultProfile</span></span>
<span data-ttu-id="9cc53-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc53-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="9cc53-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="9cc53-126">Określa okno czasu historii wykrywania duplikatów, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) określa czas trwania historii wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="9cc53-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="9cc53-127">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="9cc53-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="9cc53-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="9cc53-129">Włączanie operacji wsadowych — wartość wskazująca, czy są włączone operacje wsadowe po stronie serwera</span><span class="sxs-lookup"><span data-stu-id="9cc53-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="9cc53-130">-EnableExpress</span></span>
<span data-ttu-id="9cc53-131">EnableExpress-wartość wskazująca, czy jednostki ekspresowe są włączone.</span><span class="sxs-lookup"><span data-stu-id="9cc53-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="9cc53-132">Kolejka ekspresowa przechowuje wiadomość w pamięci, zanim zapisze ją do magazynu trwałego.</span><span class="sxs-lookup"><span data-stu-id="9cc53-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="9cc53-133">-EnablePartitioning</span></span>
<span data-ttu-id="9cc53-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="9cc53-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="9cc53-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="9cc53-136">Nazwa kolejki/tematu przesyłającej wiadomość utraconą</span><span class="sxs-lookup"><span data-stu-id="9cc53-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="9cc53-137">-ForwardTo</span></span>
<span data-ttu-id="9cc53-138">Nazwa kolejki/tematu w celu przesłania dalej wiadomości</span><span class="sxs-lookup"><span data-stu-id="9cc53-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="9cc53-139">-LockDuration</span></span>
<span data-ttu-id="9cc53-140">Czas trwania blokady</span><span class="sxs-lookup"><span data-stu-id="9cc53-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="9cc53-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="9cc53-142">MaxDeliveryCount — Maksymalna liczba dostaw.</span><span class="sxs-lookup"><span data-stu-id="9cc53-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="9cc53-143">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="9cc53-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="9cc53-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="9cc53-145">MaxSizeInMegabytes — maksymalny rozmiar kolejki w megabajtach, czyli rozmiar pamięci przydzielonej dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="9cc53-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="9cc53-146">-MessageCount</span></span>
<span data-ttu-id="9cc53-147">MessageCount — liczba wiadomości w kolejce</span><span class="sxs-lookup"><span data-stu-id="9cc53-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9cc53-148">-Name</span></span>
<span data-ttu-id="9cc53-149">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="9cc53-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9cc53-150">-Namespace</span></span>
<span data-ttu-id="9cc53-151">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="9cc53-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="9cc53-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="9cc53-153">RequiresDuplicateDetection-wartość wskazująca, czy kolejka obsługuje koncepcję sesji</span><span class="sxs-lookup"><span data-stu-id="9cc53-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="9cc53-154">-RequiresSession</span></span>
<span data-ttu-id="9cc53-155">RequiresSession — wartość wskazująca, czy ta Kolejka wymaga wykrywania duplikatów</span><span class="sxs-lookup"><span data-stu-id="9cc53-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc53-156">-ResourceGroupName</span></span>
<span data-ttu-id="9cc53-157">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9cc53-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="9cc53-158">-SizeInBytes</span></span>
<span data-ttu-id="9cc53-159">SizeInBytes — rozmiar kolejki w bajtach</span><span class="sxs-lookup"><span data-stu-id="9cc53-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc53-160">-WhatIf</span></span>
<span data-ttu-id="9cc53-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cc53-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc53-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9cc53-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc53-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc53-163">CommonParameters</span></span>
<span data-ttu-id="9cc53-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc53-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9cc53-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc53-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc53-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cc53-166">INPUTS</span></span>

### <span data-ttu-id="9cc53-167">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9cc53-167">-ResourceGroup</span></span>
 <span data-ttu-id="9cc53-168">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc53-168">System.String</span></span>

### <span data-ttu-id="9cc53-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9cc53-169">-NamespaceName</span></span>
 <span data-ttu-id="9cc53-170">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc53-170">System.String</span></span>

### <span data-ttu-id="9cc53-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="9cc53-171">-QueueName</span></span>
 <span data-ttu-id="9cc53-172">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc53-172">System.String</span></span>

### <span data-ttu-id="9cc53-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="9cc53-173">-EnablePartitioning</span></span>
 <span data-ttu-id="9cc53-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="9cc53-174">System.Boolean?</span></span>


## <span data-ttu-id="9cc53-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cc53-175">OUTPUTS</span></span>

### <span data-ttu-id="9cc53-176">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="9cc53-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="9cc53-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cc53-177">NOTES</span></span>

## <span data-ttu-id="9cc53-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cc53-178">RELATED LINKS</span></span>
