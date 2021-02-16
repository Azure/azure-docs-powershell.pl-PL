---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185699"
---
# <span data-ttu-id="07ec4-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="07ec4-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="07ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="07ec4-103">Pobiera wszystkie grupy klientów w usłudze EventHub.</span><span class="sxs-lookup"><span data-stu-id="07ec4-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="07ec4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07ec4-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ec4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="07ec4-105">DESCRIPTION</span></span>
<span data-ttu-id="07ec4-106">Pobiera wszystkie grupy klientów z usługi Eventhub dla różnychhub zdarzeń używanych przez usługę IotHub.</span><span class="sxs-lookup"><span data-stu-id="07ec4-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="07ec4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07ec4-107">EXAMPLES</span></span>

### <span data-ttu-id="07ec4-108">Przykład 1. Pobiera wszystkie grupy konsumenckie aplikacji Eventhub dla telemetrii</span><span class="sxs-lookup"><span data-stu-id="07ec4-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="07ec4-109">Pobiera wszystkie grupy użytkowników z aplikacji Eventhub dla telemetrii dla aplikacji iothub o nazwie myiothub.</span><span class="sxs-lookup"><span data-stu-id="07ec4-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="07ec4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07ec4-110">PARAMETERS</span></span>

### <span data-ttu-id="07ec4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ec4-111">-DefaultProfile</span></span>
<span data-ttu-id="07ec4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="07ec4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07ec4-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="07ec4-113">-Name</span></span>
<span data-ttu-id="07ec4-114">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="07ec4-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="07ec4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ec4-115">-ResourceGroupName</span></span>
<span data-ttu-id="07ec4-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="07ec4-116">Resource Group Name</span></span>

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

### <span data-ttu-id="07ec4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ec4-117">CommonParameters</span></span>
<span data-ttu-id="07ec4-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ec4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ec4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ec4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ec4-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07ec4-120">INPUTS</span></span>

### <span data-ttu-id="07ec4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="07ec4-121">System.String</span></span>

## <span data-ttu-id="07ec4-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07ec4-122">OUTPUTS</span></span>

### <span data-ttu-id="07ec4-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="07ec4-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="07ec4-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07ec4-124">NOTES</span></span>

## <span data-ttu-id="07ec4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07ec4-125">RELATED LINKS</span></span>
