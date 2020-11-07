---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59a180d422a27ca9d2c3e1e4932d843ba7c70093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868072"
---
# <span data-ttu-id="e4a35-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e4a35-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="e4a35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4a35-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a35-103">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="e4a35-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="e4a35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4a35-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4a35-105">DESCRIPTION</span></span>
<span data-ttu-id="e4a35-106">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="e4a35-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="e4a35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4a35-107">EXAMPLES</span></span>

### <span data-ttu-id="e4a35-108">Przykład 1 Usuwanie z centrum telemetrycznego tej samej firmy eventhub</span><span class="sxs-lookup"><span data-stu-id="e4a35-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="e4a35-109">Usuwa z IotHub "myiothub" nazwę użytkownika o nazwie "".</span><span class="sxs-lookup"><span data-stu-id="e4a35-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e4a35-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4a35-110">PARAMETERS</span></span>

### <span data-ttu-id="e4a35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a35-111">-DefaultProfile</span></span>
<span data-ttu-id="e4a35-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4a35-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4a35-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a35-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="e4a35-114">Nazwa odbiorcy EventHub.</span><span class="sxs-lookup"><span data-stu-id="e4a35-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4a35-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="e4a35-115">-EventHubEndpointName</span></span>
<span data-ttu-id="e4a35-116">Nazwa punktu końcowego EventHub.</span><span class="sxs-lookup"><span data-stu-id="e4a35-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="e4a35-117">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="e4a35-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="e4a35-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4a35-118">-Name</span></span>
<span data-ttu-id="e4a35-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="e4a35-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="e4a35-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a35-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4a35-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e4a35-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e4a35-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4a35-122">-Confirm</span></span>
<span data-ttu-id="e4a35-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a35-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a35-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a35-124">-WhatIf</span></span>
<span data-ttu-id="e4a35-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a35-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4a35-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4a35-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a35-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a35-127">CommonParameters</span></span>
<span data-ttu-id="e4a35-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4a35-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a35-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a35-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a35-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4a35-130">INPUTS</span></span>

### <span data-ttu-id="e4a35-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e4a35-131">System.String</span></span>

## <span data-ttu-id="e4a35-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4a35-132">OUTPUTS</span></span>

### <span data-ttu-id="e4a35-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e4a35-133">System.String</span></span>

## <span data-ttu-id="e4a35-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4a35-134">NOTES</span></span>

## <span data-ttu-id="e4a35-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4a35-135">RELATED LINKS</span></span>
