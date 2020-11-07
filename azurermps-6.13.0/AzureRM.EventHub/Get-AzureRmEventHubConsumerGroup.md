---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 205dc883f8f6e0481f88438137ca45ad7a99c4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717409"
---
# <span data-ttu-id="dad73-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="dad73-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="dad73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dad73-102">SYNOPSIS</span></span>
<span data-ttu-id="dad73-103">Umożliwia wyświetlenie szczegółów dotyczących określonej grupy odbiorców koncentratorów zdarzeń lub wypełnianie listy grup klientów w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dad73-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dad73-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dad73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dad73-105">DESCRIPTION</span></span>
<span data-ttu-id="dad73-106">Polecenie cmdlet Get-AzureRmEventHubConsumerGroup powoduje wyświetlenie szczegółów dotyczących określonej grupy użytkowników koncentratorów zdarzeń lub listy grup klientów w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dad73-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="dad73-107">Jeśli jest podana nazwa grupy konsumenckiej, zostaną zwrócone szczegółowe dane dotyczące jednej grupy użytkowników.</span><span class="sxs-lookup"><span data-stu-id="dad73-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="dad73-108">Jeśli nie podano nazwy grupy konsumenckiej, zostanie zwrócona lista grup odbiorców określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dad73-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="dad73-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dad73-109">EXAMPLES</span></span>

### <span data-ttu-id="dad73-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dad73-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="dad73-111">Pobiera MyConsumerGroupName grup konsumenckich \` \` w MyEventHubName centrum zdarzeń \` \` , które istnieją w przestrzeni nazw obszar_nazwname \` \` z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="dad73-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="dad73-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dad73-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="dad73-113">Pobiera listę grup konsumenckich w MyEventHubName centrum zdarzeń \` \` , które istnieją w obszarze nazw obszar_nazwname \` \` z grupami zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="dad73-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="dad73-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dad73-114">PARAMETERS</span></span>

### <span data-ttu-id="dad73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad73-115">-DefaultProfile</span></span>
<span data-ttu-id="dad73-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dad73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad73-117">— EventHub</span><span class="sxs-lookup"><span data-stu-id="dad73-117">-EventHub</span></span>
<span data-ttu-id="dad73-118">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="dad73-118">EventHub Name</span></span>

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

### <span data-ttu-id="dad73-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="dad73-119">-MaxCount</span></span>
<span data-ttu-id="dad73-120">Określ maksymalną liczbę zwracanych ConsumerGroups.</span><span class="sxs-lookup"><span data-stu-id="dad73-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="dad73-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dad73-121">-Name</span></span>
<span data-ttu-id="dad73-122">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="dad73-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="dad73-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dad73-123">-Namespace</span></span>
<span data-ttu-id="dad73-124">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="dad73-124">Namespace Name</span></span>

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

### <span data-ttu-id="dad73-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad73-125">-ResourceGroupName</span></span>
<span data-ttu-id="dad73-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dad73-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dad73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad73-127">CommonParameters</span></span>
<span data-ttu-id="dad73-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad73-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad73-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad73-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dad73-130">INPUTS</span></span>

### <span data-ttu-id="dad73-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dad73-131">System.String</span></span>

## <span data-ttu-id="dad73-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dad73-132">OUTPUTS</span></span>

### <span data-ttu-id="dad73-133">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="dad73-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="dad73-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dad73-134">NOTES</span></span>

## <span data-ttu-id="dad73-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dad73-135">RELATED LINKS</span></span>