---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 20c142df2a3df0ea6448c2bcb58ad47169d9e483
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180091"
---
# <span data-ttu-id="8a81a-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="8a81a-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="8a81a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a81a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a81a-103">Uzyskiwanie informacji o dostępnej wersji SKU dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="8a81a-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="8a81a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a81a-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a81a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a81a-105">DESCRIPTION</span></span>
<span data-ttu-id="8a81a-106">Uzyskiwanie informacji o dostępnej wersji SKU dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="8a81a-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="8a81a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a81a-107">EXAMPLES</span></span>

### <span data-ttu-id="8a81a-108">Przykład 1. Uzyskiwanie funkcji lokalizacji według nazwy lokalizacji</span><span class="sxs-lookup"><span data-stu-id="8a81a-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerLocationBasedCapability -Location westus2
"Please refer to https://aka.ms/mysql-pricing for pricing details"

SKU               Tier            Memory vCore
---               ----            ------ -----
Standard_B1s      Burstable         1024     1
Standard_B1ms     Burstable         2048     1
Standard_B2s      Burstable         2048     2
Standard_D2ds_v4  GeneralPurpose    4096     2
Standard_D4ds_v4  GeneralPurpose    4096     4
Standard_D8ds_v4  GeneralPurpose    4096     8
Standard_D16ds_v4 GeneralPurpose    4096    16
Standard_D32ds_v4 GeneralPurpose    4096    32
Standard_D48ds_v4 GeneralPurpose    4096    48
Standard_D64ds_v4 GeneralPurpose    4096    64
Standard_E2ds_v4  MemoryOptimized   8192     2
Standard_E4ds_v4  MemoryOptimized   8192     4
Standard_E8ds_v4  MemoryOptimized   8192     8
Standard_E16ds_v4 MemoryOptimized   8192    16
Standard_E32ds_v4 MemoryOptimized   8192    32
Standard_E48ds_v4 MemoryOptimized   8192    48
Standard_E64ds_v4 MemoryOptimized   8192    64

```

<span data-ttu-id="8a81a-109">To polecenie cmdlet wyświetla podstawowe informacje o wersji SKU podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8a81a-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="8a81a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a81a-110">PARAMETERS</span></span>

### <span data-ttu-id="8a81a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a81a-111">-DefaultProfile</span></span>
<span data-ttu-id="8a81a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a81a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a81a-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8a81a-113">-Location</span></span>
<span data-ttu-id="8a81a-114">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8a81a-114">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a81a-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a81a-115">-SubscriptionId</span></span>
<span data-ttu-id="8a81a-116">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8a81a-116">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a81a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a81a-117">CommonParameters</span></span>
<span data-ttu-id="8a81a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a81a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a81a-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a81a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a81a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a81a-120">INPUTS</span></span>

## <span data-ttu-id="8a81a-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a81a-121">OUTPUTS</span></span>

### <span data-ttu-id="8a81a-122">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20200701Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="8a81a-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="8a81a-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a81a-123">NOTES</span></span>

<span data-ttu-id="8a81a-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8a81a-124">ALIASES</span></span>

## <span data-ttu-id="8a81a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a81a-125">RELATED LINKS</span></span>

