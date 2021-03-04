---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 4b34731c0cd0c2d49a7c26112d370d8d4a2f948e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957274"
---
# <span data-ttu-id="6f5f6-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6f5f6-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="6f5f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5f6-103">Pobiera szczegółowe informacje dotyczące określonej grupy klientów w centrum zdarzeń lub listę grup dla klientów konsumenckich w Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="6f5f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6f5f6-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f5f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6f5f6-105">DESCRIPTION</span></span>
<span data-ttu-id="6f5f6-106">Polecenie cmdlet Get-AzEventHubConsumerGroup szczegółowe informacje dotyczące określonej grupy klientów z centrum zdarzeń lub listy grup konsumentów w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="6f5f6-107">Jeśli podano nazwę grupy konsumenckiej, zostaną zwrócone szczegóły dotyczące jednej grupy klientów.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="6f5f6-108">Jeśli nazwa grupy konsumenckiej nie jest podana, jest zwracana lista grup konsumentów w określonym Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="6f5f6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6f5f6-109">EXAMPLES</span></span>

### <span data-ttu-id="6f5f6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f5f6-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="6f5f6-111">Pobiera grupę konsumencką MyConsumerGroupName w centrum zdarzeń MyEventHubName, które istnieje w przestrzeni nazw MyNamespaceName z grupą zasobów \` \` \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6f5f6-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6f5f6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6f5f6-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6f5f6-113">Pobiera listę grup konsumentów w centrum zdarzeń MyEventHubName, które istnieje w przestrzeni nazw MyNamespaceName z grupą zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6f5f6-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6f5f6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f5f6-114">PARAMETERS</span></span>

### <span data-ttu-id="6f5f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5f6-115">-DefaultProfile</span></span>
<span data-ttu-id="6f5f6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f5f6-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6f5f6-117">-EventHub</span></span>
<span data-ttu-id="6f5f6-118">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="6f5f6-118">EventHub Name</span></span>

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

### <span data-ttu-id="6f5f6-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6f5f6-119">-MaxCount</span></span>
<span data-ttu-id="6f5f6-120">Określ maksymalną liczbę zwracanych grup klientów.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5f6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6f5f6-121">-Name</span></span>
<span data-ttu-id="6f5f6-122">Nazwa grupy konsumenckiej</span><span class="sxs-lookup"><span data-stu-id="6f5f6-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f5f6-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="6f5f6-123">-Namespace</span></span>
<span data-ttu-id="6f5f6-124">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="6f5f6-124">Namespace Name</span></span>

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

### <span data-ttu-id="6f5f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f5f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f5f6-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6f5f6-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6f5f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5f6-127">CommonParameters</span></span>
<span data-ttu-id="6f5f6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f5f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5f6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5f6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5f6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f5f6-130">INPUTS</span></span>

### <span data-ttu-id="6f5f6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6f5f6-131">System.String</span></span>

## <span data-ttu-id="6f5f6-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f5f6-132">OUTPUTS</span></span>

### <span data-ttu-id="6f5f6-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="6f5f6-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="6f5f6-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6f5f6-134">NOTES</span></span>

## <span data-ttu-id="6f5f6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f5f6-135">RELATED LINKS</span></span>
