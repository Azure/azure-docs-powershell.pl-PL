---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 7da36f401647a4e020097eb2cfe6690aa1327755
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891373"
---
# <span data-ttu-id="f92c3-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f92c3-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="f92c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f92c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f92c3-103">Pobiera metryki przydziału dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="f92c3-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f92c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f92c3-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f92c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f92c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f92c3-106">Pobiera metryki przydziału dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="f92c3-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f92c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f92c3-107">EXAMPLES</span></span>

### <span data-ttu-id="f92c3-108">Przykład 1 pobieranie metryki przydziału</span><span class="sxs-lookup"><span data-stu-id="f92c3-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f92c3-109">Pobiera informacje metryki przydziału dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f92c3-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f92c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f92c3-110">PARAMETERS</span></span>

### <span data-ttu-id="f92c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92c3-111">-DefaultProfile</span></span>
<span data-ttu-id="f92c3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f92c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f92c3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f92c3-113">-Name</span></span>
<span data-ttu-id="f92c3-114">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f92c3-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f92c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f92c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="f92c3-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f92c3-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f92c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92c3-117">CommonParameters</span></span>
<span data-ttu-id="f92c3-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f92c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92c3-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f92c3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92c3-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f92c3-120">INPUTS</span></span>

### <span data-ttu-id="f92c3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f92c3-121">System.String</span></span>

## <span data-ttu-id="f92c3-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f92c3-122">OUTPUTS</span></span>

### <span data-ttu-id="f92c3-123">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f92c3-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="f92c3-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f92c3-124">NOTES</span></span>

## <span data-ttu-id="f92c3-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f92c3-125">RELATED LINKS</span></span>
