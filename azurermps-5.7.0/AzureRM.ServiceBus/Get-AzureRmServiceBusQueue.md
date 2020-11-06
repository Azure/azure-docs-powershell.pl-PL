---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542280"
---
# <span data-ttu-id="91337-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="91337-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="91337-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91337-102">SYNOPSIS</span></span>
<span data-ttu-id="91337-103">Zwraca opis określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="91337-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91337-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91337-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91337-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91337-105">DESCRIPTION</span></span>
<span data-ttu-id="91337-106">Polecenie cmdlet **Get-AzureRmServiceBusQueue** zwraca opis określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="91337-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="91337-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91337-107">EXAMPLES</span></span>

### <span data-ttu-id="91337-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91337-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="91337-109">Zwraca opis kolejki.</span><span class="sxs-lookup"><span data-stu-id="91337-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="91337-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91337-110">PARAMETERS</span></span>

### <span data-ttu-id="91337-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91337-111">-DefaultProfile</span></span>
<span data-ttu-id="91337-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91337-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91337-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91337-113">-Name</span></span>
<span data-ttu-id="91337-114">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="91337-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91337-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="91337-115">-Namespace</span></span>
<span data-ttu-id="91337-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="91337-116">Namespace Name.</span></span>

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

### <span data-ttu-id="91337-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91337-117">-ResourceGroupName</span></span>
<span data-ttu-id="91337-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="91337-118">The name of the resource group</span></span>

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

### <span data-ttu-id="91337-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91337-119">CommonParameters</span></span>
<span data-ttu-id="91337-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91337-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91337-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91337-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91337-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91337-122">INPUTS</span></span>

### <span data-ttu-id="91337-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="91337-123">-ResourceGroup</span></span>
 <span data-ttu-id="91337-124">System. String</span><span class="sxs-lookup"><span data-stu-id="91337-124">System.String</span></span>
 

### <span data-ttu-id="91337-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="91337-125">-NamespaceName</span></span>
 <span data-ttu-id="91337-126">System. String</span><span class="sxs-lookup"><span data-stu-id="91337-126">System.String</span></span>
 

### <span data-ttu-id="91337-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="91337-127">-QueueName</span></span>
 <span data-ttu-id="91337-128">System. String</span><span class="sxs-lookup"><span data-stu-id="91337-128">System.String</span></span> 

## <span data-ttu-id="91337-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91337-129">OUTPUTS</span></span>

### <span data-ttu-id="91337-130">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="91337-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="91337-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91337-131">NOTES</span></span>

## <span data-ttu-id="91337-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91337-132">RELATED LINKS</span></span>

