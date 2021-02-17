---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180682"
---
# <span data-ttu-id="79893-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="79893-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="79893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79893-102">SYNOPSIS</span></span>
<span data-ttu-id="79893-103">Tworzy nową grupę klientów dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="79893-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="79893-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79893-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79893-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79893-105">DESCRIPTION</span></span>
<span data-ttu-id="79893-106">Tworzy nową grupę klientów dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="79893-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="79893-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79893-107">EXAMPLES</span></span>

### <span data-ttu-id="79893-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79893-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="79893-109">Tworzy grupę konsumencką \` MyConsumerGroupName w centrum zdarzeń \` MyEventHubName w zakresie nazw MyNamespaceName z grupą zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="79893-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="79893-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79893-110">PARAMETERS</span></span>

### <span data-ttu-id="79893-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79893-111">-DefaultProfile</span></span>
<span data-ttu-id="79893-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79893-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79893-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="79893-113">-EventHub</span></span>
<span data-ttu-id="79893-114">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="79893-114">EventHub Name</span></span>

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

### <span data-ttu-id="79893-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79893-115">-Name</span></span>
<span data-ttu-id="79893-116">Nazwa grupy konsumenckiej</span><span class="sxs-lookup"><span data-stu-id="79893-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="79893-117">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="79893-117">-Namespace</span></span>
<span data-ttu-id="79893-118">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="79893-118">Namespace Name</span></span>

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

### <span data-ttu-id="79893-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79893-119">-ResourceGroupName</span></span>
<span data-ttu-id="79893-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="79893-120">Resource Group Name</span></span>

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

### <span data-ttu-id="79893-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="79893-121">-UserMetadata</span></span>
<span data-ttu-id="79893-122">Metadane użytkownika dla grupy ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="79893-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="79893-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79893-123">-Confirm</span></span>
<span data-ttu-id="79893-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79893-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79893-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79893-125">-WhatIf</span></span>
<span data-ttu-id="79893-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79893-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79893-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79893-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79893-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79893-128">CommonParameters</span></span>
<span data-ttu-id="79893-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79893-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79893-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79893-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79893-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79893-131">INPUTS</span></span>

### <span data-ttu-id="79893-132">System.String</span><span class="sxs-lookup"><span data-stu-id="79893-132">System.String</span></span>

## <span data-ttu-id="79893-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79893-133">OUTPUTS</span></span>

### <span data-ttu-id="79893-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="79893-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="79893-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79893-135">NOTES</span></span>

## <span data-ttu-id="79893-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79893-136">RELATED LINKS</span></span>
