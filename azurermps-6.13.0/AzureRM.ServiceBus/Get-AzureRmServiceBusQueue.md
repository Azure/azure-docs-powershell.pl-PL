---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 25a64b352622cf9c057ce0e3f38bc3e4e122e22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717368"
---
# <span data-ttu-id="713f5-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="713f5-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="713f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="713f5-102">SYNOPSIS</span></span>
<span data-ttu-id="713f5-103">Zwraca opis określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="713f5-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="713f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="713f5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="713f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="713f5-105">DESCRIPTION</span></span>
<span data-ttu-id="713f5-106">Zwraca opis określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="713f5-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="713f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="713f5-107">EXAMPLES</span></span>

### <span data-ttu-id="713f5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="713f5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

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
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="713f5-109">Zwraca opis kolejki.</span><span class="sxs-lookup"><span data-stu-id="713f5-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="713f5-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="713f5-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="713f5-111">Zwraca listę kolejek dla danego obszaru nazw, a domyślnie zostaną zwrócone kolejki usługi 100, jeśli do zwrócenia więcej niż 100 kolejek, należy użyć parametru-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="713f5-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="713f5-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="713f5-112">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="713f5-113">Zwraca listę pierwszych kolejek usługi 150 dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="713f5-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="713f5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="713f5-114">PARAMETERS</span></span>

### <span data-ttu-id="713f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713f5-115">-DefaultProfile</span></span>
<span data-ttu-id="713f5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="713f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="713f5-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="713f5-117">-MaxCount</span></span>
<span data-ttu-id="713f5-118">Określ maksymalną liczbę zwracanych kolejek.</span><span class="sxs-lookup"><span data-stu-id="713f5-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="713f5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="713f5-119">-Name</span></span>
<span data-ttu-id="713f5-120">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="713f5-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="713f5-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="713f5-121">-Namespace</span></span>
<span data-ttu-id="713f5-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="713f5-122">Namespace Name</span></span>

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

### <span data-ttu-id="713f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="713f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="713f5-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="713f5-124">The name of the resource group</span></span>

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

### <span data-ttu-id="713f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713f5-125">CommonParameters</span></span>
<span data-ttu-id="713f5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="713f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713f5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="713f5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713f5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="713f5-128">INPUTS</span></span>

### <span data-ttu-id="713f5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="713f5-129">System.String</span></span>

## <span data-ttu-id="713f5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="713f5-130">OUTPUTS</span></span>

### <span data-ttu-id="713f5-131">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="713f5-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="713f5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="713f5-132">NOTES</span></span>

## <span data-ttu-id="713f5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="713f5-133">RELATED LINKS</span></span>
