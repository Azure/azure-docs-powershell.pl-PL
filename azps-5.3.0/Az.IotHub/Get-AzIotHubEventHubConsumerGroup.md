---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503417"
---
# <span data-ttu-id="932e2-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="932e2-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="932e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="932e2-102">SYNOPSIS</span></span>
<span data-ttu-id="932e2-103">Pobiera wszystkie consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="932e2-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="932e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="932e2-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="932e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="932e2-105">DESCRIPTION</span></span>
<span data-ttu-id="932e2-106">Pobiera wszystkie consumergroups eventhub dla różnych EventHubs używanych przez IotHub.</span><span class="sxs-lookup"><span data-stu-id="932e2-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="932e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="932e2-107">EXAMPLES</span></span>

### <span data-ttu-id="932e2-108">Przykład 1 pobiera wszystkie consumergroups eventhub dla telemetrii eventhub</span><span class="sxs-lookup"><span data-stu-id="932e2-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="932e2-109">Pobiera wszystkie consumergroups eventhub dla składnika eventhub dla iothub o nazwie myiothub</span><span class="sxs-lookup"><span data-stu-id="932e2-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="932e2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="932e2-110">PARAMETERS</span></span>

### <span data-ttu-id="932e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932e2-111">-DefaultProfile</span></span>
<span data-ttu-id="932e2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="932e2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="932e2-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="932e2-113">-Name</span></span>
<span data-ttu-id="932e2-114">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="932e2-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="932e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="932e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="932e2-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="932e2-116">Resource Group Name</span></span>

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

### <span data-ttu-id="932e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932e2-117">CommonParameters</span></span>
<span data-ttu-id="932e2-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="932e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932e2-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="932e2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932e2-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="932e2-120">INPUTS</span></span>

### <span data-ttu-id="932e2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="932e2-121">System.String</span></span>

## <span data-ttu-id="932e2-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="932e2-122">OUTPUTS</span></span>

### <span data-ttu-id="932e2-123">Microsoft. Azure. Commands. Management. IotHub. models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="932e2-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="932e2-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="932e2-124">NOTES</span></span>

## <span data-ttu-id="932e2-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="932e2-125">RELATED LINKS</span></span>
