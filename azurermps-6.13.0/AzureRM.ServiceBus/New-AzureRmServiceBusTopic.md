---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: e2ca0b6902ecc13c9dfe4f418ea5d321b6e36dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543432"
---
# <span data-ttu-id="b465e-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b465e-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="b465e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b465e-102">SYNOPSIS</span></span>
<span data-ttu-id="b465e-103">Tworzy nowy temat magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="b465e-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b465e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b465e-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b465e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b465e-105">DESCRIPTION</span></span>
<span data-ttu-id="b465e-106">Polecenie cmdlet **New-AzureRmServiceBusTopic** tworzy nowy temat magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="b465e-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b465e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b465e-107">EXAMPLES</span></span>

### <span data-ttu-id="b465e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b465e-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="b465e-109">Tworzy nowy temat magistrali usług `SB-Topic_exampl1` w określonym obszarze nazw usługi Service Bus `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b465e-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="b465e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b465e-110">PARAMETERS</span></span>

### <span data-ttu-id="b465e-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b465e-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b465e-112">Określa interwał [bezczynności](https://msdn.microsoft.com/library/system.timespan.aspx) przedziału czasu, po upływie którego temat zostanie automatycznie usunięty.</span><span class="sxs-lookup"><span data-stu-id="b465e-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="b465e-113">Minimalny czas trwania to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="b465e-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b465e-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b465e-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b465e-115">Określa czas trwania, po upływie którego wiadomość wygasa, licząc od momentu wysłania wiadomości do usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="b465e-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="b465e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b465e-116">-DefaultProfile</span></span>
<span data-ttu-id="b465e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b465e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b465e-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b465e-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="b465e-119">Określa strukturę [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) definiującą czas trwania historii wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="b465e-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="b465e-120">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="b465e-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="b465e-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b465e-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="b465e-122">Wskazuje, czy są włączone operacje wsadowe po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="b465e-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="b465e-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="b465e-123">-EnableExpress</span></span>
<span data-ttu-id="b465e-124">Wskazuje, czy jednostki ekspresowe są włączone.</span><span class="sxs-lookup"><span data-stu-id="b465e-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="b465e-125">Kolejka ekspresowa przechowuje wiadomość w pamięci, zanim zapisze ją do magazynu trwałego.</span><span class="sxs-lookup"><span data-stu-id="b465e-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="b465e-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b465e-126">-EnablePartitioning</span></span>
<span data-ttu-id="b465e-127">Określa, czy chcesz, aby temat był podzielony na wiele brokerów wiadomości.</span><span class="sxs-lookup"><span data-stu-id="b465e-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="b465e-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b465e-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="b465e-129">Maksymalny rozmiar tematu w megabajtach, czyli rozmiar pamięci przydzielonej dla tego tematu.</span><span class="sxs-lookup"><span data-stu-id="b465e-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="b465e-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b465e-130">-Name</span></span>
<span data-ttu-id="b465e-131">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="b465e-131">Topic Name.</span></span>

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

### <span data-ttu-id="b465e-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b465e-132">-Namespace</span></span>
<span data-ttu-id="b465e-133">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b465e-133">Namespace Name.</span></span>

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

### <span data-ttu-id="b465e-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="b465e-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="b465e-135">Wskazuje, czy temat wymaga wykrywania duplikatów.</span><span class="sxs-lookup"><span data-stu-id="b465e-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="b465e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b465e-136">-ResourceGroupName</span></span>
<span data-ttu-id="b465e-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b465e-137">The name of the resource group</span></span>

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

### <span data-ttu-id="b465e-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b465e-138">-SizeInBytes</span></span>
<span data-ttu-id="b465e-139">Określa rozmiar tematu w bajtach.</span><span class="sxs-lookup"><span data-stu-id="b465e-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="b465e-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="b465e-140">-SupportOrdering</span></span>
<span data-ttu-id="b465e-141">Wskazuje, czy temat obsługuje porządkowanie.</span><span class="sxs-lookup"><span data-stu-id="b465e-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="b465e-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b465e-142">-Confirm</span></span>
<span data-ttu-id="b465e-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b465e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b465e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b465e-144">-WhatIf</span></span>
<span data-ttu-id="b465e-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b465e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b465e-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b465e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b465e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b465e-147">CommonParameters</span></span>
<span data-ttu-id="b465e-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b465e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b465e-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b465e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b465e-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b465e-150">INPUTS</span></span>

### <span data-ttu-id="b465e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b465e-151">System.String</span></span>

### <span data-ttu-id="b465e-152">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b465e-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b465e-153">System. Nullable "1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b465e-153">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b465e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b465e-154">OUTPUTS</span></span>

### <span data-ttu-id="b465e-155">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b465e-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b465e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b465e-156">NOTES</span></span>

## <span data-ttu-id="b465e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b465e-157">RELATED LINKS</span></span>
