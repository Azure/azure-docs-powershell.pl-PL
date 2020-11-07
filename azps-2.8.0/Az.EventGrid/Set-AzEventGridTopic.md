---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: f27533a36314ae2b31cd0055e8cc17027c95016a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705473"
---
# <span data-ttu-id="da774-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="da774-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="da774-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da774-102">SYNOPSIS</span></span>
<span data-ttu-id="da774-103">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="da774-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="da774-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da774-104">SYNTAX</span></span>

### <span data-ttu-id="da774-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da774-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da774-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="da774-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da774-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da774-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da774-108">Opis</span><span class="sxs-lookup"><span data-stu-id="da774-108">DESCRIPTION</span></span>
<span data-ttu-id="da774-109">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="da774-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="da774-110">Za pomocą tej funkcji można zastępować znaczniki tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="da774-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="da774-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da774-111">EXAMPLES</span></span>

### <span data-ttu-id="da774-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da774-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="da774-113">Ustawia właściwości tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów, \` \` Aby zamienić Tagi na określone znaczniki "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="da774-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="da774-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da774-114">PARAMETERS</span></span>

### <span data-ttu-id="da774-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da774-115">-DefaultProfile</span></span>
<span data-ttu-id="da774-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="da774-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da774-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da774-117">-InputObject</span></span>
<span data-ttu-id="da774-118">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="da774-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="da774-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da774-119">-Name</span></span>
<span data-ttu-id="da774-120">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="da774-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="da774-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da774-121">-ResourceGroupName</span></span>
<span data-ttu-id="da774-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da774-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="da774-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da774-123">-ResourceId</span></span>
<span data-ttu-id="da774-124">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="da774-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="da774-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="da774-125">-Tag</span></span>
<span data-ttu-id="da774-126">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="da774-126">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="da774-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da774-127">-Confirm</span></span>
<span data-ttu-id="da774-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da774-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da774-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da774-129">-WhatIf</span></span>
<span data-ttu-id="da774-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da774-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da774-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da774-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da774-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da774-132">CommonParameters</span></span>
<span data-ttu-id="da774-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da774-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da774-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da774-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da774-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da774-135">INPUTS</span></span>

### <span data-ttu-id="da774-136">System. String</span><span class="sxs-lookup"><span data-stu-id="da774-136">System.String</span></span>

### <span data-ttu-id="da774-137">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="da774-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="da774-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da774-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da774-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da774-139">OUTPUTS</span></span>

### <span data-ttu-id="da774-140">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="da774-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="da774-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da774-141">NOTES</span></span>

## <span data-ttu-id="da774-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da774-142">RELATED LINKS</span></span>
