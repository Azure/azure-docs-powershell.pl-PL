---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: dbc3acdf65f97e5fa46d9359f1f7af43c2c137d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546476"
---
# <span data-ttu-id="9681c-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="9681c-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="9681c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9681c-102">SYNOPSIS</span></span>
<span data-ttu-id="9681c-103">Aktualizuje opis subskrypcji tematu magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9681c-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9681c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9681c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9681c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9681c-105">DESCRIPTION</span></span>
<span data-ttu-id="9681c-106">Polecenie cmdlet **Set-AzureRmServiceBusSubscription** umożliwia zaktualizowanie opisu subskrypcji tematu usługi Service Bus w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="9681c-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9681c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9681c-107">EXAMPLES</span></span>

### <span data-ttu-id="9681c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9681c-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="9681c-109">Umożliwia zaktualizowanie opisu określonej subskrypcji do danego tematu.</span><span class="sxs-lookup"><span data-stu-id="9681c-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="9681c-110">W tym przykładzie jest aktualizowana Właściwość **DeadLetteringOnMessageExpiration** na **wartość PRAWDA** i **MaxDeliveryCount** .</span><span class="sxs-lookup"><span data-stu-id="9681c-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="9681c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9681c-111">PARAMETERS</span></span>

### <span data-ttu-id="9681c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9681c-112">-DefaultProfile</span></span>
<span data-ttu-id="9681c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9681c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9681c-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9681c-114">-InputObject</span></span>
<span data-ttu-id="9681c-115">Definicja subskrypcji usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="9681c-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="9681c-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9681c-116">-Namespace</span></span>
<span data-ttu-id="9681c-117">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9681c-117">Namespace Name.</span></span>

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

### <span data-ttu-id="9681c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9681c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9681c-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9681c-119">The name of the resource group</span></span>

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

### <span data-ttu-id="9681c-120">— Temat</span><span class="sxs-lookup"><span data-stu-id="9681c-120">-Topic</span></span>
<span data-ttu-id="9681c-121">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="9681c-121">Topic Name.</span></span>

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

### <span data-ttu-id="9681c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9681c-122">-Confirm</span></span>
<span data-ttu-id="9681c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9681c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9681c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9681c-124">-WhatIf</span></span>
<span data-ttu-id="9681c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9681c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9681c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9681c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9681c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9681c-127">CommonParameters</span></span>
<span data-ttu-id="9681c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9681c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9681c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9681c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9681c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9681c-130">INPUTS</span></span>

### <span data-ttu-id="9681c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9681c-131">System.String</span></span>

### <span data-ttu-id="9681c-132">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="9681c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="9681c-133">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9681c-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9681c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9681c-134">OUTPUTS</span></span>

### <span data-ttu-id="9681c-135">Microsoft. Azure. Commands. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="9681c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="9681c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9681c-136">NOTES</span></span>

## <span data-ttu-id="9681c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9681c-137">RELATED LINKS</span></span>
