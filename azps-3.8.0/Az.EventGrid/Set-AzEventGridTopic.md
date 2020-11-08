---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: edccb9bf46a75c8a9f6fe0c577a87e13d11a2ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049899"
---
# <span data-ttu-id="c46cb-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c46cb-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="c46cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c46cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c46cb-103">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c46cb-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="c46cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c46cb-104">SYNTAX</span></span>

### <span data-ttu-id="c46cb-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c46cb-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46cb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46cb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46cb-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46cb-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c46cb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c46cb-108">DESCRIPTION</span></span>
<span data-ttu-id="c46cb-109">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c46cb-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="c46cb-110">Za pomocą tej funkcji można zastępować znaczniki tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c46cb-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="c46cb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c46cb-111">EXAMPLES</span></span>

### <span data-ttu-id="c46cb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c46cb-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="c46cb-113">Ustawia właściwości tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów, \` \` Aby zamienić Tagi na określone znaczniki "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="c46cb-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="c46cb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c46cb-114">PARAMETERS</span></span>

### <span data-ttu-id="c46cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46cb-115">-DefaultProfile</span></span>
<span data-ttu-id="c46cb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c46cb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c46cb-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c46cb-117">-InputObject</span></span>
<span data-ttu-id="c46cb-118">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c46cb-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c46cb-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c46cb-119">-Name</span></span>
<span data-ttu-id="c46cb-120">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c46cb-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c46cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="c46cb-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c46cb-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c46cb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c46cb-123">-ResourceId</span></span>
<span data-ttu-id="c46cb-124">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c46cb-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="c46cb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c46cb-125">-Tag</span></span>
<span data-ttu-id="c46cb-126">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="c46cb-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c46cb-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c46cb-127">-Confirm</span></span>
<span data-ttu-id="c46cb-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c46cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46cb-129">-WhatIf</span></span>
<span data-ttu-id="c46cb-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c46cb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c46cb-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c46cb-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46cb-132">CommonParameters</span></span>
<span data-ttu-id="c46cb-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c46cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46cb-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c46cb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46cb-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c46cb-135">INPUTS</span></span>

### <span data-ttu-id="c46cb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c46cb-136">System.String</span></span>

### <span data-ttu-id="c46cb-137">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c46cb-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c46cb-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c46cb-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c46cb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c46cb-139">OUTPUTS</span></span>

### <span data-ttu-id="c46cb-140">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c46cb-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c46cb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c46cb-141">NOTES</span></span>

## <span data-ttu-id="c46cb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c46cb-142">RELATED LINKS</span></span>
