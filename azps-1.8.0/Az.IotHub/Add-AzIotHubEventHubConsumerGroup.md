---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: c4378b156d17759c180ee3bf966bc20d06d00b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868160"
---
# <span data-ttu-id="6d100-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6d100-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="6d100-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d100-102">SYNOPSIS</span></span>
<span data-ttu-id="6d100-103">Tworzy grupę odbiorców eventhub.</span><span class="sxs-lookup"><span data-stu-id="6d100-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="6d100-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d100-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d100-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d100-105">DESCRIPTION</span></span>
<span data-ttu-id="6d100-106">Tworzy grupę odbiorców w centrum Eventhub skojarzonym z określonym IotHub.</span><span class="sxs-lookup"><span data-stu-id="6d100-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="6d100-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d100-107">EXAMPLES</span></span>

### <span data-ttu-id="6d100-108">Przykład 1. Dodawanie grupy konsumenckiej do telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="6d100-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="6d100-109">Dodaje nową nazwę użytkownika "The Consumer" do centrum eventhub dla zdarzeń telemetrii w iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="6d100-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="6d100-110">Przykład 2: Dodawanie grupy konsumenckiej do monitorowania operacji eventhub</span><span class="sxs-lookup"><span data-stu-id="6d100-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="6d100-111">Dodaje nową nazwę użytkownika "The Consumer" do zdarzeń monitorowania operacji eventhub na iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="6d100-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="6d100-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d100-112">PARAMETERS</span></span>

### <span data-ttu-id="6d100-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d100-113">-DefaultProfile</span></span>
<span data-ttu-id="6d100-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d100-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d100-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="6d100-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="6d100-116">Nazwa dodaną w centrum EventHub, którą chcesz dodać.</span><span class="sxs-lookup"><span data-stu-id="6d100-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d100-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="6d100-117">-EventHubEndpointName</span></span>
<span data-ttu-id="6d100-118">Nazwa punktu końcowego EventHub.</span><span class="sxs-lookup"><span data-stu-id="6d100-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="6d100-119">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="6d100-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d100-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d100-120">-Name</span></span>
<span data-ttu-id="6d100-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="6d100-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d100-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d100-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d100-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d100-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="6d100-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d100-124">-Confirm</span></span>
<span data-ttu-id="6d100-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d100-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d100-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d100-126">-WhatIf</span></span>
<span data-ttu-id="6d100-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d100-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d100-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d100-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d100-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d100-129">CommonParameters</span></span>
<span data-ttu-id="6d100-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d100-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d100-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d100-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d100-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d100-132">INPUTS</span></span>

### <span data-ttu-id="6d100-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6d100-133">System.String</span></span>

## <span data-ttu-id="6d100-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d100-134">OUTPUTS</span></span>

### <span data-ttu-id="6d100-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6d100-135">System.String</span></span>

## <span data-ttu-id="6d100-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d100-136">NOTES</span></span>

## <span data-ttu-id="6d100-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d100-137">RELATED LINKS</span></span>
