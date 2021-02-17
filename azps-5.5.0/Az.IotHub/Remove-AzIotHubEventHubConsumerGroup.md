---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188186"
---
# <span data-ttu-id="4a77a-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4a77a-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="4a77a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a77a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a77a-103">Usuwa grupę konsumencką aplikacji Eventhub.</span><span class="sxs-lookup"><span data-stu-id="4a77a-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="4a77a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a77a-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a77a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a77a-105">DESCRIPTION</span></span>
<span data-ttu-id="4a77a-106">Usuwa grupę konsumencką aplikacji Eventhub.</span><span class="sxs-lookup"><span data-stu-id="4a77a-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="4a77a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a77a-107">EXAMPLES</span></span>

### <span data-ttu-id="4a77a-108">Przykład 1. Usuwanie grupy konsumenckiej aplikacji Eventhub z telemetrii aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="4a77a-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="4a77a-109">Usuwa grupę o nazwie myconsumergroup z usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="4a77a-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4a77a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a77a-110">PARAMETERS</span></span>

### <span data-ttu-id="4a77a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a77a-111">-DefaultProfile</span></span>
<span data-ttu-id="4a77a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4a77a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a77a-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="4a77a-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="4a77a-114">Nazwa grupy konsumenckiej aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="4a77a-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a77a-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4a77a-115">-Name</span></span>
<span data-ttu-id="4a77a-116">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="4a77a-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="4a77a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a77a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a77a-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4a77a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4a77a-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a77a-119">-Confirm</span></span>
<span data-ttu-id="4a77a-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4a77a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a77a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a77a-121">-WhatIf</span></span>
<span data-ttu-id="4a77a-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a77a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a77a-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4a77a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a77a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a77a-124">CommonParameters</span></span>
<span data-ttu-id="4a77a-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a77a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a77a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a77a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a77a-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a77a-127">INPUTS</span></span>

### <span data-ttu-id="4a77a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4a77a-128">System.String</span></span>

## <span data-ttu-id="4a77a-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a77a-129">OUTPUTS</span></span>

### <span data-ttu-id="4a77a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4a77a-130">System.String</span></span>

## <span data-ttu-id="4a77a-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a77a-131">NOTES</span></span>

## <span data-ttu-id="4a77a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a77a-132">RELATED LINKS</span></span>
