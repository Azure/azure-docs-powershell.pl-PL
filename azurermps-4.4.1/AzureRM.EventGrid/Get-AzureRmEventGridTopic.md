---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551023"
---
# <span data-ttu-id="c4c1c-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c4c1c-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="c4c1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c1c-103">Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4c1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4c1c-104">SYNTAX</span></span>

### <span data-ttu-id="c4c1c-105">ResourceGroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4c1c-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4c1c-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c1c-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4c1c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c1c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4c1c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c4c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c4c1c-109">Polecenie cmdlet Get-AzureRmEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="c4c1c-110">W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="c4c1c-111">Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="c4c1c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4c1c-112">EXAMPLES</span></span>

### <span data-ttu-id="c4c1c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4c1c-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="c4c1c-114">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="c4c1c-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c4c1c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c4c1c-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="c4c1c-116">Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="c4c1c-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c4c1c-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c4c1c-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="c4c1c-118">Lista wszystkich tematów dotyczących siatki zdarzeń w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="c4c1c-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c4c1c-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c4c1c-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="c4c1c-120">Lista wszystkich tematów siatki zdarzeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="c4c1c-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4c1c-121">PARAMETERS</span></span>

### <span data-ttu-id="c4c1c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4c1c-122">-Name</span></span>
<span data-ttu-id="c4c1c-123">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-123">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c4c1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4c1c-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4c1c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4c1c-126">-ResourceId</span></span>
<span data-ttu-id="c4c1c-127">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-127">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="c4c1c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c1c-128">-DefaultProfile</span></span>
<span data-ttu-id="c4c1c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4c1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c1c-130">CommonParameters</span></span>
<span data-ttu-id="c4c1c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c1c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c1c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c1c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4c1c-133">INPUTS</span></span>

### <span data-ttu-id="c4c1c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c4c1c-134">System.String</span></span>
<span data-ttu-id="c4c1c-135">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c4c1c-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c4c1c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4c1c-136">OUTPUTS</span></span>

### <span data-ttu-id="c4c1c-137">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c4c1c-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="c4c1c-138">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventGrid. MODELES. PSTopicListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c4c1c-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c4c1c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4c1c-139">NOTES</span></span>

## <span data-ttu-id="c4c1c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4c1c-140">RELATED LINKS</span></span>

