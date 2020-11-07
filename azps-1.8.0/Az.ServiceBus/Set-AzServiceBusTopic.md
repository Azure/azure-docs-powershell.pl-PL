---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 67ce9249134365aa182024dff6e5913f68e11738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708101"
---
# <span data-ttu-id="6f05c-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6f05c-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="6f05c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f05c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f05c-103">Aktualizuje opis tematu magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6f05c-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6f05c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f05c-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f05c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f05c-105">DESCRIPTION</span></span>
<span data-ttu-id="6f05c-106">Polecenie cmdlet **Set-AzServiceBusTopic** umożliwia zaktualizowanie obiektu opisu dla tematu magistrali usług w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="6f05c-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6f05c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f05c-107">EXAMPLES</span></span>

### <span data-ttu-id="6f05c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f05c-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="6f05c-109">Umożliwia zaktualizowanie określonego tematu o nowy opis w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="6f05c-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="6f05c-110">W tym przykładzie jest aktualizowana Właściwość **EnableExpress** na **wartość true**.</span><span class="sxs-lookup"><span data-stu-id="6f05c-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="6f05c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f05c-111">PARAMETERS</span></span>

### <span data-ttu-id="6f05c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f05c-112">-DefaultProfile</span></span>
<span data-ttu-id="6f05c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f05c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f05c-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6f05c-114">-InputObject</span></span>
<span data-ttu-id="6f05c-115">Definicja tematu ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6f05c-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f05c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f05c-116">-Name</span></span>
<span data-ttu-id="6f05c-117">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="6f05c-117">Topic Name.</span></span>

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

### <span data-ttu-id="6f05c-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6f05c-118">-Namespace</span></span>
<span data-ttu-id="6f05c-119">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6f05c-119">Namespace Name.</span></span>

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

### <span data-ttu-id="6f05c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f05c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f05c-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6f05c-121">The name of the resource group</span></span>

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

### <span data-ttu-id="6f05c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f05c-122">-Confirm</span></span>
<span data-ttu-id="6f05c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f05c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f05c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f05c-124">-WhatIf</span></span>
<span data-ttu-id="6f05c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f05c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f05c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f05c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f05c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f05c-127">CommonParameters</span></span>
<span data-ttu-id="6f05c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f05c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f05c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f05c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f05c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f05c-130">INPUTS</span></span>

### <span data-ttu-id="6f05c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6f05c-131">System.String</span></span>

### <span data-ttu-id="6f05c-132">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="6f05c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="6f05c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f05c-133">OUTPUTS</span></span>

### <span data-ttu-id="6f05c-134">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="6f05c-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="6f05c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f05c-135">NOTES</span></span>

## <span data-ttu-id="6f05c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f05c-136">RELATED LINKS</span></span>