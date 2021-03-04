---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: 2a11ab0ec68ee01864f1255953121b91f1b27ebf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957121"
---
# <span data-ttu-id="5b246-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5b246-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="5b246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b246-102">SYNOPSIS</span></span>
<span data-ttu-id="5b246-103">Tworzy nową grupę klientów dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5b246-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5b246-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b246-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b246-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b246-105">DESCRIPTION</span></span>
<span data-ttu-id="5b246-106">Tworzy nową grupę klientów dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5b246-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5b246-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b246-107">EXAMPLES</span></span>

### <span data-ttu-id="5b246-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b246-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="5b246-109">Tworzy grupę konsumencką \` MyConsumerGroupName w centrum zdarzeń \` MyEventHubName w zakresie nazw MyNamespaceName z grupą zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="5b246-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5b246-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b246-110">PARAMETERS</span></span>

### <span data-ttu-id="5b246-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b246-111">-DefaultProfile</span></span>
<span data-ttu-id="5b246-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b246-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b246-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5b246-113">-EventHub</span></span>
<span data-ttu-id="5b246-114">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="5b246-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b246-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5b246-115">-Name</span></span>
<span data-ttu-id="5b246-116">Nazwa grupy konsumenckiej</span><span class="sxs-lookup"><span data-stu-id="5b246-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b246-117">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="5b246-117">-Namespace</span></span>
<span data-ttu-id="5b246-118">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5b246-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b246-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b246-119">-ResourceGroupName</span></span>
<span data-ttu-id="5b246-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5b246-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b246-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="5b246-121">-UserMetadata</span></span>
<span data-ttu-id="5b246-122">Metadane użytkownika dla grupy ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5b246-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b246-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b246-123">-Confirm</span></span>
<span data-ttu-id="5b246-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b246-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b246-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b246-125">-WhatIf</span></span>
<span data-ttu-id="5b246-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b246-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b246-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5b246-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b246-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b246-128">CommonParameters</span></span>
<span data-ttu-id="5b246-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b246-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b246-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b246-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b246-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b246-131">INPUTS</span></span>

### <span data-ttu-id="5b246-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5b246-132">System.String</span></span>

## <span data-ttu-id="5b246-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b246-133">OUTPUTS</span></span>

### <span data-ttu-id="5b246-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5b246-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="5b246-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b246-135">NOTES</span></span>

## <span data-ttu-id="5b246-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b246-136">RELATED LINKS</span></span>
