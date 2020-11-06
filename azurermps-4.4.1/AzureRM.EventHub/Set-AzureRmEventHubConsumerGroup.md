---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551019"
---
# <span data-ttu-id="d28a9-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d28a9-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d28a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d28a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d28a9-103">Aktualizuje określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="d28a9-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d28a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d28a9-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d28a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d28a9-105">DESCRIPTION</span></span>
<span data-ttu-id="d28a9-106">Polecenie cmdlet Set-AzureRmEventHubConsumerGroup aktualizuje określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="d28a9-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="d28a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d28a9-107">EXAMPLES</span></span>

### <span data-ttu-id="d28a9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d28a9-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="d28a9-109">Ustawia metadane użytkownika grupy \` MyConsumerGroupName \` na "testowanie".</span><span class="sxs-lookup"><span data-stu-id="d28a9-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="d28a9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d28a9-110">PARAMETERS</span></span>

### <span data-ttu-id="d28a9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d28a9-111">-ResourceGroupName</span></span>
<span data-ttu-id="d28a9-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d28a9-112">Resource group name.</span></span>

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

### <span data-ttu-id="d28a9-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d28a9-113">-UserMetadata</span></span>
<span data-ttu-id="d28a9-114">Metadane użytkownika dla grupy odbiorców (opcjonalnie).</span><span class="sxs-lookup"><span data-stu-id="d28a9-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="d28a9-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d28a9-115">-Confirm</span></span>
<span data-ttu-id="d28a9-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d28a9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d28a9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d28a9-117">-WhatIf</span></span>
<span data-ttu-id="d28a9-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d28a9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d28a9-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d28a9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d28a9-120">— EventHub</span><span class="sxs-lookup"><span data-stu-id="d28a9-120">-EventHub</span></span>
<span data-ttu-id="d28a9-121">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="d28a9-121">EventHub Name.</span></span>

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

### <span data-ttu-id="d28a9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d28a9-122">-Name</span></span>
<span data-ttu-id="d28a9-123">Nazwa odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="d28a9-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="d28a9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d28a9-124">-Namespace</span></span>
<span data-ttu-id="d28a9-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="d28a9-125">Namespace Name.</span></span>

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

## <span data-ttu-id="d28a9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d28a9-126">INPUTS</span></span>

### <span data-ttu-id="d28a9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d28a9-127">System.String</span></span>

## <span data-ttu-id="d28a9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d28a9-128">OUTPUTS</span></span>

### <span data-ttu-id="d28a9-129">Microsoft. Azure. Commands. EventHub. modele. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="d28a9-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="d28a9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d28a9-130">NOTES</span></span>

## <span data-ttu-id="d28a9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d28a9-131">RELATED LINKS</span></span>

