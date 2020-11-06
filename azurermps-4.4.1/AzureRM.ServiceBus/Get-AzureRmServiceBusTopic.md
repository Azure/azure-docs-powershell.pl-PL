---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527290"
---
# <span data-ttu-id="51440-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="51440-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="51440-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51440-102">SYNOPSIS</span></span>
<span data-ttu-id="51440-103">Zwraca opis określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="51440-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51440-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51440-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51440-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51440-105">DESCRIPTION</span></span>
<span data-ttu-id="51440-106">Polecenie cmdlet **Get-AzureRmServiceBusTopic** zwraca opis tematu dla określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="51440-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="51440-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51440-107">EXAMPLES</span></span>

### <span data-ttu-id="51440-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51440-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="51440-109">Zwraca opis określonego tematu dla danego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="51440-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="51440-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51440-110">PARAMETERS</span></span>

### <span data-ttu-id="51440-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51440-111">-DefaultProfile</span></span>
<span data-ttu-id="51440-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51440-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51440-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51440-113">-Name</span></span>
<span data-ttu-id="51440-114">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="51440-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51440-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51440-115">-Namespace</span></span>
<span data-ttu-id="51440-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="51440-116">Namespace Name.</span></span>

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

### <span data-ttu-id="51440-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51440-117">-ResourceGroupName</span></span>
<span data-ttu-id="51440-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="51440-118">The name of the resource group</span></span>

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

### <span data-ttu-id="51440-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51440-119">CommonParameters</span></span>
<span data-ttu-id="51440-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51440-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51440-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51440-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51440-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51440-122">INPUTS</span></span>

### <span data-ttu-id="51440-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="51440-123">-ResourceGroup</span></span>
 <span data-ttu-id="51440-124">System. String</span><span class="sxs-lookup"><span data-stu-id="51440-124">System.String</span></span>
 

### <span data-ttu-id="51440-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="51440-125">-NamespaceName</span></span>
 <span data-ttu-id="51440-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51440-126">System.String</span></span>
 

### <span data-ttu-id="51440-127">-Tematname</span><span class="sxs-lookup"><span data-stu-id="51440-127">-TopicName</span></span>
 <span data-ttu-id="51440-128">System. String</span><span class="sxs-lookup"><span data-stu-id="51440-128">System.String</span></span>

## <span data-ttu-id="51440-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51440-129">OUTPUTS</span></span>

### <span data-ttu-id="51440-130">Microsoft. Azure. Commands. ServiceBus. models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="51440-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="51440-131">Nazwa: SB-Topic_exampl1 lokalizacja:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 typ: Microsoft. ServiceBus/temat AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. MODELES. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: prawda EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: 16384 IsAnonymousAccessible:. Jeżeli, stan: Active MaxSizeInMegabytes: 1 RequiresDuplicateDetection: false SizeInBytes: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="51440-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="51440-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51440-132">NOTES</span></span>

## <span data-ttu-id="51440-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51440-133">RELATED LINKS</span></span>

