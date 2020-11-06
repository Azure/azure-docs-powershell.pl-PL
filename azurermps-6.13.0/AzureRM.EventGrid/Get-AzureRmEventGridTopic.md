---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 2d18e923e14caf4c0048575465e9f52fb14596f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526193"
---
# <span data-ttu-id="548f1-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="548f1-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="548f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="548f1-102">SYNOPSIS</span></span>
<span data-ttu-id="548f1-103">Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="548f1-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="548f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="548f1-104">SYNTAX</span></span>

### <span data-ttu-id="548f1-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="548f1-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="548f1-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="548f1-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="548f1-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="548f1-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="548f1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="548f1-108">DESCRIPTION</span></span>
<span data-ttu-id="548f1-109">Polecenie cmdlet Get-AzureRmEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="548f1-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="548f1-110">W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="548f1-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="548f1-111">Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów.</span><span class="sxs-lookup"><span data-stu-id="548f1-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="548f1-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="548f1-112">EXAMPLES</span></span>

### <span data-ttu-id="548f1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="548f1-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="548f1-114">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="548f1-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="548f1-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="548f1-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="548f1-116">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="548f1-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="548f1-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="548f1-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="548f1-118">Lista wszystkich tematów dotyczących siatki zdarzeń w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="548f1-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="548f1-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="548f1-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="548f1-120">Lista wszystkich tematów siatki zdarzeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="548f1-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="548f1-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="548f1-121">PARAMETERS</span></span>

### <span data-ttu-id="548f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548f1-122">-DefaultProfile</span></span>
<span data-ttu-id="548f1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="548f1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="548f1-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="548f1-124">-Name</span></span>
<span data-ttu-id="548f1-125">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="548f1-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="548f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="548f1-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="548f1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="548f1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="548f1-128">-ResourceId</span></span>
<span data-ttu-id="548f1-129">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="548f1-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="548f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548f1-130">CommonParameters</span></span>
<span data-ttu-id="548f1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548f1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548f1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548f1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="548f1-133">INPUTS</span></span>

### <span data-ttu-id="548f1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="548f1-134">System.String</span></span>

## <span data-ttu-id="548f1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="548f1-135">OUTPUTS</span></span>

### <span data-ttu-id="548f1-136">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="548f1-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="548f1-137">Microsoft. Azure. Commands. EventGrid. models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="548f1-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="548f1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="548f1-138">NOTES</span></span>

## <span data-ttu-id="548f1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="548f1-139">RELATED LINKS</span></span>
