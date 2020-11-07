---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: b08b4d9bd201f8a29ef878a4aaa73c926eb47151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546475"
---
# <span data-ttu-id="9e3ba-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="9e3ba-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="9e3ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3ba-103">Aktualizuje opis tematu magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e3ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e3ba-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e3ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="9e3ba-106">Polecenie cmdlet **Set-AzureRmServiceBusTopic** umożliwia zaktualizowanie obiektu opisu dla tematu magistrali usług w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9e3ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e3ba-107">EXAMPLES</span></span>

### <span data-ttu-id="9e3ba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e3ba-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

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

<span data-ttu-id="9e3ba-109">Umożliwia zaktualizowanie określonego tematu o nowy opis w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="9e3ba-110">W tym przykładzie jest aktualizowana Właściwość **EnableExpress** na **wartość true**.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="9e3ba-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e3ba-111">PARAMETERS</span></span>

### <span data-ttu-id="9e3ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3ba-112">-DefaultProfile</span></span>
<span data-ttu-id="9e3ba-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e3ba-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e3ba-114">-InputObject</span></span>
<span data-ttu-id="9e3ba-115">Definicja tematu ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="9e3ba-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e3ba-116">-Name</span></span>
<span data-ttu-id="9e3ba-117">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-117">Topic Name.</span></span>

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

### <span data-ttu-id="9e3ba-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e3ba-118">-Namespace</span></span>
<span data-ttu-id="9e3ba-119">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-119">Namespace Name.</span></span>

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

### <span data-ttu-id="9e3ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e3ba-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9e3ba-121">The name of the resource group</span></span>

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

### <span data-ttu-id="9e3ba-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e3ba-122">-Confirm</span></span>
<span data-ttu-id="9e3ba-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3ba-124">-WhatIf</span></span>
<span data-ttu-id="9e3ba-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3ba-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e3ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3ba-127">CommonParameters</span></span>
<span data-ttu-id="9e3ba-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3ba-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3ba-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e3ba-130">INPUTS</span></span>

### <span data-ttu-id="9e3ba-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e3ba-131">System.String</span></span>

### <span data-ttu-id="9e3ba-132">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="9e3ba-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="9e3ba-133">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e3ba-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9e3ba-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e3ba-134">OUTPUTS</span></span>

### <span data-ttu-id="9e3ba-135">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="9e3ba-135">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="9e3ba-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e3ba-136">NOTES</span></span>

## <span data-ttu-id="9e3ba-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e3ba-137">RELATED LINKS</span></span>