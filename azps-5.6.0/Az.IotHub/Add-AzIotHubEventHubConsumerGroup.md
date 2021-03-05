---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 23f6c4b7d40f0ec2e02541f82d5d517019bd15fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997872"
---
# <span data-ttu-id="64e2c-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="64e2c-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="64e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="64e2c-103">Tworzy grupę klientów z aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="64e2c-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="64e2c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64e2c-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64e2c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="64e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="64e2c-106">Tworzy grupę klienta w witrynie Eventhub skojarzoną z określoną usługą IotHub.</span><span class="sxs-lookup"><span data-stu-id="64e2c-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="64e2c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64e2c-107">EXAMPLES</span></span>

### <span data-ttu-id="64e2c-108">Przykład 1. Dodawanie grupy konsumentów do aplikacji Eventhub telemetrii</span><span class="sxs-lookup"><span data-stu-id="64e2c-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="64e2c-109">Dodaje nową grupę klientów o nazwie "myconsumergroup" do aplikacji Eventhub na wypadek zdarzeń telemetrii w aplikacji iothub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="64e2c-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="64e2c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64e2c-110">PARAMETERS</span></span>

### <span data-ttu-id="64e2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e2c-111">-DefaultProfile</span></span>
<span data-ttu-id="64e2c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="64e2c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64e2c-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="64e2c-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="64e2c-114">Nazwa grupy konsumenckiej aplikacji EventHub, którą chcesz dodać.</span><span class="sxs-lookup"><span data-stu-id="64e2c-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="64e2c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64e2c-115">-Name</span></span>
<span data-ttu-id="64e2c-116">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="64e2c-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="64e2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64e2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="64e2c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64e2c-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="64e2c-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64e2c-119">-Confirm</span></span>
<span data-ttu-id="64e2c-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="64e2c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64e2c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e2c-121">-WhatIf</span></span>
<span data-ttu-id="64e2c-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64e2c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e2c-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="64e2c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64e2c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e2c-124">CommonParameters</span></span>
<span data-ttu-id="64e2c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64e2c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e2c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64e2c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e2c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64e2c-127">INPUTS</span></span>

### <span data-ttu-id="64e2c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="64e2c-128">System.String</span></span>

## <span data-ttu-id="64e2c-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64e2c-129">OUTPUTS</span></span>

### <span data-ttu-id="64e2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="64e2c-130">System.String</span></span>

## <span data-ttu-id="64e2c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64e2c-131">NOTES</span></span>

## <span data-ttu-id="64e2c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64e2c-132">RELATED LINKS</span></span>
