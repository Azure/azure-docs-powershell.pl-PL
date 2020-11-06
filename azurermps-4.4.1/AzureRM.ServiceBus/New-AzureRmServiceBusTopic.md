---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542988"
---
# <span data-ttu-id="afd15-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="afd15-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="afd15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afd15-102">SYNOPSIS</span></span>
<span data-ttu-id="afd15-103">Tworzy nowy temat magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="afd15-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afd15-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="afd15-105">DESCRIPTION</span></span>
<span data-ttu-id="afd15-106">Polecenie cmdlet **New-AzureRmServiceBusTopic** tworzy nowy temat magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="afd15-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="afd15-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afd15-107">EXAMPLES</span></span>

### <span data-ttu-id="afd15-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afd15-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="afd15-109">Tworzy nowy temat magistrali usług `SB-Topic_exampl1` w określonym obszarze nazw usługi Service Bus `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="afd15-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="afd15-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afd15-110">PARAMETERS</span></span>

### <span data-ttu-id="afd15-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="afd15-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="afd15-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego temat zostanie automatycznie usunięty.</span><span class="sxs-lookup"><span data-stu-id="afd15-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="afd15-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="afd15-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="afd15-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="afd15-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="afd15-115">Określa czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="afd15-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="afd15-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="afd15-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="afd15-117">Określa strukturę [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) definiującą czas trwania historii wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="afd15-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="afd15-118">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="afd15-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="afd15-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="afd15-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="afd15-120">Wskazuje, czy są włączone operacje wsadowe po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="afd15-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="afd15-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="afd15-121">-EnableExpress</span></span>
<span data-ttu-id="afd15-122">Wskazuje, czy jednostki ekspresowe są włączone.</span><span class="sxs-lookup"><span data-stu-id="afd15-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="afd15-123">Kolejka ekspresowa przechowuje wiadomość w pamięci, zanim zapisze ją do magazynu trwałego.</span><span class="sxs-lookup"><span data-stu-id="afd15-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="afd15-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="afd15-124">-EnablePartitioning</span></span>
<span data-ttu-id="afd15-125">Określa, czy chcesz, aby temat był podzielony na wiele brokerów wiadomości.</span><span class="sxs-lookup"><span data-stu-id="afd15-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="afd15-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="afd15-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="afd15-127">Określa, czy włączyć partycjonowanie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="afd15-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="afd15-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="afd15-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="afd15-129">Wskazuje, czy filtrowanie jest włączone dla wiadomości przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="afd15-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="afd15-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="afd15-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="afd15-131">Wskazuje, czy wiadomość zezwala na dostęp anonimowy.</span><span class="sxs-lookup"><span data-stu-id="afd15-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="afd15-132">-Isexpress</span><span class="sxs-lookup"><span data-stu-id="afd15-132">-IsExpress</span></span>
<span data-ttu-id="afd15-133">Wskazuje, czy temat jest dostępny w programie Express.</span><span class="sxs-lookup"><span data-stu-id="afd15-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="afd15-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="afd15-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="afd15-135">Maksymalny rozmiar tematu w megabajtach, czyli rozmiar pamięci przydzielonej dla tego tematu.</span><span class="sxs-lookup"><span data-stu-id="afd15-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="afd15-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="afd15-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="afd15-137">Wskazuje, czy temat wymaga wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="afd15-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="afd15-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="afd15-138">-SizeInBytes</span></span>
<span data-ttu-id="afd15-139">Określa rozmiar tematu w bajtach.</span><span class="sxs-lookup"><span data-stu-id="afd15-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="afd15-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="afd15-140">-SupportOrdering</span></span>
<span data-ttu-id="afd15-141">Wskazuje, czy temat obsługuje porządkowanie.</span><span class="sxs-lookup"><span data-stu-id="afd15-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="afd15-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afd15-142">-Confirm</span></span>
<span data-ttu-id="afd15-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd15-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd15-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd15-144">-WhatIf</span></span>
<span data-ttu-id="afd15-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd15-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd15-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afd15-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd15-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd15-147">-DefaultProfile</span></span>
<span data-ttu-id="afd15-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afd15-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd15-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afd15-149">-Name</span></span>
<span data-ttu-id="afd15-150">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="afd15-150">Topic Name.</span></span>

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

### <span data-ttu-id="afd15-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="afd15-151">-Namespace</span></span>
<span data-ttu-id="afd15-152">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="afd15-152">Namespace Name.</span></span>

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

### <span data-ttu-id="afd15-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd15-153">-ResourceGroupName</span></span>
<span data-ttu-id="afd15-154">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="afd15-154">The name of the resource group</span></span>

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

### <span data-ttu-id="afd15-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd15-155">CommonParameters</span></span>
<span data-ttu-id="afd15-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd15-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd15-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd15-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd15-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd15-158">INPUTS</span></span>

### <span data-ttu-id="afd15-159">System. String</span><span class="sxs-lookup"><span data-stu-id="afd15-159">System.String</span></span>
<span data-ttu-id="afd15-160">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="afd15-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="afd15-161">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="afd15-161">-ResourceGroup</span></span>
 <span data-ttu-id="afd15-162">System. String</span><span class="sxs-lookup"><span data-stu-id="afd15-162">System.String</span></span>

### <span data-ttu-id="afd15-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="afd15-163">-NamespaceName</span></span>
 <span data-ttu-id="afd15-164">System. String</span><span class="sxs-lookup"><span data-stu-id="afd15-164">System.String</span></span>

### <span data-ttu-id="afd15-165">-Tematname</span><span class="sxs-lookup"><span data-stu-id="afd15-165">-TopicName</span></span>
 <span data-ttu-id="afd15-166">System. String</span><span class="sxs-lookup"><span data-stu-id="afd15-166">System.String</span></span>

### <span data-ttu-id="afd15-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="afd15-167">-EnablePartitioning</span></span>
 <span data-ttu-id="afd15-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="afd15-168">System.Boolean?</span></span>

## <span data-ttu-id="afd15-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afd15-169">OUTPUTS</span></span>

### <span data-ttu-id="afd15-170">Microsoft. Azure. Commands. ServiceBus. models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="afd15-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="afd15-171">Nazwa: SB-Topic_exampl1 lokalizacji: zachodni numer w Stanach Zjednoczonych:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 typ: Microsoft. ServiceBus/temat AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 AM CountDetails: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: 16384 IsAnonymousAccessible: false MaxSizeInMegabytes:: false RequiresDuplicateDetection: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="afd15-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="afd15-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afd15-172">NOTES</span></span>

## <span data-ttu-id="afd15-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afd15-173">RELATED LINKS</span></span>

