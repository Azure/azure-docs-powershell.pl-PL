---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062071"
---
# <span data-ttu-id="bb5d5-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bb5d5-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="bb5d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5d5-103">Aktualizuje opis subskrypcji tematu magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bb5d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb5d5-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb5d5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb5d5-105">DESCRIPTION</span></span>
<span data-ttu-id="bb5d5-106">Polecenie cmdlet **Set-AzServiceBusSubscription** umożliwia zaktualizowanie opisu subskrypcji tematu usługi Service Bus w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bb5d5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb5d5-107">EXAMPLES</span></span>

### <span data-ttu-id="bb5d5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb5d5-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="bb5d5-109">Umożliwia zaktualizowanie opisu określonej subskrypcji do danego tematu.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="bb5d5-110">W tym przykładzie jest aktualizowana Właściwość **DeadLetteringOnMessageExpiration** na **wartość PRAWDA** i **MaxDeliveryCount** .</span><span class="sxs-lookup"><span data-stu-id="bb5d5-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="bb5d5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb5d5-111">PARAMETERS</span></span>

### <span data-ttu-id="bb5d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5d5-112">-DefaultProfile</span></span>
<span data-ttu-id="bb5d5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb5d5-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb5d5-114">-InputObject</span></span>
<span data-ttu-id="bb5d5-115">Definicja subskrypcji usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5d5-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb5d5-116">-Namespace</span></span>
<span data-ttu-id="bb5d5-117">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-117">Namespace Name.</span></span>

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

### <span data-ttu-id="bb5d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb5d5-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb5d5-119">The name of the resource group</span></span>

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

### <span data-ttu-id="bb5d5-120">— Temat</span><span class="sxs-lookup"><span data-stu-id="bb5d5-120">-Topic</span></span>
<span data-ttu-id="bb5d5-121">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-121">Topic Name.</span></span>

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

### <span data-ttu-id="bb5d5-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb5d5-122">-Confirm</span></span>
<span data-ttu-id="bb5d5-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb5d5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb5d5-124">-WhatIf</span></span>
<span data-ttu-id="bb5d5-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb5d5-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb5d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5d5-127">CommonParameters</span></span>
<span data-ttu-id="bb5d5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5d5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5d5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5d5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb5d5-130">INPUTS</span></span>

### <span data-ttu-id="bb5d5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bb5d5-131">System.String</span></span>

### <span data-ttu-id="bb5d5-132">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bb5d5-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bb5d5-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb5d5-133">OUTPUTS</span></span>

### <span data-ttu-id="bb5d5-134">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bb5d5-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bb5d5-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb5d5-135">NOTES</span></span>

## <span data-ttu-id="bb5d5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb5d5-136">RELATED LINKS</span></span>
