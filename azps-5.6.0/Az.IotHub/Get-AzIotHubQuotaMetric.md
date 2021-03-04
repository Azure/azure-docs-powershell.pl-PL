---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 70e63723bd9647f003082813cd680a84ae5638c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987918"
---
# <span data-ttu-id="771dc-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="771dc-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="771dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="771dc-102">SYNOPSIS</span></span>
<span data-ttu-id="771dc-103">Pobiera metryki przydziału dla aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="771dc-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="771dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="771dc-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="771dc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="771dc-105">DESCRIPTION</span></span>
<span data-ttu-id="771dc-106">Pobiera metryki przydziału dla aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="771dc-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="771dc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="771dc-107">EXAMPLES</span></span>

### <span data-ttu-id="771dc-108">Przykład 1. Uzyskiwanie metryk przydziału</span><span class="sxs-lookup"><span data-stu-id="771dc-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="771dc-109">Pobiera informacje o metryki przydziału dla usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="771dc-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="771dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="771dc-110">PARAMETERS</span></span>

### <span data-ttu-id="771dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771dc-111">-DefaultProfile</span></span>
<span data-ttu-id="771dc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="771dc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="771dc-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="771dc-113">-Name</span></span>
<span data-ttu-id="771dc-114">Nazwa centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="771dc-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="771dc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771dc-115">-ResourceGroupName</span></span>
<span data-ttu-id="771dc-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="771dc-116">Resource Group Name</span></span>

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

### <span data-ttu-id="771dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771dc-117">CommonParameters</span></span>
<span data-ttu-id="771dc-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="771dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771dc-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771dc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771dc-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="771dc-120">INPUTS</span></span>

### <span data-ttu-id="771dc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="771dc-121">System.String</span></span>

## <span data-ttu-id="771dc-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="771dc-122">OUTPUTS</span></span>

### <span data-ttu-id="771dc-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="771dc-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="771dc-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="771dc-124">NOTES</span></span>

## <span data-ttu-id="771dc-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="771dc-125">RELATED LINKS</span></span>
