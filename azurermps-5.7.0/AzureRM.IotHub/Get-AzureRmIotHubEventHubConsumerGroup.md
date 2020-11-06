---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 62704390e28f6f6a256b2202a61d1e400de7f7e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545680"
---
# <span data-ttu-id="efc8c-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="efc8c-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="efc8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="efc8c-103">Pobiera wszystkie consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="efc8c-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efc8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efc8c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="efc8c-105">DESCRIPTION</span></span>
<span data-ttu-id="efc8c-106">Pobiera wszystkie consumergroups eventhub dla różnych EventHubs używanych przez IotHub.</span><span class="sxs-lookup"><span data-stu-id="efc8c-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="efc8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efc8c-107">EXAMPLES</span></span>

### <span data-ttu-id="efc8c-108">Przykład 1 pobiera wszystkie consumergroups eventhub dla telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="efc8c-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="efc8c-109">Pobiera wszystkie consumergroups eventhub dla składnika eventhub dla iothub o nazwie myiothub</span><span class="sxs-lookup"><span data-stu-id="efc8c-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="efc8c-110">Przykład 2 pobiera wszystkie consumergroups eventhub dla operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="efc8c-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="efc8c-111">Pobiera wszystkie consumergroups eventhub dla operationsMonitoringEvents eventhub dla iothub o nazwie myiothub</span><span class="sxs-lookup"><span data-stu-id="efc8c-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="efc8c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efc8c-112">PARAMETERS</span></span>

### <span data-ttu-id="efc8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc8c-113">-DefaultProfile</span></span>
<span data-ttu-id="efc8c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="efc8c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efc8c-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="efc8c-115">-EventHubEndpointName</span></span>
<span data-ttu-id="efc8c-116">Nazwa punktu końcowego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="efc8c-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="efc8c-117">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="efc8c-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc8c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="efc8c-118">-Name</span></span>
<span data-ttu-id="efc8c-119">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="efc8c-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="efc8c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc8c-120">-ResourceGroupName</span></span>
<span data-ttu-id="efc8c-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="efc8c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="efc8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc8c-122">CommonParameters</span></span>
<span data-ttu-id="efc8c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc8c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc8c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc8c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efc8c-125">INPUTS</span></span>

### <span data-ttu-id="efc8c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="efc8c-126">System.String</span></span>

## <span data-ttu-id="efc8c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efc8c-127">OUTPUTS</span></span>

### <span data-ttu-id="efc8c-128">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="efc8c-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="efc8c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efc8c-129">NOTES</span></span>

## <span data-ttu-id="efc8c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efc8c-130">RELATED LINKS</span></span>

