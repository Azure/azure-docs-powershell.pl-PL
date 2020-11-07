---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718862"
---
# <span data-ttu-id="09c04-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="09c04-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="09c04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09c04-102">SYNOPSIS</span></span>
<span data-ttu-id="09c04-103">Pobiera metryki przydziału dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="09c04-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09c04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09c04-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09c04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09c04-105">DESCRIPTION</span></span>
<span data-ttu-id="09c04-106">Pobiera metryki przydziału dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="09c04-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="09c04-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09c04-107">EXAMPLES</span></span>

### <span data-ttu-id="09c04-108">Przykład 1 pobieranie metryki przydziału</span><span class="sxs-lookup"><span data-stu-id="09c04-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="09c04-109">Pobiera informacje metryki przydziału dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="09c04-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="09c04-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09c04-110">PARAMETERS</span></span>

### <span data-ttu-id="09c04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c04-111">-DefaultProfile</span></span>
<span data-ttu-id="09c04-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="09c04-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09c04-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09c04-113">-Name</span></span>
<span data-ttu-id="09c04-114">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="09c04-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="09c04-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c04-115">-ResourceGroupName</span></span>
<span data-ttu-id="09c04-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="09c04-116">Resource Group Name</span></span>

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

### <span data-ttu-id="09c04-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c04-117">CommonParameters</span></span>
<span data-ttu-id="09c04-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c04-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c04-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c04-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c04-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09c04-120">INPUTS</span></span>

### <span data-ttu-id="09c04-121">System. String</span><span class="sxs-lookup"><span data-stu-id="09c04-121">System.String</span></span>

## <span data-ttu-id="09c04-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09c04-122">OUTPUTS</span></span>

### <span data-ttu-id="09c04-123">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="09c04-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="09c04-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09c04-124">NOTES</span></span>

## <span data-ttu-id="09c04-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09c04-125">RELATED LINKS</span></span>
