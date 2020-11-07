---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709844"
---
# <span data-ttu-id="b421d-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="b421d-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="b421d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b421d-102">SYNOPSIS</span></span>
<span data-ttu-id="b421d-103">Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b421d-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="b421d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b421d-104">SYNTAX</span></span>

### <span data-ttu-id="b421d-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b421d-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b421d-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b421d-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b421d-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b421d-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b421d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b421d-108">DESCRIPTION</span></span>
<span data-ttu-id="b421d-109">Polecenie cmdlet Get-AzEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b421d-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="b421d-110">W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b421d-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="b421d-111">Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów.</span><span class="sxs-lookup"><span data-stu-id="b421d-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="b421d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b421d-112">EXAMPLES</span></span>

### <span data-ttu-id="b421d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b421d-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="b421d-114">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b421d-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b421d-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b421d-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="b421d-116">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b421d-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b421d-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b421d-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="b421d-118">Lista wszystkich tematów dotyczących siatki zdarzeń w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="b421d-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b421d-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b421d-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="b421d-120">Lista wszystkich tematów siatki zdarzeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b421d-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="b421d-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b421d-121">PARAMETERS</span></span>

### <span data-ttu-id="b421d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b421d-122">-DefaultProfile</span></span>
<span data-ttu-id="b421d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b421d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b421d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b421d-124">-Name</span></span>
<span data-ttu-id="b421d-125">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b421d-125">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b421d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b421d-126">-ResourceGroupName</span></span>
<span data-ttu-id="b421d-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b421d-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b421d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b421d-128">-ResourceId</span></span>
<span data-ttu-id="b421d-129">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b421d-129">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b421d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b421d-130">CommonParameters</span></span>
<span data-ttu-id="b421d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b421d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b421d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b421d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b421d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b421d-133">INPUTS</span></span>

### <span data-ttu-id="b421d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b421d-134">System.String</span></span>

## <span data-ttu-id="b421d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b421d-135">OUTPUTS</span></span>

### <span data-ttu-id="b421d-136">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="b421d-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="b421d-137">Microsoft. Azure. Commands. EventGrid. models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="b421d-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="b421d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b421d-138">NOTES</span></span>

## <span data-ttu-id="b421d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b421d-139">RELATED LINKS</span></span>
