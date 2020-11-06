---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 3600d7523e95b937f20d9d0b97d677c5cf02ca0f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554403"
---
# <span data-ttu-id="75829-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="75829-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="75829-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75829-102">SYNOPSIS</span></span>
<span data-ttu-id="75829-103">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75829-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75829-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75829-104">SYNTAX</span></span>

### <span data-ttu-id="75829-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75829-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75829-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75829-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75829-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="75829-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75829-108">Opis</span><span class="sxs-lookup"><span data-stu-id="75829-108">DESCRIPTION</span></span>
<span data-ttu-id="75829-109">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75829-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="75829-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75829-110">EXAMPLES</span></span>

### <span data-ttu-id="75829-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="75829-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="75829-112">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="75829-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="75829-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="75829-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="75829-114">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="75829-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="75829-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75829-115">PARAMETERS</span></span>

### <span data-ttu-id="75829-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75829-116">-DefaultProfile</span></span>
<span data-ttu-id="75829-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75829-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75829-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75829-118">-InputObject</span></span>
<span data-ttu-id="75829-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="75829-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="75829-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="75829-120">-KeyName</span></span>
<span data-ttu-id="75829-121">Nazwa klucza, który należy ponownie wygenerować</span><span class="sxs-lookup"><span data-stu-id="75829-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75829-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75829-122">-ResourceGroupName</span></span>
<span data-ttu-id="75829-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75829-123">Resource group name.</span></span>

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

### <span data-ttu-id="75829-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75829-124">-ResourceId</span></span>
<span data-ttu-id="75829-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="75829-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75829-126">-Tematname</span><span class="sxs-lookup"><span data-stu-id="75829-126">-TopicName</span></span>
<span data-ttu-id="75829-127">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="75829-127">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75829-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75829-128">-Confirm</span></span>
<span data-ttu-id="75829-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75829-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75829-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75829-130">-WhatIf</span></span>
<span data-ttu-id="75829-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75829-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75829-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75829-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75829-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75829-133">CommonParameters</span></span>
<span data-ttu-id="75829-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75829-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75829-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75829-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75829-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75829-136">INPUTS</span></span>

### <span data-ttu-id="75829-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75829-137">System.String</span></span>

## <span data-ttu-id="75829-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75829-138">OUTPUTS</span></span>

### <span data-ttu-id="75829-139">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="75829-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="75829-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75829-140">NOTES</span></span>

## <span data-ttu-id="75829-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75829-141">RELATED LINKS</span></span>

