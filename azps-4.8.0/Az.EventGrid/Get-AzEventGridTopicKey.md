---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064109"
---
# <span data-ttu-id="69b72-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="69b72-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="69b72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69b72-102">SYNOPSIS</span></span>
<span data-ttu-id="69b72-103">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w temacie dotyczącym siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="69b72-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="69b72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69b72-104">SYNTAX</span></span>

### <span data-ttu-id="69b72-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69b72-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69b72-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69b72-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69b72-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="69b72-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69b72-108">Opis</span><span class="sxs-lookup"><span data-stu-id="69b72-108">DESCRIPTION</span></span>
<span data-ttu-id="69b72-109">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w temacie dotyczącym siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="69b72-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="69b72-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69b72-110">EXAMPLES</span></span>

### <span data-ttu-id="69b72-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69b72-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="69b72-112">Pobiera klucze dostępu współużytkowanego tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="69b72-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="69b72-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="69b72-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="69b72-114">Pobiera klucze dostępu współużytkowanego tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="69b72-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="69b72-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69b72-115">PARAMETERS</span></span>

### <span data-ttu-id="69b72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b72-116">-DefaultProfile</span></span>
<span data-ttu-id="69b72-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="69b72-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69b72-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69b72-118">-InputObject</span></span>
<span data-ttu-id="69b72-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="69b72-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69b72-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69b72-120">-Name</span></span>
<span data-ttu-id="69b72-121">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="69b72-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="69b72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b72-122">-ResourceGroupName</span></span>
<span data-ttu-id="69b72-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69b72-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="69b72-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69b72-124">-ResourceId</span></span>
<span data-ttu-id="69b72-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="69b72-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="69b72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b72-126">CommonParameters</span></span>
<span data-ttu-id="69b72-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b72-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69b72-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b72-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69b72-129">INPUTS</span></span>

### <span data-ttu-id="69b72-130">System. String</span><span class="sxs-lookup"><span data-stu-id="69b72-130">System.String</span></span>

### <span data-ttu-id="69b72-131">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="69b72-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="69b72-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69b72-132">OUTPUTS</span></span>

### <span data-ttu-id="69b72-133">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="69b72-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="69b72-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69b72-134">NOTES</span></span>

## <span data-ttu-id="69b72-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69b72-135">RELATED LINKS</span></span>
