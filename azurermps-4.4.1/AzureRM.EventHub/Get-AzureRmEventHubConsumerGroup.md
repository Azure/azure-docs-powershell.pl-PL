---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553908"
---
# <span data-ttu-id="aabdb-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="aabdb-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="aabdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aabdb-102">SYNOPSIS</span></span>
<span data-ttu-id="aabdb-103">Umożliwia wyświetlenie szczegółów dotyczących określonej grupy odbiorców koncentratorów zdarzeń lub wypełnianie listy grup klientów w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="aabdb-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aabdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aabdb-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="aabdb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aabdb-105">DESCRIPTION</span></span>
<span data-ttu-id="aabdb-106">Polecenie cmdlet Get-AzureRmEventHubConsumerGroup powoduje wyświetlenie szczegółów dotyczących określonej grupy użytkowników koncentratorów zdarzeń lub listy grup klientów w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="aabdb-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="aabdb-107">Jeśli jest podana nazwa grupy konsumenckiej, zostaną zwrócone szczegółowe dane dotyczące jednej grupy użytkowników.</span><span class="sxs-lookup"><span data-stu-id="aabdb-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="aabdb-108">Jeśli nie podano nazwy grupy konsumenckiej, zostanie zwrócona lista grup odbiorców określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="aabdb-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="aabdb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aabdb-109">EXAMPLES</span></span>

### <span data-ttu-id="aabdb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aabdb-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="aabdb-111">Pobiera MyConsumerGroupName grup konsumenckich \` \` w MyEventHubName centrum zdarzeń \` \` , które istnieją w przestrzeni nazw obszar_nazwname \` \` z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="aabdb-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="aabdb-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="aabdb-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="aabdb-113">Pobiera listę grup konsumenckich w MyEventHubName centrum zdarzeń \` \` , które istnieją w obszarze nazw obszar_nazwname \` \` z grupami zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="aabdb-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="aabdb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aabdb-114">PARAMETERS</span></span>

### <span data-ttu-id="aabdb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabdb-115">-ResourceGroupName</span></span>
<span data-ttu-id="aabdb-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aabdb-116">Resource group name.</span></span>

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

### <span data-ttu-id="aabdb-117">— EventHub</span><span class="sxs-lookup"><span data-stu-id="aabdb-117">-EventHub</span></span>
<span data-ttu-id="aabdb-118">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="aabdb-118">EventHub Name.</span></span>

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

### <span data-ttu-id="aabdb-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aabdb-119">-Name</span></span>
<span data-ttu-id="aabdb-120">Nazwa odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="aabdb-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aabdb-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aabdb-121">-Namespace</span></span>
<span data-ttu-id="aabdb-122">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="aabdb-122">Namespace Name.</span></span>

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

## <span data-ttu-id="aabdb-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aabdb-123">INPUTS</span></span>

### <span data-ttu-id="aabdb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="aabdb-124">System.String</span></span>

## <span data-ttu-id="aabdb-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aabdb-125">OUTPUTS</span></span>

### <span data-ttu-id="aabdb-126">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. ConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="aabdb-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="aabdb-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aabdb-127">NOTES</span></span>

## <span data-ttu-id="aabdb-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aabdb-128">RELATED LINKS</span></span>

