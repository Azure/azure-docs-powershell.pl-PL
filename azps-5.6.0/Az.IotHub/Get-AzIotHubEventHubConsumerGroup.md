---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988002"
---
# <span data-ttu-id="f5f0d-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f5f0d-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="f5f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f0d-103">Pobiera wszystkie grupy klientów w usłudze EventHub.</span><span class="sxs-lookup"><span data-stu-id="f5f0d-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="f5f0d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5f0d-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f0d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f0d-106">Pobiera wszystkie grupy klientów z usługi Eventhub dla różnychhub zdarzeń używanych przez usługę IotHub.</span><span class="sxs-lookup"><span data-stu-id="f5f0d-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="f5f0d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5f0d-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f0d-108">Przykład 1. Pobiera wszystkie grupy konsumenckie w aplikacji Eventhub dla telemetrii</span><span class="sxs-lookup"><span data-stu-id="f5f0d-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f5f0d-109">Pobiera wszystkie grupy użytkowników z aplikacji Eventhub dla telemetrii dla aplikacji iothub o nazwie myiothub.</span><span class="sxs-lookup"><span data-stu-id="f5f0d-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="f5f0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5f0d-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f0d-111">-DefaultProfile</span></span>
<span data-ttu-id="f5f0d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f5f0d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5f0d-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5f0d-113">-Name</span></span>
<span data-ttu-id="f5f0d-114">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="f5f0d-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="f5f0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5f0d-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f5f0d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f5f0d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f0d-117">CommonParameters</span></span>
<span data-ttu-id="f5f0d-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f0d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f0d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f0d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f0d-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f0d-120">INPUTS</span></span>

### <span data-ttu-id="f5f0d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f5f0d-121">System.String</span></span>

## <span data-ttu-id="f5f0d-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f0d-122">OUTPUTS</span></span>

### <span data-ttu-id="f5f0d-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="f5f0d-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="f5f0d-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5f0d-124">NOTES</span></span>

## <span data-ttu-id="f5f0d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5f0d-125">RELATED LINKS</span></span>
