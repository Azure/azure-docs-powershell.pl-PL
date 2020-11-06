---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aa9ef35ec0571628eb209163e91c9415706b57a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544344"
---
# <span data-ttu-id="40ec8-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="40ec8-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="40ec8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="40ec8-103">Usuwa temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40ec8-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ec8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40ec8-104">SYNTAX</span></span>

### <span data-ttu-id="40ec8-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="40ec8-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ec8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ec8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ec8-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ec8-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ec8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="40ec8-108">DESCRIPTION</span></span>
<span data-ttu-id="40ec8-109">Usuwa temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40ec8-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="40ec8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40ec8-110">EXAMPLES</span></span>

### <span data-ttu-id="40ec8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40ec8-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="40ec8-112">Usuwa temat \` Temat1 w siatce zdarzeń \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="40ec8-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="40ec8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="40ec8-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="40ec8-114">Usuwa temat \` Temat1 w siatce zdarzeń \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="40ec8-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="40ec8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40ec8-115">PARAMETERS</span></span>

### <span data-ttu-id="40ec8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ec8-116">-DefaultProfile</span></span>
<span data-ttu-id="40ec8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="40ec8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40ec8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="40ec8-118">-InputObject</span></span>
<span data-ttu-id="40ec8-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="40ec8-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40ec8-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40ec8-120">-Name</span></span>
<span data-ttu-id="40ec8-121">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="40ec8-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="40ec8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40ec8-122">-PassThru</span></span>
<span data-ttu-id="40ec8-123">Zwraca stan operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="40ec8-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="40ec8-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="40ec8-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ec8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ec8-125">-ResourceGroupName</span></span>
<span data-ttu-id="40ec8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40ec8-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="40ec8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40ec8-127">-ResourceId</span></span>
<span data-ttu-id="40ec8-128">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="40ec8-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ec8-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40ec8-129">-Confirm</span></span>
<span data-ttu-id="40ec8-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ec8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ec8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ec8-131">-WhatIf</span></span>
<span data-ttu-id="40ec8-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ec8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ec8-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40ec8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ec8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ec8-134">CommonParameters</span></span>
<span data-ttu-id="40ec8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ec8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ec8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ec8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ec8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40ec8-137">INPUTS</span></span>

### <span data-ttu-id="40ec8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="40ec8-138">System.String</span></span>
<span data-ttu-id="40ec8-139">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="40ec8-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="40ec8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40ec8-140">OUTPUTS</span></span>

### <span data-ttu-id="40ec8-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="40ec8-141">System.Object</span></span>

## <span data-ttu-id="40ec8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40ec8-142">NOTES</span></span>

## <span data-ttu-id="40ec8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40ec8-143">RELATED LINKS</span></span>

