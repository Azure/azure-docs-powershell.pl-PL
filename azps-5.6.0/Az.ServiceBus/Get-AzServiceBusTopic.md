---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 9f8e7ee089972768053fd2873be22ed31dab206c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993364"
---
# <span data-ttu-id="da11d-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="da11d-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="da11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da11d-102">SYNOPSIS</span></span>
<span data-ttu-id="da11d-103">Zwraca opis określonego tematu "Service Bus" (Autobus usług).</span><span class="sxs-lookup"><span data-stu-id="da11d-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="da11d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da11d-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da11d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="da11d-105">DESCRIPTION</span></span>
<span data-ttu-id="da11d-106">Polecenie **cmdlet Get-AzServiceBusTopic** zwraca opis tematu dla określonej przestrzeni nazw typu bus usługi.</span><span class="sxs-lookup"><span data-stu-id="da11d-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="da11d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da11d-107">EXAMPLES</span></span>

### <span data-ttu-id="da11d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da11d-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

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

<span data-ttu-id="da11d-109">Zwraca opis określonego tematu dla danej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="da11d-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="da11d-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da11d-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="da11d-111">Zwraca listę tematów dla danej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="da11d-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="da11d-112">Domyślnie zostanie zwróconych 100 tematów, jeśli zostanie zwróconych więcej niż 100 tematów, użyj parametru -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="da11d-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="da11d-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="da11d-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="da11d-114">Zwraca listę pierwszych 150 tematów dla danej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="da11d-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="da11d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da11d-115">PARAMETERS</span></span>

### <span data-ttu-id="da11d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da11d-116">-DefaultProfile</span></span>
<span data-ttu-id="da11d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da11d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da11d-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="da11d-118">-MaxCount</span></span>
<span data-ttu-id="da11d-119">Określ maksymalną liczbę zwracanych tematów.</span><span class="sxs-lookup"><span data-stu-id="da11d-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="da11d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="da11d-120">-Name</span></span>
<span data-ttu-id="da11d-121">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="da11d-121">Topic Name</span></span>

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

### <span data-ttu-id="da11d-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="da11d-122">-Namespace</span></span>
<span data-ttu-id="da11d-123">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="da11d-123">Namespace Name</span></span>

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

### <span data-ttu-id="da11d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da11d-124">-ResourceGroupName</span></span>
<span data-ttu-id="da11d-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="da11d-125">The name of the resource group</span></span>

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

### <span data-ttu-id="da11d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da11d-126">CommonParameters</span></span>
<span data-ttu-id="da11d-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da11d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da11d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da11d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da11d-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da11d-129">INPUTS</span></span>

### <span data-ttu-id="da11d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="da11d-130">System.String</span></span>

## <span data-ttu-id="da11d-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da11d-131">OUTPUTS</span></span>

### <span data-ttu-id="da11d-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="da11d-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="da11d-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da11d-133">NOTES</span></span>

## <span data-ttu-id="da11d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da11d-134">RELATED LINKS</span></span>
