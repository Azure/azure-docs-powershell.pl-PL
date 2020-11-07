---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891358"
---
# <span data-ttu-id="d7de4-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d7de4-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d7de4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7de4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7de4-103">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="d7de4-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="d7de4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7de4-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7de4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7de4-105">DESCRIPTION</span></span>
<span data-ttu-id="d7de4-106">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="d7de4-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="d7de4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7de4-107">EXAMPLES</span></span>

### <span data-ttu-id="d7de4-108">Przykład 1 Usuwanie z centrum telemetrycznego tej samej firmy eventhub</span><span class="sxs-lookup"><span data-stu-id="d7de4-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="d7de4-109">Usuwa z IotHub "myiothub" nazwę użytkownika o nazwie "".</span><span class="sxs-lookup"><span data-stu-id="d7de4-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d7de4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7de4-110">PARAMETERS</span></span>

### <span data-ttu-id="d7de4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7de4-111">-DefaultProfile</span></span>
<span data-ttu-id="d7de4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7de4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7de4-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="d7de4-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="d7de4-114">Nazwa odbiorcy EventHub.</span><span class="sxs-lookup"><span data-stu-id="d7de4-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="d7de4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7de4-115">-Name</span></span>
<span data-ttu-id="d7de4-116">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="d7de4-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="d7de4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7de4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7de4-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d7de4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d7de4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7de4-119">-Confirm</span></span>
<span data-ttu-id="d7de4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7de4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7de4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7de4-121">-WhatIf</span></span>
<span data-ttu-id="d7de4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7de4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7de4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7de4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7de4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7de4-124">CommonParameters</span></span>
<span data-ttu-id="d7de4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7de4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7de4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7de4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7de4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7de4-127">INPUTS</span></span>

### <span data-ttu-id="d7de4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d7de4-128">System.String</span></span>

## <span data-ttu-id="d7de4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7de4-129">OUTPUTS</span></span>

### <span data-ttu-id="d7de4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d7de4-130">System.String</span></span>

## <span data-ttu-id="d7de4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7de4-131">NOTES</span></span>

## <span data-ttu-id="d7de4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7de4-132">RELATED LINKS</span></span>
