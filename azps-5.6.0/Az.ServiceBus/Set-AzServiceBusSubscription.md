---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: e19906f4a26f39929c62ffba89bd54092b4c961c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988835"
---
# <span data-ttu-id="bf315-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bf315-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="bf315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf315-102">SYNOPSIS</span></span>
<span data-ttu-id="bf315-103">Aktualizuje opis subskrypcji tematu "Autobus usług" w określonej przestrzeni nazw tego typu.</span><span class="sxs-lookup"><span data-stu-id="bf315-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bf315-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf315-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf315-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf315-105">DESCRIPTION</span></span>
<span data-ttu-id="bf315-106">Polecenie **cmdlet Set-AzServiceBusSubscription** aktualizuje opis subskrypcji dla tematu Autobus usługi w określonej przestrzeni nazw tego typu.</span><span class="sxs-lookup"><span data-stu-id="bf315-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bf315-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf315-107">EXAMPLES</span></span>

### <span data-ttu-id="bf315-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf315-108">Example 1</span></span>
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

<span data-ttu-id="bf315-109">Aktualizuje opis określonej subskrypcji dla danego tematu.</span><span class="sxs-lookup"><span data-stu-id="bf315-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="bf315-110">W tym przykładzie właściwość **DeadLetteringOnMessageExpiration ma wartość** **true,** a **funkcja MaxDeliveryCount** ma wartość 9.</span><span class="sxs-lookup"><span data-stu-id="bf315-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="bf315-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf315-111">PARAMETERS</span></span>

### <span data-ttu-id="bf315-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf315-112">-DefaultProfile</span></span>
<span data-ttu-id="bf315-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf315-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf315-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf315-114">-InputObject</span></span>
<span data-ttu-id="bf315-115">Definicja subskrypcji usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bf315-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="bf315-116">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="bf315-116">-Namespace</span></span>
<span data-ttu-id="bf315-117">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="bf315-117">Namespace Name.</span></span>

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

### <span data-ttu-id="bf315-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf315-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf315-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bf315-119">The name of the resource group</span></span>

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

### <span data-ttu-id="bf315-120">— Temat</span><span class="sxs-lookup"><span data-stu-id="bf315-120">-Topic</span></span>
<span data-ttu-id="bf315-121">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="bf315-121">Topic Name.</span></span>

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

### <span data-ttu-id="bf315-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf315-122">-Confirm</span></span>
<span data-ttu-id="bf315-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bf315-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf315-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf315-124">-WhatIf</span></span>
<span data-ttu-id="bf315-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf315-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf315-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bf315-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf315-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf315-127">CommonParameters</span></span>
<span data-ttu-id="bf315-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf315-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf315-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf315-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf315-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf315-130">INPUTS</span></span>

### <span data-ttu-id="bf315-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bf315-131">System.String</span></span>

### <span data-ttu-id="bf315-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bf315-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bf315-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf315-133">OUTPUTS</span></span>

### <span data-ttu-id="bf315-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bf315-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bf315-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf315-135">NOTES</span></span>

## <span data-ttu-id="bf315-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf315-136">RELATED LINKS</span></span>
