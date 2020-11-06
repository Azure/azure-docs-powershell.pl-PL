---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546008"
---
# <span data-ttu-id="98461-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="98461-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="98461-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98461-102">SYNOPSIS</span></span>
<span data-ttu-id="98461-103">Tworzy subskrypcję określonego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="98461-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98461-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98461-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98461-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98461-105">DESCRIPTION</span></span>
<span data-ttu-id="98461-106">Polecenie cmdlet **New-AzureRmServiceBusSubscription** tworzy nową subskrypcję określonego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="98461-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="98461-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98461-107">EXAMPLES</span></span>

### <span data-ttu-id="98461-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98461-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="98461-109">Tworzy abonament `SB-TopicSubscription-Example1` dla określonego tematu magistrali usług `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="98461-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="98461-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98461-110">PARAMETERS</span></span>

### <span data-ttu-id="98461-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="98461-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="98461-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego abonament jest automatycznie usuwany.</span><span class="sxs-lookup"><span data-stu-id="98461-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="98461-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="98461-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="98461-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="98461-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="98461-115">Wskazuje, czy w ramach subskrypcji jest obsługiwana obsługa listowa z wyjątkami oceny filtru.</span><span class="sxs-lookup"><span data-stu-id="98461-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="98461-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="98461-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="98461-117">Wskazuje, czy subskrypcja ma obsługiwać wiadomości utraconych wiadomości, gdy wiadomość traci ważność.</span><span class="sxs-lookup"><span data-stu-id="98461-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="98461-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="98461-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="98461-119">Wskazuje, czy są włączone operacje wsadowe po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="98461-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="98461-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="98461-120">-IsReadOnly</span></span>
<span data-ttu-id="98461-121">Wskazuje, czy opis encji jest tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="98461-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="98461-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="98461-122">-LockDuration</span></span>
<span data-ttu-id="98461-123">Określa przedział czasu blokowania dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="98461-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="98461-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="98461-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="98461-125">Określa liczbę maksymalnych dostaw.</span><span class="sxs-lookup"><span data-stu-id="98461-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="98461-126">Po tej liczbie dostaw automatycznie deadlettered wiadomość.</span><span class="sxs-lookup"><span data-stu-id="98461-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="98461-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="98461-127">-RequiresSession</span></span>
<span data-ttu-id="98461-128">Określa, czy subskrypcja obsługuje koncepcję sesji.</span><span class="sxs-lookup"><span data-stu-id="98461-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="98461-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98461-129">-Confirm</span></span>
<span data-ttu-id="98461-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98461-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98461-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98461-131">-WhatIf</span></span>
<span data-ttu-id="98461-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98461-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98461-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98461-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98461-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="98461-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="98461-135">Wartość TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="98461-135">Timespan to live value.</span></span> <span data-ttu-id="98461-136">Jest to czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="98461-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="98461-137">Jest to wartość domyślna używana, gdy TimeToLive nie jest ustawiony w wiadomości.</span><span class="sxs-lookup"><span data-stu-id="98461-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="98461-138">Dla standardu = TimeSpan. Max i Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="98461-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="98461-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98461-139">-DefaultProfile</span></span>
<span data-ttu-id="98461-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98461-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98461-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98461-141">-Name</span></span>
<span data-ttu-id="98461-142">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="98461-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98461-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98461-143">-Namespace</span></span>
<span data-ttu-id="98461-144">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="98461-144">Namespace Name.</span></span>

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

### <span data-ttu-id="98461-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98461-145">-ResourceGroupName</span></span>
<span data-ttu-id="98461-146">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="98461-146">The name of the resource group</span></span>

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

### <span data-ttu-id="98461-147">— Temat</span><span class="sxs-lookup"><span data-stu-id="98461-147">-Topic</span></span>
<span data-ttu-id="98461-148">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="98461-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98461-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98461-149">CommonParameters</span></span>
<span data-ttu-id="98461-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98461-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98461-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98461-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98461-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98461-152">INPUTS</span></span>

### <span data-ttu-id="98461-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="98461-153">-ResourceGroup</span></span>
 <span data-ttu-id="98461-154">System. String</span><span class="sxs-lookup"><span data-stu-id="98461-154">System.String</span></span>
 

### <span data-ttu-id="98461-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="98461-155">-NamespaceName</span></span>
 <span data-ttu-id="98461-156">System. String</span><span class="sxs-lookup"><span data-stu-id="98461-156">System.String</span></span>
 

### <span data-ttu-id="98461-157">-Tematname</span><span class="sxs-lookup"><span data-stu-id="98461-157">-TopicName</span></span>
 <span data-ttu-id="98461-158">System. String</span><span class="sxs-lookup"><span data-stu-id="98461-158">System.String</span></span>
 

### <span data-ttu-id="98461-159">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="98461-159">-SubscriptionName</span></span>
 <span data-ttu-id="98461-160">System. String</span><span class="sxs-lookup"><span data-stu-id="98461-160">System.String</span></span>

## <span data-ttu-id="98461-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98461-161">OUTPUTS</span></span>

### <span data-ttu-id="98461-162">Microsoft. Azure. Commands. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="98461-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="98461-163">Nazwa: SB-TopicSubscription — lokalizacja example1: zachodni stan AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. MODELES. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: DeadLetteringOnMessageExpiration: EnableBatchedOperations: 00:01:00 EntityAvailabilityStatus: true IsReadOnly: Microsoft LockDuration: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="98461-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="98461-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98461-164">NOTES</span></span>

## <span data-ttu-id="98461-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98461-165">RELATED LINKS</span></span>

