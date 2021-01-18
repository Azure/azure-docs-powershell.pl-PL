---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503515"
---
# <span data-ttu-id="5d830-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5d830-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5d830-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d830-102">SYNOPSIS</span></span>
<span data-ttu-id="5d830-103">Tworzy grupę odbiorców eventhub.</span><span class="sxs-lookup"><span data-stu-id="5d830-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="5d830-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d830-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d830-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d830-105">DESCRIPTION</span></span>
<span data-ttu-id="5d830-106">Tworzy grupę odbiorców w centrum Eventhub skojarzonym z określonym IotHub.</span><span class="sxs-lookup"><span data-stu-id="5d830-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="5d830-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d830-107">EXAMPLES</span></span>

### <span data-ttu-id="5d830-108">Przykład 1. Dodawanie grupy konsumenckiej do telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="5d830-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="5d830-109">Dodaje nową nazwę użytkownika "The Consumer" do centrum eventhub dla zdarzeń telemetrii w iothub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="5d830-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="5d830-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d830-110">PARAMETERS</span></span>

### <span data-ttu-id="5d830-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d830-111">-DefaultProfile</span></span>
<span data-ttu-id="5d830-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d830-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d830-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5d830-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5d830-114">Nazwa dodaną w centrum EventHub, którą chcesz dodać.</span><span class="sxs-lookup"><span data-stu-id="5d830-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d830-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d830-115">-Name</span></span>
<span data-ttu-id="5d830-116">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5d830-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5d830-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d830-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d830-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d830-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="5d830-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d830-119">-Confirm</span></span>
<span data-ttu-id="5d830-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d830-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d830-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d830-121">-WhatIf</span></span>
<span data-ttu-id="5d830-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d830-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d830-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d830-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d830-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d830-124">CommonParameters</span></span>
<span data-ttu-id="5d830-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d830-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d830-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d830-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d830-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d830-127">INPUTS</span></span>

### <span data-ttu-id="5d830-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5d830-128">System.String</span></span>

## <span data-ttu-id="5d830-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d830-129">OUTPUTS</span></span>

### <span data-ttu-id="5d830-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5d830-130">System.String</span></span>

## <span data-ttu-id="5d830-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d830-131">NOTES</span></span>

## <span data-ttu-id="5d830-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d830-132">RELATED LINKS</span></span>
