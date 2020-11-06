---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527285"
---
# <span data-ttu-id="dbbbd-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="dbbbd-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="dbbbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbbd-103">Tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbbbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbbbd-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbbbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dbbbd-105">DESCRIPTION</span></span>
<span data-ttu-id="dbbbd-106">Polecenie cmdlet **New-AzureRmServiceBusQueue** tworzy kolejkę usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dbbbd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbbbd-107">EXAMPLES</span></span>

### <span data-ttu-id="dbbbd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dbbbd-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="dbbbd-109">Tworzy nową kolejkę usługi Service Bus `SB-Queue_exampl1` w określonym obszarze nazw usługi Service Bus `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="dbbbd-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="dbbbd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbbbd-110">PARAMETERS</span></span>

### <span data-ttu-id="dbbbd-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="dbbbd-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="dbbbd-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego kolejka jest automatycznie usuwana.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="dbbbd-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="dbbbd-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="dbbbd-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="dbbbd-115">Określa, czy wiadomości są deadletteredne po wygaśnięciu.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="dbbbd-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="dbbbd-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="dbbbd-117">Określa domyślny czas wygaśnięcia (TTL) dla wiadomości.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="dbbbd-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="dbbbd-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="dbbbd-119">Określa okno czasu historii wykrywania duplikatów, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) określa czas trwania historii wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="dbbbd-120">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="dbbbd-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="dbbbd-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="dbbbd-122">Określa, czy są włączone operacje wsadowe po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="dbbbd-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="dbbbd-123">-EnableExpress</span></span>
<span data-ttu-id="dbbbd-124">Określa, czy jednostki ekspresowe są włączone.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="dbbbd-125">Kolejka ekspresowa przechowuje wiadomość w pamięci, zanim zapisze ją do magazynu trwałego.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="dbbbd-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="dbbbd-126">-EnablePartitioning</span></span>
<span data-ttu-id="dbbbd-127">Określa, czy EnablePartitioning jest włączony.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbbd-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="dbbbd-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="dbbbd-129">Określa, czy wiadomość jest anonimowo dostępna.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="dbbbd-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="dbbbd-130">-LockDuration</span></span>
<span data-ttu-id="dbbbd-131">Określa czas blokowania.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="dbbbd-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="dbbbd-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="dbbbd-133">Określa maksymalną liczbę dostaw.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="dbbbd-134">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="dbbbd-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="dbbbd-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="dbbbd-136">Określa maksymalny rozmiar kolejki w megabajtach, czyli rozmiar pamięci przydzielonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="dbbbd-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="dbbbd-137">-MessageCount</span></span>
<span data-ttu-id="dbbbd-138">Określa liczbę wiadomości w kolejce.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="dbbbd-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="dbbbd-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="dbbbd-140">Określa, czy kolejka wymaga wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="dbbbd-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="dbbbd-141">-RequiresSession</span></span>
<span data-ttu-id="dbbbd-142">Określa, czy ta Kolejka obsługuje sesje.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="dbbbd-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="dbbbd-143">-SizeInBytes</span></span>
<span data-ttu-id="dbbbd-144">Rozmiar kolejki w bajtach.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="dbbbd-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbbbd-145">-Confirm</span></span>
<span data-ttu-id="dbbbd-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbbbd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbbbd-147">-WhatIf</span></span>
<span data-ttu-id="dbbbd-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbbbd-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbbbd-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbbd-150">-DefaultProfile</span></span>
<span data-ttu-id="dbbbd-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbbbd-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dbbbd-152">-Name</span></span>
<span data-ttu-id="dbbbd-153">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbbd-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dbbbd-154">-Namespace</span></span>
<span data-ttu-id="dbbbd-155">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbbd-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbbbd-156">-ResourceGroupName</span></span>
<span data-ttu-id="dbbbd-157">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dbbbd-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbbd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbbd-158">CommonParameters</span></span>
<span data-ttu-id="dbbbd-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbbbd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbbd-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbbbd-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbbd-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbbbd-161">INPUTS</span></span>

### <span data-ttu-id="dbbbd-162">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dbbbd-162">-ResourceGroup</span></span>
 <span data-ttu-id="dbbbd-163">System. String</span><span class="sxs-lookup"><span data-stu-id="dbbbd-163">System.String</span></span>

### <span data-ttu-id="dbbbd-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="dbbbd-164">-NamespaceName</span></span>
 <span data-ttu-id="dbbbd-165">System. String</span><span class="sxs-lookup"><span data-stu-id="dbbbd-165">System.String</span></span>

### <span data-ttu-id="dbbbd-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="dbbbd-166">-QueueName</span></span>
 <span data-ttu-id="dbbbd-167">System. String</span><span class="sxs-lookup"><span data-stu-id="dbbbd-167">System.String</span></span>

### <span data-ttu-id="dbbbd-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="dbbbd-168">-EnablePartitioning</span></span>
 <span data-ttu-id="dbbbd-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="dbbbd-169">System.Boolean?</span></span>

## <span data-ttu-id="dbbbd-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbbbd-170">OUTPUTS</span></span>

### <span data-ttu-id="dbbbd-171">Microsoft. Azure. Commands. ServiceBus. models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="dbbbd-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="dbbbd-172">Nazwa: SB-Queue_exampl1 lokalizacji: zachodni stan LockDuration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: prawda DeadLetteringOnMessageExpiration: false EnableExpress: EnablePartitioning 16384: IsAnonymousAccessible MaxDeliveryCount: MaxSizeInMegabytes: MessageCount: false CountDetails: FAŁSZ RequiresDuplicateDetection: 1/20/2017 2:51:37 AM</span><span class="sxs-lookup"><span data-stu-id="dbbbd-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="dbbbd-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbbbd-173">NOTES</span></span>

## <span data-ttu-id="dbbbd-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbbbd-174">RELATED LINKS</span></span>

