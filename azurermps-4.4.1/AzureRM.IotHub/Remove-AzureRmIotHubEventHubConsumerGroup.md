---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553284"
---
# <span data-ttu-id="62ba0-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="62ba0-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="62ba0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="62ba0-103">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="62ba0-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ba0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62ba0-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ba0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="62ba0-106">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="62ba0-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="62ba0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="62ba0-108">Przykład 1 Usuwanie z centrum telemetrycznego tej samej firmy eventhub</span><span class="sxs-lookup"><span data-stu-id="62ba0-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="62ba0-109">Usuwa z IotHub "myiothub" nazwę użytkownika o nazwie "".</span><span class="sxs-lookup"><span data-stu-id="62ba0-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="62ba0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62ba0-110">PARAMETERS</span></span>

### <span data-ttu-id="62ba0-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="62ba0-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="62ba0-112">Nazwa odbiorcy EventHub.</span><span class="sxs-lookup"><span data-stu-id="62ba0-112">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="62ba0-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="62ba0-113">-EventHubEndpointName</span></span>
<span data-ttu-id="62ba0-114">Nazwa punktu końcowego EventHub.</span><span class="sxs-lookup"><span data-stu-id="62ba0-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="62ba0-115">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="62ba0-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="62ba0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62ba0-116">-Name</span></span>
<span data-ttu-id="62ba0-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="62ba0-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="62ba0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ba0-118">-ResourceGroupName</span></span>
<span data-ttu-id="62ba0-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="62ba0-119">Resource Group Name</span></span>

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

### <span data-ttu-id="62ba0-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62ba0-120">-Confirm</span></span>
<span data-ttu-id="62ba0-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ba0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ba0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ba0-122">-WhatIf</span></span>
<span data-ttu-id="62ba0-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ba0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ba0-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62ba0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ba0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ba0-125">-DefaultProfile</span></span>
<span data-ttu-id="62ba0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62ba0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ba0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ba0-127">CommonParameters</span></span>
<span data-ttu-id="62ba0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ba0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ba0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ba0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ba0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ba0-130">INPUTS</span></span>

### <span data-ttu-id="62ba0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="62ba0-131">System.String</span></span>

## <span data-ttu-id="62ba0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62ba0-132">OUTPUTS</span></span>

### <span data-ttu-id="62ba0-133">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="62ba0-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="62ba0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62ba0-134">NOTES</span></span>

## <span data-ttu-id="62ba0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ba0-135">RELATED LINKS</span></span>

