---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 3d99b261dc65af5d19a93acb575116a91c8a97fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551584"
---
# <span data-ttu-id="fda61-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="fda61-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="fda61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fda61-102">SYNOPSIS</span></span>
<span data-ttu-id="fda61-103">Zwraca opis abonamentu dla określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="fda61-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fda61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fda61-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fda61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fda61-105">DESCRIPTION</span></span>
<span data-ttu-id="fda61-106">Polecenie cmdlet **Get-AzureRmServiceBusSubscription** zwraca opis subskrypcji określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="fda61-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="fda61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fda61-107">EXAMPLES</span></span>

### <span data-ttu-id="fda61-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fda61-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="fda61-109">Zwraca opis abonamentu dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="fda61-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="fda61-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fda61-110">PARAMETERS</span></span>

### <span data-ttu-id="fda61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda61-111">-DefaultProfile</span></span>
<span data-ttu-id="fda61-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fda61-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fda61-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fda61-113">-Name</span></span>
<span data-ttu-id="fda61-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fda61-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda61-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fda61-115">-Namespace</span></span>
<span data-ttu-id="fda61-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="fda61-116">Namespace Name.</span></span>

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

### <span data-ttu-id="fda61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda61-117">-ResourceGroupName</span></span>
<span data-ttu-id="fda61-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fda61-118">The name of the resource group</span></span>

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

### <span data-ttu-id="fda61-119">— Temat</span><span class="sxs-lookup"><span data-stu-id="fda61-119">-Topic</span></span>
<span data-ttu-id="fda61-120">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="fda61-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda61-121">CommonParameters</span></span>
<span data-ttu-id="fda61-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda61-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda61-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda61-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fda61-124">INPUTS</span></span>

### <span data-ttu-id="fda61-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fda61-125">-ResourceGroup</span></span>
 <span data-ttu-id="fda61-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fda61-126">System.String</span></span>
 

### <span data-ttu-id="fda61-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="fda61-127">-NamespaceName</span></span>
 <span data-ttu-id="fda61-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fda61-128">System.String</span></span>
 

### <span data-ttu-id="fda61-129">-Tematname</span><span class="sxs-lookup"><span data-stu-id="fda61-129">-TopicName</span></span>
 <span data-ttu-id="fda61-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fda61-130">System.String</span></span>
 

### <span data-ttu-id="fda61-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="fda61-131">-SubscriptionName</span></span>
 <span data-ttu-id="fda61-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fda61-132">System.String</span></span>
 

## <span data-ttu-id="fda61-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fda61-133">OUTPUTS</span></span>

### <span data-ttu-id="fda61-134">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="fda61-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="fda61-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fda61-135">NOTES</span></span>

## <span data-ttu-id="fda61-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fda61-136">RELATED LINKS</span></span>

