---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553919"
---
# <span data-ttu-id="21062-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="21062-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="21062-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21062-102">SYNOPSIS</span></span>
<span data-ttu-id="21062-103">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21062-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21062-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21062-104">SYNTAX</span></span>

### <span data-ttu-id="21062-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21062-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21062-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21062-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21062-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="21062-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21062-108">Opis</span><span class="sxs-lookup"><span data-stu-id="21062-108">DESCRIPTION</span></span>
<span data-ttu-id="21062-109">Generuje ponownie klucz dostępu współużytkowanego tematu siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21062-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="21062-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21062-110">EXAMPLES</span></span>

### <span data-ttu-id="21062-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21062-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="21062-112">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="21062-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="21062-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="21062-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="21062-114">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ Temat1 temat siatki \` zdarzeń \` w MyResourceGroupName grup \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="21062-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="21062-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21062-115">PARAMETERS</span></span>

### <span data-ttu-id="21062-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21062-116">-InputObject</span></span>
<span data-ttu-id="21062-117">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="21062-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="21062-118">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="21062-118">-KeyName</span></span>
<span data-ttu-id="21062-119">Nazwa klucza, który należy ponownie wygenerować</span><span class="sxs-lookup"><span data-stu-id="21062-119">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="21062-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21062-120">-ResourceGroupName</span></span>
<span data-ttu-id="21062-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21062-121">Resource group name.</span></span>

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

### <span data-ttu-id="21062-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21062-122">-ResourceId</span></span>
<span data-ttu-id="21062-123">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="21062-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="21062-124">-Tematname</span><span class="sxs-lookup"><span data-stu-id="21062-124">-TopicName</span></span>
<span data-ttu-id="21062-125">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="21062-125">The name of the topic.</span></span>

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

### <span data-ttu-id="21062-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21062-126">-Confirm</span></span>
<span data-ttu-id="21062-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21062-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21062-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21062-128">-WhatIf</span></span>
<span data-ttu-id="21062-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21062-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21062-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21062-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21062-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21062-131">-DefaultProfile</span></span>
<span data-ttu-id="21062-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21062-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21062-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21062-133">CommonParameters</span></span>
<span data-ttu-id="21062-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21062-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21062-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21062-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21062-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21062-136">INPUTS</span></span>

### <span data-ttu-id="21062-137">System. String</span><span class="sxs-lookup"><span data-stu-id="21062-137">System.String</span></span>

## <span data-ttu-id="21062-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21062-138">OUTPUTS</span></span>

### <span data-ttu-id="21062-139">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="21062-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="21062-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21062-140">NOTES</span></span>

## <span data-ttu-id="21062-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21062-141">RELATED LINKS</span></span>

