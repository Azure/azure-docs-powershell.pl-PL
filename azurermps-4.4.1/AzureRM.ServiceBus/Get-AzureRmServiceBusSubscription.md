---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527298"
---
# <span data-ttu-id="44234-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="44234-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="44234-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44234-102">SYNOPSIS</span></span>
<span data-ttu-id="44234-103">Zwraca opis abonamentu dla określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="44234-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44234-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44234-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44234-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44234-105">DESCRIPTION</span></span>
<span data-ttu-id="44234-106">Polecenie cmdlet **Get-AzureRmServiceBusSubscription** zwraca opis subskrypcji określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="44234-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="44234-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44234-107">EXAMPLES</span></span>

### <span data-ttu-id="44234-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44234-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="44234-109">Zwraca opis abonamentu dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="44234-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="44234-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44234-110">PARAMETERS</span></span>

### <span data-ttu-id="44234-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44234-111">-DefaultProfile</span></span>
<span data-ttu-id="44234-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44234-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44234-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44234-113">-Name</span></span>
<span data-ttu-id="44234-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="44234-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44234-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="44234-115">-Namespace</span></span>
<span data-ttu-id="44234-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="44234-116">Namespace Name.</span></span>

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

### <span data-ttu-id="44234-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44234-117">-ResourceGroupName</span></span>
<span data-ttu-id="44234-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44234-118">The name of the resource group</span></span>

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

### <span data-ttu-id="44234-119">— Temat</span><span class="sxs-lookup"><span data-stu-id="44234-119">-Topic</span></span>
<span data-ttu-id="44234-120">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="44234-120">Topic Name.</span></span>

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

### <span data-ttu-id="44234-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44234-121">CommonParameters</span></span>
<span data-ttu-id="44234-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44234-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44234-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44234-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44234-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44234-124">INPUTS</span></span>

### <span data-ttu-id="44234-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="44234-125">-ResourceGroup</span></span>
 <span data-ttu-id="44234-126">System. String</span><span class="sxs-lookup"><span data-stu-id="44234-126">System.String</span></span>
 

### <span data-ttu-id="44234-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="44234-127">-NamespaceName</span></span>
 <span data-ttu-id="44234-128">System. String</span><span class="sxs-lookup"><span data-stu-id="44234-128">System.String</span></span>
 

### <span data-ttu-id="44234-129">-Tematname</span><span class="sxs-lookup"><span data-stu-id="44234-129">-TopicName</span></span>
 <span data-ttu-id="44234-130">System. String</span><span class="sxs-lookup"><span data-stu-id="44234-130">System.String</span></span>
 

### <span data-ttu-id="44234-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="44234-131">-SubscriptionName</span></span>
 <span data-ttu-id="44234-132">System. String</span><span class="sxs-lookup"><span data-stu-id="44234-132">System.String</span></span>
 

## <span data-ttu-id="44234-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44234-133">OUTPUTS</span></span>

### <span data-ttu-id="44234-134">Microsoft. Azure. Commands. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="44234-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="44234-135">Nazwa: SB-TopicSubscription — lokalizacja example1: zachodni stan AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. MODELES. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: DeadLetteringOnMessageExpiration: EnableBatchedOperations: 00:01:00 EntityAvailabilityStatus: true IsReadOnly: Microsoft LockDuration: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="44234-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="44234-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44234-136">NOTES</span></span>

## <span data-ttu-id="44234-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44234-137">RELATED LINKS</span></span>

