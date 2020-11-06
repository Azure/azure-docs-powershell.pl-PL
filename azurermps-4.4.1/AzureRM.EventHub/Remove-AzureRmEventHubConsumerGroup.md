---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549203"
---
# <span data-ttu-id="5974a-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5974a-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="5974a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5974a-102">SYNOPSIS</span></span>
<span data-ttu-id="5974a-103">Usuwa określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5974a-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5974a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5974a-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5974a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5974a-105">DESCRIPTION</span></span>
<span data-ttu-id="5974a-106">Polecenie cmdlet Remove-AzureRmEventHubConsumerGroup usuwa i usuwa określoną grupę klientów z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="5974a-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="5974a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5974a-107">EXAMPLES</span></span>

### <span data-ttu-id="5974a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5974a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="5974a-109">Usuwa MyConsumerGroupName grupy konsumenckiej \` \` z MyEventHubName centrum zdarzeń \` \` i zakresu do \` obszaru nazw moja przestrzeń nazw \` .</span><span class="sxs-lookup"><span data-stu-id="5974a-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="5974a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5974a-110">PARAMETERS</span></span>

### <span data-ttu-id="5974a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5974a-111">-ResourceGroupName</span></span>
<span data-ttu-id="5974a-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5974a-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5974a-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5974a-113">-Confirm</span></span>
<span data-ttu-id="5974a-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5974a-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5974a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5974a-115">-WhatIf</span></span>
<span data-ttu-id="5974a-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5974a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5974a-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5974a-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5974a-118">— EventHub</span><span class="sxs-lookup"><span data-stu-id="5974a-118">-EventHub</span></span>
<span data-ttu-id="5974a-119">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="5974a-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5974a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5974a-120">-Name</span></span>
<span data-ttu-id="5974a-121">Nazwa odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="5974a-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5974a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5974a-122">-Namespace</span></span>
<span data-ttu-id="5974a-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="5974a-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="5974a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5974a-124">INPUTS</span></span>

### <span data-ttu-id="5974a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5974a-125">System.String</span></span>

## <span data-ttu-id="5974a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5974a-126">OUTPUTS</span></span>

### <span data-ttu-id="5974a-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="5974a-127">System.Object</span></span>

## <span data-ttu-id="5974a-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5974a-128">NOTES</span></span>

## <span data-ttu-id="5974a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5974a-129">RELATED LINKS</span></span>

