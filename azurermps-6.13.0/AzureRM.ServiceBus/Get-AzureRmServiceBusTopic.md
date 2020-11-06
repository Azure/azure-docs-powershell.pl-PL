---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: ddccdb907dac89466a81be62e104202a3e59a672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550219"
---
# <span data-ttu-id="724a6-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="724a6-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="724a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="724a6-102">SYNOPSIS</span></span>
<span data-ttu-id="724a6-103">Zwraca opis określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="724a6-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="724a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="724a6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="724a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="724a6-105">DESCRIPTION</span></span>
<span data-ttu-id="724a6-106">Polecenie cmdlet **Get-AzureRmServiceBusTopic** zwraca opis tematu dla określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="724a6-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="724a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="724a6-107">EXAMPLES</span></span>

### <span data-ttu-id="724a6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="724a6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="724a6-109">Zwraca opis określonego tematu dla danego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="724a6-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="724a6-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="724a6-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="724a6-111">Zwraca listę tematów dotyczących danego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="724a6-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="724a6-112">Domyślnie zostaną zwrócone tematy dotyczące programu 100, a w przypadku zwrócenia więcej niż 100 tematów należy użyć parametru-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="724a6-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="724a6-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="724a6-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="724a6-114">Zwraca listę pierwszych tematów programu 150 dla danego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="724a6-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="724a6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="724a6-115">PARAMETERS</span></span>

### <span data-ttu-id="724a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724a6-116">-DefaultProfile</span></span>
<span data-ttu-id="724a6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="724a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="724a6-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="724a6-118">-MaxCount</span></span>
<span data-ttu-id="724a6-119">Określ maksymalną liczbę tematów, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="724a6-119">Determine the maximum number of Topics to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724a6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="724a6-120">-Name</span></span>
<span data-ttu-id="724a6-121">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="724a6-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="724a6-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="724a6-122">-Namespace</span></span>
<span data-ttu-id="724a6-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="724a6-123">Namespace Name</span></span>

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

### <span data-ttu-id="724a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="724a6-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="724a6-125">The name of the resource group</span></span>

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

### <span data-ttu-id="724a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724a6-126">CommonParameters</span></span>
<span data-ttu-id="724a6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724a6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724a6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724a6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="724a6-129">INPUTS</span></span>

### <span data-ttu-id="724a6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="724a6-130">System.String</span></span>

## <span data-ttu-id="724a6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="724a6-131">OUTPUTS</span></span>

### <span data-ttu-id="724a6-132">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="724a6-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="724a6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="724a6-133">NOTES</span></span>

## <span data-ttu-id="724a6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="724a6-134">RELATED LINKS</span></span>
