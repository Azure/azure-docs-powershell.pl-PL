---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062704"
---
# <span data-ttu-id="574ba-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="574ba-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="574ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="574ba-102">SYNOPSIS</span></span>
<span data-ttu-id="574ba-103">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="574ba-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="574ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="574ba-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="574ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="574ba-105">DESCRIPTION</span></span>
<span data-ttu-id="574ba-106">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="574ba-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="574ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="574ba-107">EXAMPLES</span></span>

### <span data-ttu-id="574ba-108">Przykład 1 Usuwanie z centrum telemetrycznego tej samej firmy eventhub</span><span class="sxs-lookup"><span data-stu-id="574ba-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="574ba-109">Usuwa z IotHub "myiothub" nazwę użytkownika o nazwie "".</span><span class="sxs-lookup"><span data-stu-id="574ba-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="574ba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="574ba-110">PARAMETERS</span></span>

### <span data-ttu-id="574ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574ba-111">-DefaultProfile</span></span>
<span data-ttu-id="574ba-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="574ba-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="574ba-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="574ba-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="574ba-114">Nazwa odbiorcy EventHub.</span><span class="sxs-lookup"><span data-stu-id="574ba-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="574ba-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="574ba-115">-Name</span></span>
<span data-ttu-id="574ba-116">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="574ba-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="574ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="574ba-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="574ba-118">Resource Group Name</span></span>

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

### <span data-ttu-id="574ba-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="574ba-119">-Confirm</span></span>
<span data-ttu-id="574ba-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="574ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="574ba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="574ba-121">-WhatIf</span></span>
<span data-ttu-id="574ba-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="574ba-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="574ba-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="574ba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="574ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574ba-124">CommonParameters</span></span>
<span data-ttu-id="574ba-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="574ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574ba-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574ba-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574ba-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="574ba-127">INPUTS</span></span>

### <span data-ttu-id="574ba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="574ba-128">System.String</span></span>

## <span data-ttu-id="574ba-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="574ba-129">OUTPUTS</span></span>

### <span data-ttu-id="574ba-130">System. String</span><span class="sxs-lookup"><span data-stu-id="574ba-130">System.String</span></span>

## <span data-ttu-id="574ba-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="574ba-131">NOTES</span></span>

## <span data-ttu-id="574ba-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="574ba-132">RELATED LINKS</span></span>
