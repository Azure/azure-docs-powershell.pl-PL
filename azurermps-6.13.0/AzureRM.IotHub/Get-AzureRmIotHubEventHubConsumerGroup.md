---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 507787df7215efcd1b275f481b638aa80f979498
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718868"
---
# <span data-ttu-id="6bbf8-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6bbf8-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="6bbf8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbf8-103">Pobiera wszystkie consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bbf8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bbf8-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bbf8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6bbf8-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbf8-106">Pobiera wszystkie consumergroups eventhub dla różnych EventHubs używanych przez IotHub.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="6bbf8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bbf8-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbf8-108">Przykład 1 pobiera wszystkie consumergroups eventhub dla telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="6bbf8-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="6bbf8-109">Pobiera wszystkie consumergroups eventhub dla składnika eventhub dla iothub o nazwie myiothub</span><span class="sxs-lookup"><span data-stu-id="6bbf8-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="6bbf8-110">Przykład 2 pobiera wszystkie consumergroups eventhub dla operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="6bbf8-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="6bbf8-111">Pobiera wszystkie consumergroups eventhub dla operationsMonitoringEvents eventhub dla iothub o nazwie myiothub</span><span class="sxs-lookup"><span data-stu-id="6bbf8-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="6bbf8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bbf8-112">PARAMETERS</span></span>

### <span data-ttu-id="6bbf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbf8-113">-DefaultProfile</span></span>
<span data-ttu-id="6bbf8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6bbf8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bbf8-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="6bbf8-115">-EventHubEndpointName</span></span>
<span data-ttu-id="6bbf8-116">Nazwa punktu końcowego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="6bbf8-117">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="6bbf8-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbf8-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bbf8-118">-Name</span></span>
<span data-ttu-id="6bbf8-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="6bbf8-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="6bbf8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bbf8-120">-ResourceGroupName</span></span>
<span data-ttu-id="6bbf8-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6bbf8-121">Resource Group Name</span></span>

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

### <span data-ttu-id="6bbf8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbf8-122">CommonParameters</span></span>
<span data-ttu-id="6bbf8-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbf8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbf8-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbf8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbf8-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bbf8-125">INPUTS</span></span>

### <span data-ttu-id="6bbf8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6bbf8-126">System.String</span></span>

## <span data-ttu-id="6bbf8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bbf8-127">OUTPUTS</span></span>

### <span data-ttu-id="6bbf8-128">Microsoft. Azure. Commands. Management. IotHub. models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="6bbf8-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="6bbf8-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bbf8-129">NOTES</span></span>

## <span data-ttu-id="6bbf8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bbf8-130">RELATED LINKS</span></span>
