---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242226"
---
# <span data-ttu-id="55846-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="55846-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="55846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55846-102">SYNOPSIS</span></span>
<span data-ttu-id="55846-103">Zwraca opis subskrypcji dla określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="55846-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="55846-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55846-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55846-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="55846-105">DESCRIPTION</span></span>
<span data-ttu-id="55846-106">Polecenie **cmdlet Get-AzServiceBusSubscription** zwraca opis subskrypcji dla określonego tematu typu usługi.</span><span class="sxs-lookup"><span data-stu-id="55846-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="55846-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55846-107">EXAMPLES</span></span>

### <span data-ttu-id="55846-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55846-108">Example 1</span></span>
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

<span data-ttu-id="55846-109">Zwraca opis subskrypcji dla określonego tematu "Service Bus" (Autobus usług).</span><span class="sxs-lookup"><span data-stu-id="55846-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="55846-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="55846-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="55846-111">Zwraca listę subskrypcji dla określonego tematu "Service Bus".</span><span class="sxs-lookup"><span data-stu-id="55846-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="55846-112">Domyślnie zostanie zwróconych 100 subskrypcji, dla liczby subskrypcji użyj parametru -MaxCount</span><span class="sxs-lookup"><span data-stu-id="55846-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="55846-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="55846-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="55846-114">Zwraca listę pierwszych 150 subskrypcji dla określonego tematu "Service Bus" (Autobus usług).</span><span class="sxs-lookup"><span data-stu-id="55846-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="55846-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55846-115">PARAMETERS</span></span>

### <span data-ttu-id="55846-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55846-116">-DefaultProfile</span></span>
<span data-ttu-id="55846-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55846-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55846-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="55846-118">-MaxCount</span></span>
<span data-ttu-id="55846-119">Określ maksymalną liczbę subskrypcji do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="55846-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="55846-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55846-120">-Name</span></span>
<span data-ttu-id="55846-121">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="55846-121">Subscription Name</span></span>

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

### <span data-ttu-id="55846-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="55846-122">-Namespace</span></span>
<span data-ttu-id="55846-123">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="55846-123">Namespace Name</span></span>

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

### <span data-ttu-id="55846-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55846-124">-ResourceGroupName</span></span>
<span data-ttu-id="55846-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55846-125">The name of the resource group</span></span>

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

### <span data-ttu-id="55846-126">— Temat</span><span class="sxs-lookup"><span data-stu-id="55846-126">-Topic</span></span>
<span data-ttu-id="55846-127">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="55846-127">Topic Name</span></span>

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

### <span data-ttu-id="55846-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55846-128">CommonParameters</span></span>
<span data-ttu-id="55846-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55846-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55846-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55846-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55846-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55846-131">INPUTS</span></span>

### <span data-ttu-id="55846-132">System.String</span><span class="sxs-lookup"><span data-stu-id="55846-132">System.String</span></span>

## <span data-ttu-id="55846-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55846-133">OUTPUTS</span></span>

### <span data-ttu-id="55846-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="55846-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="55846-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55846-135">NOTES</span></span>

## <span data-ttu-id="55846-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55846-136">RELATED LINKS</span></span>
