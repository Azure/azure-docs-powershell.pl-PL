---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705248"
---
# <span data-ttu-id="91bbc-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="91bbc-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="91bbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="91bbc-103">Pobiera wszystkie consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="91bbc-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="91bbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91bbc-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91bbc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="91bbc-106">Pobiera wszystkie consumergroups eventhub dla różnych EventHubs używanych przez IotHub.</span><span class="sxs-lookup"><span data-stu-id="91bbc-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="91bbc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91bbc-107">EXAMPLES</span></span>

### <span data-ttu-id="91bbc-108">Przykład 1 pobiera wszystkie consumergroups eventhub dla telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="91bbc-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="91bbc-109">Pobiera wszystkie consumergroups eventhub dla składnika eventhub dla iothub o nazwie myiothub</span><span class="sxs-lookup"><span data-stu-id="91bbc-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="91bbc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91bbc-110">PARAMETERS</span></span>

### <span data-ttu-id="91bbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bbc-111">-DefaultProfile</span></span>
<span data-ttu-id="91bbc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="91bbc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91bbc-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="91bbc-113">-EventHubEndpointName</span></span>
<span data-ttu-id="91bbc-114">Nazwa punktu końcowego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="91bbc-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="91bbc-115">Możliwe wartości zdarzenia, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="91bbc-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="91bbc-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91bbc-116">-Name</span></span>
<span data-ttu-id="91bbc-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="91bbc-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="91bbc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91bbc-118">-ResourceGroupName</span></span>
<span data-ttu-id="91bbc-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="91bbc-119">Resource Group Name</span></span>

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

### <span data-ttu-id="91bbc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bbc-120">CommonParameters</span></span>
<span data-ttu-id="91bbc-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91bbc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bbc-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91bbc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bbc-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91bbc-123">INPUTS</span></span>

### <span data-ttu-id="91bbc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="91bbc-124">System.String</span></span>

## <span data-ttu-id="91bbc-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91bbc-125">OUTPUTS</span></span>

### <span data-ttu-id="91bbc-126">Microsoft. Azure. Commands. Management. IotHub. models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="91bbc-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="91bbc-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91bbc-127">NOTES</span></span>

## <span data-ttu-id="91bbc-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91bbc-128">RELATED LINKS</span></span>
