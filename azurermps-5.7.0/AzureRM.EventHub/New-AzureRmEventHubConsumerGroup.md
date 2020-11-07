---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718494"
---
# <span data-ttu-id="87817-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="87817-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="87817-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87817-102">SYNOPSIS</span></span>
<span data-ttu-id="87817-103">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="87817-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87817-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87817-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87817-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87817-105">EXAMPLES</span></span>

### <span data-ttu-id="87817-106">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87817-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="87817-107">Tworzy MyConsumerGroupName grupy konsumenckiej \` \` w MyEventHubName centrum zdarzeń \` \` z zakresem nazw obszar_nazwname \` \` , z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="87817-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="87817-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87817-108">PARAMETERS</span></span>

### <span data-ttu-id="87817-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87817-109">-DefaultProfile</span></span>
<span data-ttu-id="87817-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87817-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87817-111">— EventHub</span><span class="sxs-lookup"><span data-stu-id="87817-111">-EventHub</span></span>
<span data-ttu-id="87817-112">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="87817-112">EventHub Name</span></span>

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

### <span data-ttu-id="87817-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87817-113">-Name</span></span>
<span data-ttu-id="87817-114">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="87817-114">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="87817-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="87817-115">-Namespace</span></span>
<span data-ttu-id="87817-116">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="87817-116">Namespace Name</span></span>

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

### <span data-ttu-id="87817-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87817-117">-ResourceGroupName</span></span>
<span data-ttu-id="87817-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="87817-118">Resource Group Name</span></span>

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

### <span data-ttu-id="87817-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="87817-119">-UserMetadata</span></span>
<span data-ttu-id="87817-120">Metadane użytkownika dla usługi Konsumenckej</span><span class="sxs-lookup"><span data-stu-id="87817-120">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="87817-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87817-121">-Confirm</span></span>
<span data-ttu-id="87817-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87817-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87817-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87817-123">-WhatIf</span></span>
<span data-ttu-id="87817-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87817-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87817-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87817-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87817-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87817-126">CommonParameters</span></span>
<span data-ttu-id="87817-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87817-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="87817-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87817-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87817-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87817-129">INPUTS</span></span>

### <span data-ttu-id="87817-130">System. String</span><span class="sxs-lookup"><span data-stu-id="87817-130">System.String</span></span>


## <span data-ttu-id="87817-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87817-131">OUTPUTS</span></span>

### <span data-ttu-id="87817-132">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="87817-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="87817-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87817-133">NOTES</span></span>

## <span data-ttu-id="87817-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87817-134">RELATED LINKS</span></span>
