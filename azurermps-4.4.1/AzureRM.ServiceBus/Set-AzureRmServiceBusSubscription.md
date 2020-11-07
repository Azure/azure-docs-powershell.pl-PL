---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718984"
---
# <span data-ttu-id="80186-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="80186-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="80186-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80186-102">SYNOPSIS</span></span>
<span data-ttu-id="80186-103">Aktualizuje opis subskrypcji tematu magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="80186-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80186-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80186-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80186-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80186-105">DESCRIPTION</span></span>
<span data-ttu-id="80186-106">Polecenie cmdlet **Set-AzureRmServiceBusSubscription** umożliwia zaktualizowanie opisu subskrypcji tematu usługi Service Bus w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="80186-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="80186-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80186-107">EXAMPLES</span></span>

### <span data-ttu-id="80186-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80186-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="80186-109">Umożliwia zaktualizowanie opisu określonej subskrypcji do danego tematu.</span><span class="sxs-lookup"><span data-stu-id="80186-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="80186-110">W tym przykładzie jest aktualizowana Właściwość **DeadLetteringOnMessageExpiration** na **wartość PRAWDA** i **MaxDeliveryCount** .</span><span class="sxs-lookup"><span data-stu-id="80186-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="80186-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80186-111">PARAMETERS</span></span>

### <span data-ttu-id="80186-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80186-112">-Confirm</span></span>
<span data-ttu-id="80186-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80186-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80186-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80186-114">-WhatIf</span></span>
<span data-ttu-id="80186-115">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80186-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80186-116">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80186-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80186-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80186-117">-DefaultProfile</span></span>
<span data-ttu-id="80186-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80186-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80186-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80186-119">-InputObject</span></span>
<span data-ttu-id="80186-120">Definicja subskrypcji usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="80186-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80186-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80186-121">-Namespace</span></span>
<span data-ttu-id="80186-122">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="80186-122">Namespace Name.</span></span>

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

### <span data-ttu-id="80186-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80186-123">-ResourceGroupName</span></span>
<span data-ttu-id="80186-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="80186-124">The name of the resource group</span></span>

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

### <span data-ttu-id="80186-125">— Temat</span><span class="sxs-lookup"><span data-stu-id="80186-125">-Topic</span></span>
<span data-ttu-id="80186-126">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="80186-126">Topic Name.</span></span>

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

### <span data-ttu-id="80186-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80186-127">CommonParameters</span></span>
<span data-ttu-id="80186-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80186-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80186-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80186-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80186-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80186-130">INPUTS</span></span>

### <span data-ttu-id="80186-131">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="80186-131">-ResourceGroup</span></span>
 <span data-ttu-id="80186-132">System. String</span><span class="sxs-lookup"><span data-stu-id="80186-132">System.String</span></span>

### <span data-ttu-id="80186-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="80186-133">-NamespaceName</span></span>
 <span data-ttu-id="80186-134">System. String</span><span class="sxs-lookup"><span data-stu-id="80186-134">System.String</span></span>

### <span data-ttu-id="80186-135">-Tematname</span><span class="sxs-lookup"><span data-stu-id="80186-135">-TopicName</span></span>
 <span data-ttu-id="80186-136">System. String</span><span class="sxs-lookup"><span data-stu-id="80186-136">System.String</span></span>

### <span data-ttu-id="80186-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="80186-137">-SubscriptionObj</span></span>
 <span data-ttu-id="80186-138">Microsoft. Azure. Commands. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="80186-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="80186-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80186-139">OUTPUTS</span></span>

### <span data-ttu-id="80186-140">Microsoft. Azure. Commands. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="80186-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="80186-141">Name (nazwa): SB-TopicSubscription-example1 Location: zachodni stan AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: true EnableBatchedOperations: prawda EntityAvailabilityStatus: dostępne IsReadOnly: LockDuration: 00:01:00 1/20/2017 9:59:15 MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="80186-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="80186-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80186-142">NOTES</span></span>

## <span data-ttu-id="80186-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80186-143">RELATED LINKS</span></span>

