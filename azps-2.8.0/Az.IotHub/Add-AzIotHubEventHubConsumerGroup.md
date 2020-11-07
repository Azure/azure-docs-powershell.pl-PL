---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705267"
---
# <span data-ttu-id="ecd82-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ecd82-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="ecd82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecd82-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd82-103">Tworzy grupę odbiorców eventhub.</span><span class="sxs-lookup"><span data-stu-id="ecd82-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="ecd82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecd82-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecd82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ecd82-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd82-106">Tworzy grupę odbiorców w centrum Eventhub skojarzonym z określonym IotHub.</span><span class="sxs-lookup"><span data-stu-id="ecd82-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="ecd82-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecd82-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd82-108">Przykład 1. Dodawanie grupy konsumenckiej do telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="ecd82-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="ecd82-109">Dodaje nową nazwę użytkownika "The Consumer" do centrum eventhub dla zdarzeń telemetrii w iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ecd82-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="ecd82-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecd82-110">PARAMETERS</span></span>

### <span data-ttu-id="ecd82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd82-111">-DefaultProfile</span></span>
<span data-ttu-id="ecd82-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ecd82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecd82-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd82-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="ecd82-114">Nazwa dodaną w centrum EventHub, którą chcesz dodać.</span><span class="sxs-lookup"><span data-stu-id="ecd82-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="ecd82-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="ecd82-115">-EventHubEndpointName</span></span>
<span data-ttu-id="ecd82-116">Nazwa punktu końcowego EventHub.</span><span class="sxs-lookup"><span data-stu-id="ecd82-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="ecd82-117">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="ecd82-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="ecd82-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ecd82-118">-Name</span></span>
<span data-ttu-id="ecd82-119">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="ecd82-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ecd82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd82-120">-ResourceGroupName</span></span>
<span data-ttu-id="ecd82-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ecd82-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ecd82-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ecd82-122">-Confirm</span></span>
<span data-ttu-id="ecd82-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd82-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd82-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd82-124">-WhatIf</span></span>
<span data-ttu-id="ecd82-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd82-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd82-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ecd82-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd82-127">CommonParameters</span></span>
<span data-ttu-id="ecd82-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd82-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd82-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd82-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecd82-130">INPUTS</span></span>

### <span data-ttu-id="ecd82-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd82-131">System.String</span></span>

## <span data-ttu-id="ecd82-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecd82-132">OUTPUTS</span></span>

### <span data-ttu-id="ecd82-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd82-133">System.String</span></span>

## <span data-ttu-id="ecd82-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecd82-134">NOTES</span></span>

## <span data-ttu-id="ecd82-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecd82-135">RELATED LINKS</span></span>
