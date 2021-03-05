---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 92a70d16f8cd1db2c37c1247c994a3c406df5a54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991313"
---
# <span data-ttu-id="b3bc7-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="b3bc7-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="b3bc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bc7-103">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń na temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="b3bc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3bc7-104">SYNTAX</span></span>

### <span data-ttu-id="b3bc7-105">TopicNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b3bc7-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3bc7-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3bc7-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3bc7-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3bc7-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3bc7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3bc7-108">DESCRIPTION</span></span>
<span data-ttu-id="b3bc7-109">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń na temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="b3bc7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3bc7-110">EXAMPLES</span></span>

### <span data-ttu-id="b3bc7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3bc7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="b3bc7-112">Pobiera klucze dostępu udostępnionego tematu Siatka zdarzeń \` , \` temat1, w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b3bc7-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b3bc7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b3bc7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="b3bc7-114">Pobiera klucze dostępu udostępnionego tematu Siatka zdarzeń \` , \` temat1, w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b3bc7-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b3bc7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3bc7-115">PARAMETERS</span></span>

### <span data-ttu-id="b3bc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bc7-116">-DefaultProfile</span></span>
<span data-ttu-id="b3bc7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b3bc7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3bc7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3bc7-118">-InputObject</span></span>
<span data-ttu-id="b3bc7-119">Obiekt tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="b3bc7-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b3bc7-120">-Name</span></span>
<span data-ttu-id="b3bc7-121">Nazwa tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="b3bc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3bc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3bc7-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3bc7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3bc7-124">-ResourceId</span></span>
<span data-ttu-id="b3bc7-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="b3bc7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bc7-126">CommonParameters</span></span>
<span data-ttu-id="b3bc7-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bc7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bc7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3bc7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bc7-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3bc7-129">INPUTS</span></span>

### <span data-ttu-id="b3bc7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b3bc7-130">System.String</span></span>

### <span data-ttu-id="b3bc7-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="b3bc7-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="b3bc7-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3bc7-132">OUTPUTS</span></span>

### <span data-ttu-id="b3bc7-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b3bc7-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="b3bc7-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3bc7-134">NOTES</span></span>

## <span data-ttu-id="b3bc7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3bc7-135">RELATED LINKS</span></span>
