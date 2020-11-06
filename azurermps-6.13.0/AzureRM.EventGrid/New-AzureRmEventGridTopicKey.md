---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: badbb8c392e053b1f8d994164183bd593843629e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546631"
---
# <span data-ttu-id="1e43b-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="1e43b-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="1e43b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e43b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e43b-103">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e43b-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e43b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e43b-104">SYNTAX</span></span>

### <span data-ttu-id="1e43b-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e43b-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e43b-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e43b-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e43b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e43b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e43b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e43b-108">DESCRIPTION</span></span>
<span data-ttu-id="1e43b-109">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e43b-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="1e43b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e43b-110">EXAMPLES</span></span>

### <span data-ttu-id="1e43b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e43b-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="1e43b-112">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="1e43b-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1e43b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1e43b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="1e43b-114">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="1e43b-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1e43b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e43b-115">PARAMETERS</span></span>

### <span data-ttu-id="1e43b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e43b-116">-DefaultProfile</span></span>
<span data-ttu-id="1e43b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1e43b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e43b-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e43b-118">-InputObject</span></span>
<span data-ttu-id="1e43b-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1e43b-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="1e43b-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="1e43b-120">-KeyName</span></span>
<span data-ttu-id="1e43b-121">Nazwa klucza, który należy ponownie wygenerować</span><span class="sxs-lookup"><span data-stu-id="1e43b-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="1e43b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e43b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e43b-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e43b-123">Resource group name.</span></span>

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

### <span data-ttu-id="1e43b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e43b-124">-ResourceId</span></span>
<span data-ttu-id="1e43b-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1e43b-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="1e43b-126">-Tematname</span><span class="sxs-lookup"><span data-stu-id="1e43b-126">-TopicName</span></span>
<span data-ttu-id="1e43b-127">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="1e43b-127">The name of the topic.</span></span>

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

### <span data-ttu-id="1e43b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e43b-128">-Confirm</span></span>
<span data-ttu-id="1e43b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e43b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e43b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e43b-130">-WhatIf</span></span>
<span data-ttu-id="1e43b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e43b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e43b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e43b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e43b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e43b-133">CommonParameters</span></span>
<span data-ttu-id="1e43b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e43b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e43b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e43b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e43b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e43b-136">INPUTS</span></span>

### <span data-ttu-id="1e43b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1e43b-137">System.String</span></span>

### <span data-ttu-id="1e43b-138">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="1e43b-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="1e43b-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1e43b-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1e43b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e43b-140">OUTPUTS</span></span>

### <span data-ttu-id="1e43b-141">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1e43b-141">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="1e43b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e43b-142">NOTES</span></span>

## <span data-ttu-id="1e43b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e43b-143">RELATED LINKS</span></span>
