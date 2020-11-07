---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: c887aab15e0874357ec32d9c815a9a9b1dd1227a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705443"
---
# <span data-ttu-id="0cd43-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0cd43-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="0cd43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cd43-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd43-103">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="0cd43-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="0cd43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cd43-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd43-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0cd43-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd43-106">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="0cd43-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="0cd43-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cd43-107">EXAMPLES</span></span>

### <span data-ttu-id="0cd43-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0cd43-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="0cd43-109">Tworzy MyConsumerGroupName grupy konsumenckiej \` \` w MyEventHubName centrum zdarzeń \` \` z zakresem nazw obszar_nazwname \` \` , z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="0cd43-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0cd43-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cd43-110">PARAMETERS</span></span>

### <span data-ttu-id="0cd43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd43-111">-DefaultProfile</span></span>
<span data-ttu-id="0cd43-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cd43-113">— EventHub</span><span class="sxs-lookup"><span data-stu-id="0cd43-113">-EventHub</span></span>
<span data-ttu-id="0cd43-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="0cd43-114">EventHub Name</span></span>

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

### <span data-ttu-id="0cd43-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0cd43-115">-Name</span></span>
<span data-ttu-id="0cd43-116">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="0cd43-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="0cd43-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0cd43-117">-Namespace</span></span>
<span data-ttu-id="0cd43-118">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0cd43-118">Namespace Name</span></span>

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

### <span data-ttu-id="0cd43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd43-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cd43-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0cd43-120">Resource Group Name</span></span>

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

### <span data-ttu-id="0cd43-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="0cd43-121">-UserMetadata</span></span>
<span data-ttu-id="0cd43-122">Metadane użytkownika dla usługi Konsumenckej</span><span class="sxs-lookup"><span data-stu-id="0cd43-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="0cd43-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0cd43-123">-Confirm</span></span>
<span data-ttu-id="0cd43-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd43-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd43-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd43-125">-WhatIf</span></span>
<span data-ttu-id="0cd43-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd43-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cd43-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0cd43-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cd43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd43-128">CommonParameters</span></span>
<span data-ttu-id="0cd43-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd43-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd43-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd43-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cd43-131">INPUTS</span></span>

### <span data-ttu-id="0cd43-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0cd43-132">System.String</span></span>

## <span data-ttu-id="0cd43-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cd43-133">OUTPUTS</span></span>

### <span data-ttu-id="0cd43-134">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="0cd43-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="0cd43-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cd43-135">NOTES</span></span>

## <span data-ttu-id="0cd43-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cd43-136">RELATED LINKS</span></span>
