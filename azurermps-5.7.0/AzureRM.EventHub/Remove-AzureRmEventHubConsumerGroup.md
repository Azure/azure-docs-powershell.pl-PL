---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545743"
---
# <span data-ttu-id="bfb2f-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="bfb2f-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="bfb2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb2f-103">Usuwa określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfb2f-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfb2f-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb2f-106">Polecenie cmdlet Remove-AzureRmEventHubConsumerGroup usuwa i usuwa określoną grupę klientów z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="bfb2f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfb2f-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb2f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bfb2f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="bfb2f-109">Usuwa MyConsumerGroupName grupy konsumenckiej \` \` z MyEventHubName centrum zdarzeń \` \` i zakresu do \` obszaru nazw moja przestrzeń nazw \` .</span><span class="sxs-lookup"><span data-stu-id="bfb2f-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="bfb2f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfb2f-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb2f-111">-DefaultProfile</span></span>
<span data-ttu-id="bfb2f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb2f-113">— EventHub</span><span class="sxs-lookup"><span data-stu-id="bfb2f-113">-EventHub</span></span>
<span data-ttu-id="bfb2f-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="bfb2f-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb2f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfb2f-115">-Name</span></span>
<span data-ttu-id="bfb2f-116">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="bfb2f-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb2f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bfb2f-117">-Namespace</span></span>
<span data-ttu-id="bfb2f-118">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="bfb2f-118">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfb2f-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bfb2f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="bfb2f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfb2f-121">-Confirm</span></span>
<span data-ttu-id="bfb2f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb2f-123">-WhatIf</span></span>
<span data-ttu-id="bfb2f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb2f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb2f-126">CommonParameters</span></span>
<span data-ttu-id="bfb2f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bfb2f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb2f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfb2f-129">INPUTS</span></span>

### <span data-ttu-id="bfb2f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bfb2f-130">System.String</span></span>


## <span data-ttu-id="bfb2f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfb2f-131">OUTPUTS</span></span>

### <span data-ttu-id="bfb2f-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="bfb2f-132">System.Object</span></span>

## <span data-ttu-id="bfb2f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfb2f-133">NOTES</span></span>

## <span data-ttu-id="bfb2f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfb2f-134">RELATED LINKS</span></span>
