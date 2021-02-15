---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242194"
---
# <span data-ttu-id="9d47e-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="9d47e-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="9d47e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d47e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d47e-103">Aktualizuje opis kolejki autobusu usług w określonej przestrzeni nazw tego typu.</span><span class="sxs-lookup"><span data-stu-id="9d47e-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9d47e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d47e-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d47e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d47e-105">DESCRIPTION</span></span>
<span data-ttu-id="9d47e-106">Polecenie **cmdlet Set-AzServiceBusQueue** aktualizuje opis kolejki autobusu usług w określonej przestrzeni nazw tego typu.</span><span class="sxs-lookup"><span data-stu-id="9d47e-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9d47e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d47e-107">EXAMPLES</span></span>

### <span data-ttu-id="9d47e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d47e-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="9d47e-109">Aktualizuje określoną kolejkę przy użyciu nowego opisu w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="9d47e-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="9d47e-110">W tym przykładzie właściwość **DeadLetteringOnMessageExpiration jest** aktualizowana na **prawda,** a **właściwość SupportOrdering ma** wartość **true.**</span><span class="sxs-lookup"><span data-stu-id="9d47e-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="9d47e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d47e-111">PARAMETERS</span></span>

### <span data-ttu-id="9d47e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d47e-112">-DefaultProfile</span></span>
<span data-ttu-id="9d47e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d47e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d47e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d47e-114">-InputObject</span></span>
<span data-ttu-id="9d47e-115">Definicja usługi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="9d47e-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d47e-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d47e-116">-Name</span></span>
<span data-ttu-id="9d47e-117">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="9d47e-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d47e-118">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="9d47e-118">-Namespace</span></span>
<span data-ttu-id="9d47e-119">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="9d47e-119">Namespace Name.</span></span>

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

### <span data-ttu-id="9d47e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d47e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9d47e-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9d47e-121">The name of the resource group</span></span>

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

### <span data-ttu-id="9d47e-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d47e-122">-Confirm</span></span>
<span data-ttu-id="9d47e-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d47e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d47e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d47e-124">-WhatIf</span></span>
<span data-ttu-id="9d47e-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d47e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d47e-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d47e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d47e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d47e-127">CommonParameters</span></span>
<span data-ttu-id="9d47e-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d47e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d47e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d47e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d47e-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d47e-130">INPUTS</span></span>

### <span data-ttu-id="9d47e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9d47e-131">System.String</span></span>

### <span data-ttu-id="9d47e-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="9d47e-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="9d47e-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d47e-133">OUTPUTS</span></span>

### <span data-ttu-id="9d47e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="9d47e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="9d47e-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d47e-135">NOTES</span></span>

## <span data-ttu-id="9d47e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d47e-136">RELATED LINKS</span></span>
