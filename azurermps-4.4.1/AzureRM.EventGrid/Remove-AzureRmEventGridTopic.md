---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aecbc105a87cc058567cb0ff35f0bb0e8cc84c7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719330"
---
# <span data-ttu-id="c840d-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c840d-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="c840d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c840d-102">SYNOPSIS</span></span>
<span data-ttu-id="c840d-103">Usuwa temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c840d-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c840d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c840d-104">SYNTAX</span></span>

### <span data-ttu-id="c840d-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c840d-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c840d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c840d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c840d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c840d-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c840d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c840d-108">DESCRIPTION</span></span>
<span data-ttu-id="c840d-109">Usuwa temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c840d-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="c840d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c840d-110">EXAMPLES</span></span>

### <span data-ttu-id="c840d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c840d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="c840d-112">Usuwa temat \` Temat1 w siatce zdarzeń \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="c840d-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c840d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c840d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="c840d-114">Usuwa temat \` Temat1 w siatce zdarzeń \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="c840d-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c840d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c840d-115">PARAMETERS</span></span>

### <span data-ttu-id="c840d-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c840d-116">-InputObject</span></span>
<span data-ttu-id="c840d-117">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c840d-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c840d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c840d-118">-Name</span></span>
<span data-ttu-id="c840d-119">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c840d-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c840d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c840d-120">-PassThru</span></span>
<span data-ttu-id="c840d-121">Zwraca stan operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="c840d-121">Returns the status of the Remove operation.</span></span> <span data-ttu-id="c840d-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c840d-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c840d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c840d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c840d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c840d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="c840d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c840d-125">-ResourceId</span></span>
<span data-ttu-id="c840d-126">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c840d-126">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c840d-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c840d-127">-Confirm</span></span>
<span data-ttu-id="c840d-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c840d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c840d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c840d-129">-WhatIf</span></span>
<span data-ttu-id="c840d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c840d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c840d-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c840d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c840d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c840d-132">-DefaultProfile</span></span>
<span data-ttu-id="c840d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c840d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c840d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c840d-134">CommonParameters</span></span>
<span data-ttu-id="c840d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c840d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c840d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c840d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c840d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c840d-137">INPUTS</span></span>

### <span data-ttu-id="c840d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c840d-138">System.String</span></span>
<span data-ttu-id="c840d-139">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c840d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c840d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c840d-140">OUTPUTS</span></span>

### <span data-ttu-id="c840d-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="c840d-141">System.Object</span></span>

## <span data-ttu-id="c840d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c840d-142">NOTES</span></span>

## <span data-ttu-id="c840d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c840d-143">RELATED LINKS</span></span>

