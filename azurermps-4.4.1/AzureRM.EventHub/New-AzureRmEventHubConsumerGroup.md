---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719325"
---
# <span data-ttu-id="b8e27-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b8e27-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="b8e27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8e27-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e27-103">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b8e27-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8e27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8e27-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b8e27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8e27-105">DESCRIPTION</span></span>
<span data-ttu-id="b8e27-106">Polecenie cmdlet New-AzureRmEventHubConsumerGroup powoduje utworzenie nowej grupy odbiorców dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b8e27-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="b8e27-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8e27-107">EXAMPLES</span></span>

### <span data-ttu-id="b8e27-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8e27-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="b8e27-109">Tworzy MyConsumerGroupName grupy konsumenckiej \` \` w MyEventHubName centrum zdarzeń \` \` z zakresem nazw obszar_nazwname \` \` , z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b8e27-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b8e27-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8e27-110">PARAMETERS</span></span>

### <span data-ttu-id="b8e27-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e27-111">-ResourceGroupName</span></span>
<span data-ttu-id="b8e27-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8e27-112">Resource group name.</span></span>

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

### <span data-ttu-id="b8e27-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b8e27-113">-UserMetadata</span></span>
<span data-ttu-id="b8e27-114">Metadane użytkownika dla grupy odbiorców.</span><span class="sxs-lookup"><span data-stu-id="b8e27-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e27-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8e27-115">-Confirm</span></span>
<span data-ttu-id="b8e27-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8e27-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e27-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e27-117">-WhatIf</span></span>
<span data-ttu-id="b8e27-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8e27-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e27-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8e27-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e27-120">— EventHub</span><span class="sxs-lookup"><span data-stu-id="b8e27-120">-EventHub</span></span>
<span data-ttu-id="b8e27-121">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="b8e27-121">EventHub Name.</span></span>

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

### <span data-ttu-id="b8e27-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8e27-122">-Name</span></span>
<span data-ttu-id="b8e27-123">Nazwa odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="b8e27-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="b8e27-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8e27-124">-Namespace</span></span>
<span data-ttu-id="b8e27-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b8e27-125">Namespace Name.</span></span>

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

## <span data-ttu-id="b8e27-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8e27-126">INPUTS</span></span>

### <span data-ttu-id="b8e27-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b8e27-127">System.String</span></span>

## <span data-ttu-id="b8e27-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8e27-128">OUTPUTS</span></span>

### <span data-ttu-id="b8e27-129">Microsoft. Azure. Commands. EventHub. modele. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="b8e27-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="b8e27-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8e27-130">NOTES</span></span>

## <span data-ttu-id="b8e27-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8e27-131">RELATED LINKS</span></span>

