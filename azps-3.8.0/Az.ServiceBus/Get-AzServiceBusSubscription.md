---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052702"
---
# <span data-ttu-id="3eb77-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="3eb77-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="3eb77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3eb77-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb77-103">Zwraca opis abonamentu dla określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="3eb77-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="3eb77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3eb77-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3eb77-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb77-106">Polecenie cmdlet **Get-AzServiceBusSubscription** zwraca opis subskrypcji określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="3eb77-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="3eb77-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3eb77-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb77-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3eb77-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="3eb77-109">Zwraca opis abonamentu dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="3eb77-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="3eb77-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3eb77-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="3eb77-111">Zwraca listę subskrypcji określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="3eb77-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="3eb77-112">Domyślnie zostaną zwrócone subskrypcje 100 dotyczące liczby subskrypcji. Użyj parametru-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3eb77-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="3eb77-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3eb77-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="3eb77-114">Zwraca listę pierwszych 150 subskrypcji dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="3eb77-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="3eb77-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3eb77-115">PARAMETERS</span></span>

### <span data-ttu-id="3eb77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb77-116">-DefaultProfile</span></span>
<span data-ttu-id="3eb77-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb77-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3eb77-118">-MaxCount</span></span>
<span data-ttu-id="3eb77-119">Określ maksymalną liczbę zwracanych abonamentów.</span><span class="sxs-lookup"><span data-stu-id="3eb77-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="3eb77-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3eb77-120">-Name</span></span>
<span data-ttu-id="3eb77-121">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3eb77-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb77-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3eb77-122">-Namespace</span></span>
<span data-ttu-id="3eb77-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="3eb77-123">Namespace Name</span></span>

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

### <span data-ttu-id="3eb77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb77-124">-ResourceGroupName</span></span>
<span data-ttu-id="3eb77-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3eb77-125">The name of the resource group</span></span>

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

### <span data-ttu-id="3eb77-126">— Temat</span><span class="sxs-lookup"><span data-stu-id="3eb77-126">-Topic</span></span>
<span data-ttu-id="3eb77-127">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="3eb77-127">Topic Name</span></span>

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

### <span data-ttu-id="3eb77-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb77-128">CommonParameters</span></span>
<span data-ttu-id="3eb77-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb77-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb77-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb77-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb77-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3eb77-131">INPUTS</span></span>

### <span data-ttu-id="3eb77-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3eb77-132">System.String</span></span>

## <span data-ttu-id="3eb77-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3eb77-133">OUTPUTS</span></span>

### <span data-ttu-id="3eb77-134">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="3eb77-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="3eb77-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3eb77-135">NOTES</span></span>

## <span data-ttu-id="3eb77-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3eb77-136">RELATED LINKS</span></span>
