---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 5f4324ab7a27b711d33042eede5c3b88d38c4511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542584"
---
# <span data-ttu-id="9f2e3-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9f2e3-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="9f2e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f2e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2e3-103">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f2e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f2e3-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9f2e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f2e3-106">Usuwa odbiorcę eventhub.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="9f2e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f2e3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f2e3-108">Przykład 1 Usuwanie z centrum telemetrycznego tej samej firmy eventhub</span><span class="sxs-lookup"><span data-stu-id="9f2e3-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="9f2e3-109">Usuwa z IotHub "myiothub" nazwę użytkownika o nazwie "".</span><span class="sxs-lookup"><span data-stu-id="9f2e3-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9f2e3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f2e3-110">PARAMETERS</span></span>

### <span data-ttu-id="9f2e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2e3-111">-DefaultProfile</span></span>
<span data-ttu-id="9f2e3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9f2e3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2e3-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="9f2e3-114">Nazwa odbiorcy EventHub.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="9f2e3-115">-EventHubEndpointName</span></span>
<span data-ttu-id="9f2e3-116">Nazwa punktu końcowego EventHub.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="9f2e3-117">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="9f2e3-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f2e3-118">-Name</span></span>
<span data-ttu-id="9f2e3-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="9f2e3-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f2e3-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9f2e3-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f2e3-122">-Confirm</span></span>
<span data-ttu-id="9f2e3-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2e3-124">-WhatIf</span></span>
<span data-ttu-id="9f2e3-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f2e3-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2e3-127">CommonParameters</span></span>
<span data-ttu-id="9f2e3-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f2e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2e3-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f2e3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2e3-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f2e3-130">INPUTS</span></span>

### <span data-ttu-id="9f2e3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9f2e3-131">System.String</span></span>

## <span data-ttu-id="9f2e3-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f2e3-132">OUTPUTS</span></span>

### <span data-ttu-id="9f2e3-133">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9f2e3-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9f2e3-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f2e3-134">NOTES</span></span>

## <span data-ttu-id="9f2e3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f2e3-135">RELATED LINKS</span></span>

