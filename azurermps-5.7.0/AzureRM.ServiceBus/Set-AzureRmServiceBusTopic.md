---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542272"
---
# <span data-ttu-id="6c084-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6c084-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="6c084-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c084-102">SYNOPSIS</span></span>
<span data-ttu-id="6c084-103">Aktualizuje opis tematu magistrali usług w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6c084-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c084-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c084-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c084-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c084-105">DESCRIPTION</span></span>
<span data-ttu-id="6c084-106">Polecenie cmdlet **Set-AzureRmServiceBusTopic** umożliwia zaktualizowanie obiektu opisu dla tematu magistrali usług w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="6c084-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6c084-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c084-107">EXAMPLES</span></span>

### <span data-ttu-id="6c084-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c084-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="6c084-109">Umożliwia zaktualizowanie określonego tematu o nowy opis w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="6c084-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="6c084-110">W tym przykładzie jest aktualizowana Właściwość **EnableExpress** na **wartość true**.</span><span class="sxs-lookup"><span data-stu-id="6c084-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="6c084-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c084-111">PARAMETERS</span></span>

### <span data-ttu-id="6c084-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c084-112">-DefaultProfile</span></span>
<span data-ttu-id="6c084-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c084-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c084-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c084-114">-InputObject</span></span>
<span data-ttu-id="6c084-115">Definicja tematu ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6c084-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c084-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c084-116">-Name</span></span>
<span data-ttu-id="6c084-117">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="6c084-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c084-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c084-118">-Namespace</span></span>
<span data-ttu-id="6c084-119">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6c084-119">Namespace Name.</span></span>

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

### <span data-ttu-id="6c084-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c084-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c084-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c084-121">The name of the resource group</span></span>

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

### <span data-ttu-id="6c084-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c084-122">-Confirm</span></span>
<span data-ttu-id="6c084-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c084-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c084-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c084-124">-WhatIf</span></span>
<span data-ttu-id="6c084-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c084-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c084-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c084-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c084-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c084-127">CommonParameters</span></span>
<span data-ttu-id="6c084-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c084-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c084-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c084-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c084-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c084-130">INPUTS</span></span>

### <span data-ttu-id="6c084-131">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6c084-131">-ResourceGroup</span></span>
 <span data-ttu-id="6c084-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6c084-132">System.String</span></span>

### <span data-ttu-id="6c084-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6c084-133">-NamespaceName</span></span>
 <span data-ttu-id="6c084-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6c084-134">System.String</span></span>

### <span data-ttu-id="6c084-135">-Tematname</span><span class="sxs-lookup"><span data-stu-id="6c084-135">-TopicName</span></span>
 <span data-ttu-id="6c084-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c084-136">System.String</span></span>

### <span data-ttu-id="6c084-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="6c084-137">-TopicObj</span></span>
 <span data-ttu-id="6c084-138">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="6c084-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="6c084-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c084-139">OUTPUTS</span></span>

### <span data-ttu-id="6c084-140">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="6c084-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="6c084-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c084-141">NOTES</span></span>

## <span data-ttu-id="6c084-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c084-142">RELATED LINKS</span></span>

