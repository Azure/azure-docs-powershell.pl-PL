---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93719685"
---
# <span data-ttu-id="36a5c-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="36a5c-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="36a5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="36a5c-103">Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36a5c-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36a5c-104">SYNTAX</span></span>

### <span data-ttu-id="36a5c-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36a5c-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36a5c-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36a5c-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36a5c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="36a5c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36a5c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="36a5c-108">DESCRIPTION</span></span>
<span data-ttu-id="36a5c-109">Polecenie cmdlet Get-AzureRmEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36a5c-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="36a5c-110">W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="36a5c-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="36a5c-111">Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów.</span><span class="sxs-lookup"><span data-stu-id="36a5c-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="36a5c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36a5c-112">EXAMPLES</span></span>

### <span data-ttu-id="36a5c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36a5c-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="36a5c-114">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="36a5c-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="36a5c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="36a5c-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="36a5c-116">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="36a5c-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="36a5c-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="36a5c-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="36a5c-118">Lista wszystkich tematów dotyczących siatki zdarzeń w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="36a5c-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="36a5c-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="36a5c-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="36a5c-120">Lista wszystkich tematów siatki zdarzeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="36a5c-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="36a5c-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36a5c-121">PARAMETERS</span></span>

### <span data-ttu-id="36a5c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a5c-122">-DefaultProfile</span></span>
<span data-ttu-id="36a5c-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="36a5c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36a5c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36a5c-124">-Name</span></span>
<span data-ttu-id="36a5c-125">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="36a5c-125">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a5c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a5c-126">-ResourceGroupName</span></span>
<span data-ttu-id="36a5c-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36a5c-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a5c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36a5c-128">-ResourceId</span></span>
<span data-ttu-id="36a5c-129">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="36a5c-129">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a5c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a5c-130">CommonParameters</span></span>
<span data-ttu-id="36a5c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a5c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a5c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a5c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a5c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36a5c-133">INPUTS</span></span>

### <span data-ttu-id="36a5c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="36a5c-134">System.String</span></span>
<span data-ttu-id="36a5c-135">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="36a5c-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="36a5c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36a5c-136">OUTPUTS</span></span>

### <span data-ttu-id="36a5c-137">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="36a5c-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="36a5c-138">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventGrid. MODELES. PSTopicListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="36a5c-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="36a5c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36a5c-139">NOTES</span></span>

## <span data-ttu-id="36a5c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36a5c-140">RELATED LINKS</span></span>

