---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194426"
---
# <span data-ttu-id="59a6e-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="59a6e-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="59a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="59a6e-103">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń na temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="59a6e-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="59a6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59a6e-104">SYNTAX</span></span>

### <span data-ttu-id="59a6e-105">TopicNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="59a6e-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59a6e-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a6e-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a6e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a6e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59a6e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="59a6e-108">DESCRIPTION</span></span>
<span data-ttu-id="59a6e-109">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń na temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="59a6e-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="59a6e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59a6e-110">EXAMPLES</span></span>

### <span data-ttu-id="59a6e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59a6e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="59a6e-112">Pobiera klucze dostępu udostępnionego tematu Siatka zdarzeń \` , \` temat1, w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="59a6e-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="59a6e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59a6e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="59a6e-114">Pobiera klucze dostępu udostępnionego tematu Siatka zdarzeń \` , \` temat1, w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="59a6e-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="59a6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59a6e-115">PARAMETERS</span></span>

### <span data-ttu-id="59a6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a6e-116">-DefaultProfile</span></span>
<span data-ttu-id="59a6e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="59a6e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a6e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59a6e-118">-InputObject</span></span>
<span data-ttu-id="59a6e-119">Obiekt tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="59a6e-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="59a6e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59a6e-120">-Name</span></span>
<span data-ttu-id="59a6e-121">Nazwa tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="59a6e-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="59a6e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a6e-122">-ResourceGroupName</span></span>
<span data-ttu-id="59a6e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59a6e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="59a6e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59a6e-124">-ResourceId</span></span>
<span data-ttu-id="59a6e-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="59a6e-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="59a6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a6e-126">CommonParameters</span></span>
<span data-ttu-id="59a6e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a6e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59a6e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a6e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59a6e-129">INPUTS</span></span>

### <span data-ttu-id="59a6e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="59a6e-130">System.String</span></span>

### <span data-ttu-id="59a6e-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="59a6e-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="59a6e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59a6e-132">OUTPUTS</span></span>

### <span data-ttu-id="59a6e-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="59a6e-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="59a6e-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59a6e-134">NOTES</span></span>

## <span data-ttu-id="59a6e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59a6e-135">RELATED LINKS</span></span>
