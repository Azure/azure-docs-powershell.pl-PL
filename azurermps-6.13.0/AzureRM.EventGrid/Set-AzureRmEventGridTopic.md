---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546623"
---
# <span data-ttu-id="3d8d8-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3d8d8-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="3d8d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8d8-103">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d8d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d8d8-104">SYNTAX</span></span>

### <span data-ttu-id="3d8d8-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3d8d8-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8d8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d8d8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8d8-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d8d8-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d8d8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3d8d8-108">DESCRIPTION</span></span>
<span data-ttu-id="3d8d8-109">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="3d8d8-110">Za pomocą tej funkcji można zastępować znaczniki tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="3d8d8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d8d8-111">EXAMPLES</span></span>

### <span data-ttu-id="3d8d8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d8d8-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="3d8d8-113">Ustawia właściwości tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów, \` \` Aby zamienić Tagi na określone znaczniki "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="3d8d8-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="3d8d8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d8d8-114">PARAMETERS</span></span>

### <span data-ttu-id="3d8d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8d8-115">-DefaultProfile</span></span>
<span data-ttu-id="3d8d8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3d8d8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d8d8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d8d8-117">-InputObject</span></span>
<span data-ttu-id="3d8d8-118">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="3d8d8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d8d8-119">-Name</span></span>
<span data-ttu-id="3d8d8-120">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="3d8d8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8d8-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d8d8-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d8d8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d8d8-123">-ResourceId</span></span>
<span data-ttu-id="3d8d8-124">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="3d8d8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d8d8-125">-Tag</span></span>
<span data-ttu-id="3d8d8-126">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-126">Hashtables which represents resource Tag.</span></span>

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8d8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d8d8-127">-Confirm</span></span>
<span data-ttu-id="3d8d8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8d8-129">-WhatIf</span></span>
<span data-ttu-id="3d8d8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8d8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8d8-132">CommonParameters</span></span>
<span data-ttu-id="3d8d8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8d8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d8d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8d8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d8d8-135">INPUTS</span></span>

### <span data-ttu-id="3d8d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3d8d8-136">System.String</span></span>

### <span data-ttu-id="3d8d8-137">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3d8d8-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="3d8d8-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d8d8-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3d8d8-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d8d8-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d8d8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d8d8-140">OUTPUTS</span></span>

### <span data-ttu-id="3d8d8-141">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3d8d8-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="3d8d8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d8d8-142">NOTES</span></span>

## <span data-ttu-id="3d8d8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d8d8-143">RELATED LINKS</span></span>
