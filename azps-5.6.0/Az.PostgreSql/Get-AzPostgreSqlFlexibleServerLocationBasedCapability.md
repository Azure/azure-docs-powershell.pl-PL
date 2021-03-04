---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: efe45da6cd5426fda3b301efd4daf2ef532e4c02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953738"
---
# <span data-ttu-id="4f5f8-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="4f5f8-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="4f5f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5f8-103">Uzyskiwanie informacji o dostępnej wersji SKU dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="4f5f8-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="4f5f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f5f8-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4f5f8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5f8-106">Uzyskiwanie informacji o dostępnej wersji SKU dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="4f5f8-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="4f5f8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f5f8-107">EXAMPLES</span></span>

### <span data-ttu-id="4f5f8-108">Przykład 1. Uzyskiwanie funkcji lokalizacji według nazwy lokalizacji</span><span class="sxs-lookup"><span data-stu-id="4f5f8-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location eastus

SKU              Tier            Memory vCore
---              ----            ------ -----
Standard_B1ms    Burstable         2048     1
Standard_B2s     Burstable         2048     2
Standard_D2s_v3  GeneralPurpose    4096     2
Standard_D4s_v3  GeneralPurpose    4096     4
Standard_D8s_v3  GeneralPurpose    4096     8
Standard_D16s_v3 GeneralPurpose    4096    16
Standard_D32s_v3 GeneralPurpose    4096    32
Standard_D48s_v3 GeneralPurpose    4096    48
Standard_D64s_v3 GeneralPurpose    4096    64
Standard_E2s_v3  MemoryOptimized   8192     2
Standard_E4s_v3  MemoryOptimized   8192     4
Standard_E8s_v3  MemoryOptimized   8192     8
Standard_E16s_v3 MemoryOptimized   8192    16
Standard_E32s_v3 MemoryOptimized   8192    32
Standard_E48s_v3 MemoryOptimized   8192    48
Standard_E64s_v3 MemoryOptimized   6912    64
```

<span data-ttu-id="4f5f8-109">To polecenie cmdlet wyświetla podstawowe informacje o wersji SKU podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4f5f8-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="4f5f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f5f8-110">PARAMETERS</span></span>

### <span data-ttu-id="4f5f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5f8-111">-DefaultProfile</span></span>
<span data-ttu-id="4f5f8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5f8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f5f8-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4f5f8-113">-Location</span></span>
<span data-ttu-id="4f5f8-114">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4f5f8-114">The name of the location.</span></span>

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

### <span data-ttu-id="4f5f8-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f5f8-115">-SubscriptionId</span></span>
<span data-ttu-id="4f5f8-116">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4f5f8-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4f5f8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5f8-117">CommonParameters</span></span>
<span data-ttu-id="4f5f8-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5f8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5f8-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f5f8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5f8-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f5f8-120">INPUTS</span></span>

## <span data-ttu-id="4f5f8-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f5f8-121">OUTPUTS</span></span>

### <span data-ttu-id="4f5f8-122">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="4f5f8-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="4f5f8-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f5f8-123">NOTES</span></span>

<span data-ttu-id="4f5f8-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4f5f8-124">ALIASES</span></span>

## <span data-ttu-id="4f5f8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f5f8-125">RELATED LINKS</span></span>

