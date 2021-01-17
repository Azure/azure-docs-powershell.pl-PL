---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386967"
---
# <span data-ttu-id="07e0c-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="07e0c-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="07e0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="07e0c-103">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="07e0c-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="07e0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07e0c-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07e0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="07e0c-106">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="07e0c-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="07e0c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="07e0c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07e0c-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="07e0c-109">Tworzy MyConsumerGroupName grupy konsumenckiej \` \` w MyEventHubName centrum zdarzeń \` \` z zakresem nazw obszar_nazwname \` \` , z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="07e0c-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="07e0c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="07e0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e0c-111">-DefaultProfile</span></span>
<span data-ttu-id="07e0c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="07e0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e0c-113">— EventHub</span><span class="sxs-lookup"><span data-stu-id="07e0c-113">-EventHub</span></span>
<span data-ttu-id="07e0c-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="07e0c-114">EventHub Name</span></span>

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

### <span data-ttu-id="07e0c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="07e0c-115">-Name</span></span>
<span data-ttu-id="07e0c-116">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="07e0c-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="07e0c-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07e0c-117">-Namespace</span></span>
<span data-ttu-id="07e0c-118">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="07e0c-118">Namespace Name</span></span>

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

### <span data-ttu-id="07e0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="07e0c-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="07e0c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="07e0c-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="07e0c-121">-UserMetadata</span></span>
<span data-ttu-id="07e0c-122">Metadane użytkownika dla usługi Konsumenckej</span><span class="sxs-lookup"><span data-stu-id="07e0c-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="07e0c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07e0c-123">-Confirm</span></span>
<span data-ttu-id="07e0c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e0c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e0c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e0c-125">-WhatIf</span></span>
<span data-ttu-id="07e0c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e0c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07e0c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07e0c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e0c-128">CommonParameters</span></span>
<span data-ttu-id="07e0c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e0c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e0c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e0c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07e0c-131">INPUTS</span></span>

### <span data-ttu-id="07e0c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="07e0c-132">System.String</span></span>

## <span data-ttu-id="07e0c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07e0c-133">OUTPUTS</span></span>

### <span data-ttu-id="07e0c-134">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="07e0c-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="07e0c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07e0c-135">NOTES</span></span>

## <span data-ttu-id="07e0c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07e0c-136">RELATED LINKS</span></span>
