---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185666"
---
# <span data-ttu-id="bdc4f-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="bdc4f-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="bdc4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc4f-103">Pobiera metryki przydziału dla aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="bdc4f-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="bdc4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdc4f-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdc4f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdc4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc4f-106">Pobiera metryki przydziału dla aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="bdc4f-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="bdc4f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdc4f-107">EXAMPLES</span></span>

### <span data-ttu-id="bdc4f-108">Przykład 1. Uzyskiwanie metryk przydziału</span><span class="sxs-lookup"><span data-stu-id="bdc4f-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bdc4f-109">Pobiera informacje o metryki przydziału dla usługi IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bdc4f-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bdc4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdc4f-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc4f-111">-DefaultProfile</span></span>
<span data-ttu-id="bdc4f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bdc4f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdc4f-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bdc4f-113">-Name</span></span>
<span data-ttu-id="bdc4f-114">Nazwa centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="bdc4f-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="bdc4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="bdc4f-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bdc4f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="bdc4f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc4f-117">CommonParameters</span></span>
<span data-ttu-id="bdc4f-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc4f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc4f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc4f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc4f-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc4f-120">INPUTS</span></span>

### <span data-ttu-id="bdc4f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc4f-121">System.String</span></span>

## <span data-ttu-id="bdc4f-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc4f-122">OUTPUTS</span></span>

### <span data-ttu-id="bdc4f-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="bdc4f-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="bdc4f-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdc4f-124">NOTES</span></span>

## <span data-ttu-id="bdc4f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdc4f-125">RELATED LINKS</span></span>
