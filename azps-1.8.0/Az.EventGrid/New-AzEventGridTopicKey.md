---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 8532e8411f474f769a4e9686ef89bf499f4f0272
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709831"
---
# <span data-ttu-id="6d225-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="6d225-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="6d225-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d225-102">SYNOPSIS</span></span>
<span data-ttu-id="6d225-103">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6d225-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6d225-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d225-104">SYNTAX</span></span>

### <span data-ttu-id="6d225-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d225-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d225-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d225-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d225-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d225-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d225-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6d225-108">DESCRIPTION</span></span>
<span data-ttu-id="6d225-109">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6d225-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6d225-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d225-110">EXAMPLES</span></span>

### <span data-ttu-id="6d225-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d225-111">Example 1</span></span>
```
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="6d225-112">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="6d225-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6d225-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6d225-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="6d225-114">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="6d225-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6d225-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d225-115">PARAMETERS</span></span>

### <span data-ttu-id="6d225-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d225-116">-DefaultProfile</span></span>
<span data-ttu-id="6d225-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d225-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d225-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6d225-118">-InputObject</span></span>
<span data-ttu-id="6d225-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6d225-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6d225-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="6d225-120">-KeyName</span></span>
<span data-ttu-id="6d225-121">Nazwa klucza, który należy ponownie wygenerować</span><span class="sxs-lookup"><span data-stu-id="6d225-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d225-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d225-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d225-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d225-123">Resource group name.</span></span>

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

### <span data-ttu-id="6d225-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d225-124">-ResourceId</span></span>
<span data-ttu-id="6d225-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6d225-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="6d225-126">-Tematname</span><span class="sxs-lookup"><span data-stu-id="6d225-126">-TopicName</span></span>
<span data-ttu-id="6d225-127">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="6d225-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d225-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d225-128">-Confirm</span></span>
<span data-ttu-id="6d225-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d225-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d225-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d225-130">-WhatIf</span></span>
<span data-ttu-id="6d225-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d225-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d225-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d225-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d225-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d225-133">CommonParameters</span></span>
<span data-ttu-id="6d225-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d225-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d225-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d225-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d225-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d225-136">INPUTS</span></span>

### <span data-ttu-id="6d225-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6d225-137">System.String</span></span>

### <span data-ttu-id="6d225-138">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="6d225-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="6d225-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d225-139">OUTPUTS</span></span>

### <span data-ttu-id="6d225-140">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6d225-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="6d225-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d225-141">NOTES</span></span>

## <span data-ttu-id="6d225-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d225-142">RELATED LINKS</span></span>
