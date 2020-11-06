---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 192a20ee3d49bd79dff833a05ffd3ff98bcc30ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552919"
---
# <span data-ttu-id="a9b23-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a9b23-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="a9b23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9b23-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b23-103">Tworzy grupę odbiorców eventhub.</span><span class="sxs-lookup"><span data-stu-id="a9b23-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9b23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9b23-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9b23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9b23-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b23-106">Tworzy grupę odbiorców w centrum Eventhub skojarzonym z określonym IotHub.</span><span class="sxs-lookup"><span data-stu-id="a9b23-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="a9b23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9b23-107">EXAMPLES</span></span>

### <span data-ttu-id="a9b23-108">Przykład 1. Dodawanie grupy konsumenckiej do telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="a9b23-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="a9b23-109">Dodaje nową nazwę użytkownika "The Consumer" do centrum eventhub dla zdarzeń telemetrii w iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a9b23-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="a9b23-110">Przykład 2: Dodawanie grupy konsumenckiej do monitorowania operacji eventhub</span><span class="sxs-lookup"><span data-stu-id="a9b23-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="a9b23-111">Dodaje nową nazwę użytkownika "The Consumer" do zdarzeń monitorowania operacji eventhub na iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a9b23-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="a9b23-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9b23-112">PARAMETERS</span></span>

### <span data-ttu-id="a9b23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b23-113">-DefaultProfile</span></span>
<span data-ttu-id="a9b23-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a9b23-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9b23-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b23-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="a9b23-116">Nazwa dodaną w centrum EventHub, którą chcesz dodać.</span><span class="sxs-lookup"><span data-stu-id="a9b23-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b23-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="a9b23-117">-EventHubEndpointName</span></span>
<span data-ttu-id="a9b23-118">Nazwa punktu końcowego EventHub.</span><span class="sxs-lookup"><span data-stu-id="a9b23-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="a9b23-119">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="a9b23-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b23-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9b23-120">-Name</span></span>
<span data-ttu-id="a9b23-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="a9b23-121">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b23-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9b23-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9b23-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="a9b23-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9b23-124">-Confirm</span></span>
<span data-ttu-id="a9b23-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b23-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9b23-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b23-126">-WhatIf</span></span>
<span data-ttu-id="a9b23-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b23-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9b23-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9b23-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9b23-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b23-129">CommonParameters</span></span>
<span data-ttu-id="a9b23-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b23-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b23-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b23-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b23-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9b23-132">INPUTS</span></span>

### <span data-ttu-id="a9b23-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a9b23-133">System.String</span></span>

## <span data-ttu-id="a9b23-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9b23-134">OUTPUTS</span></span>

### <span data-ttu-id="a9b23-135">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9b23-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a9b23-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9b23-136">NOTES</span></span>

## <span data-ttu-id="a9b23-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9b23-137">RELATED LINKS</span></span>

