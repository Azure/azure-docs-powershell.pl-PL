---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 509f10432139ca0f2d9aaca216f22d998b7963a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553913"
---
# <span data-ttu-id="2aef4-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2aef4-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="2aef4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2aef4-102">SYNOPSIS</span></span>
<span data-ttu-id="2aef4-103">Ustawianie właściwości tematu siatki zdarzeń</span><span class="sxs-lookup"><span data-stu-id="2aef4-103">Set the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aef4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2aef4-104">SYNTAX</span></span>

### <span data-ttu-id="2aef4-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2aef4-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aef4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aef4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aef4-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aef4-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aef4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2aef4-108">DESCRIPTION</span></span>
<span data-ttu-id="2aef4-109">Ustawianie właściwości tematu siatki zdarzeń</span><span class="sxs-lookup"><span data-stu-id="2aef4-109">Set the properties of an Event Grid topic.</span></span> <span data-ttu-id="2aef4-110">Za pomocą tej funkcji można zastępować znaczniki tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2aef4-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="2aef4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2aef4-111">EXAMPLES</span></span>

### <span data-ttu-id="2aef4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2aef4-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="2aef4-113">Ustawia właściwości tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów, \` \` Aby zamienić Tagi na określone znaczniki "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="2aef4-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="2aef4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2aef4-114">PARAMETERS</span></span>

### <span data-ttu-id="2aef4-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2aef4-115">-InputObject</span></span>
<span data-ttu-id="2aef4-116">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="2aef4-116">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="2aef4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2aef4-117">-Name</span></span>
<span data-ttu-id="2aef4-118">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="2aef4-118">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2aef4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aef4-119">-ResourceGroupName</span></span>
<span data-ttu-id="2aef4-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2aef4-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="2aef4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aef4-121">-ResourceId</span></span>
<span data-ttu-id="2aef4-122">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="2aef4-122">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="2aef4-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="2aef4-123">-Tag</span></span>
<span data-ttu-id="2aef4-124">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="2aef4-124">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="2aef4-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2aef4-125">-Confirm</span></span>
<span data-ttu-id="2aef4-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aef4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aef4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aef4-127">-WhatIf</span></span>
<span data-ttu-id="2aef4-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aef4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aef4-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2aef4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aef4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aef4-130">-DefaultProfile</span></span>
<span data-ttu-id="2aef4-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2aef4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aef4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aef4-132">CommonParameters</span></span>
<span data-ttu-id="2aef4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aef4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aef4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aef4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aef4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aef4-135">INPUTS</span></span>

### <span data-ttu-id="2aef4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2aef4-136">System.String</span></span>
<span data-ttu-id="2aef4-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2aef4-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2aef4-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2aef4-138">OUTPUTS</span></span>

### <span data-ttu-id="2aef4-139">Microsoft. Azure. Management. EventGrid. models. temat</span><span class="sxs-lookup"><span data-stu-id="2aef4-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="2aef4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2aef4-140">NOTES</span></span>

## <span data-ttu-id="2aef4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aef4-141">RELATED LINKS</span></span>

