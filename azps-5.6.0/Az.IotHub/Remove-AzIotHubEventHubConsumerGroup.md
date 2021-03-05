---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 1e563126bb57986bed752184340808991f7e2a00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974849"
---
# <span data-ttu-id="b7e56-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b7e56-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b7e56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e56-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e56-103">Usuwa grupę konsumencką aplikacji Eventhub.</span><span class="sxs-lookup"><span data-stu-id="b7e56-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b7e56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7e56-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7e56-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7e56-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e56-106">Usuwa grupę konsumencką aplikacji Eventhub.</span><span class="sxs-lookup"><span data-stu-id="b7e56-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b7e56-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7e56-107">EXAMPLES</span></span>

### <span data-ttu-id="b7e56-108">Przykład 1. Usuwanie grupy konsumenckiej aplikacji Eventhub z telemetrii aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="b7e56-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="b7e56-109">Usuwa grupę o nazwie myconsumergroup z usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b7e56-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b7e56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7e56-110">PARAMETERS</span></span>

### <span data-ttu-id="b7e56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e56-111">-DefaultProfile</span></span>
<span data-ttu-id="b7e56-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b7e56-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7e56-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e56-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b7e56-114">Nazwa grupy konsumenckiej aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="b7e56-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="b7e56-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b7e56-115">-Name</span></span>
<span data-ttu-id="b7e56-116">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="b7e56-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="b7e56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e56-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7e56-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b7e56-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b7e56-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7e56-119">-Confirm</span></span>
<span data-ttu-id="b7e56-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7e56-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e56-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e56-121">-WhatIf</span></span>
<span data-ttu-id="b7e56-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e56-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e56-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b7e56-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e56-124">CommonParameters</span></span>
<span data-ttu-id="b7e56-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e56-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e56-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e56-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e56-127">INPUTS</span></span>

### <span data-ttu-id="b7e56-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b7e56-128">System.String</span></span>

## <span data-ttu-id="b7e56-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e56-129">OUTPUTS</span></span>

### <span data-ttu-id="b7e56-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b7e56-130">System.String</span></span>

## <span data-ttu-id="b7e56-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7e56-131">NOTES</span></span>

## <span data-ttu-id="b7e56-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7e56-132">RELATED LINKS</span></span>
