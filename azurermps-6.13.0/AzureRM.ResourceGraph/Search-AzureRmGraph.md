---
external help file: Microsoft.Azure.Commands.ResourceGraph.dll-Help.xml
Module Name: AzureRM.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resourcegraph/search-azurermgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
ms.openlocfilehash: 900722c15d1c7a6560ba1f498b9dd0d3981f899a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549296"
---
# <span data-ttu-id="4ffbd-101">Search-AzureRmGraph</span><span class="sxs-lookup"><span data-stu-id="4ffbd-101">Search-AzureRmGraph</span></span>

## <span data-ttu-id="4ffbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ffbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffbd-103">Wysyła zapytanie dotyczące zasobów zarządzanych przez Menedżera zasobów Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-103">Queries the resources managed by Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ffbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ffbd-104">SYNTAX</span></span>

```
Search-AzureRmGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ffbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ffbd-105">DESCRIPTION</span></span>
<span data-ttu-id="4ffbd-106">Dowiedz się więcej na temat składni kwerendy: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="4ffbd-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="4ffbd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ffbd-107">EXAMPLES</span></span>

### <span data-ttu-id="4ffbd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ffbd-108">Example 1</span></span>
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="4ffbd-109">Zapytanie zasobów prostych żądających podzestawu pól zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="4ffbd-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4ffbd-110">Example 2</span></span>
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="4ffbd-111">Złożona kwerenda w zasobach, która zawiera zaznaczenie pól, filtrowanie i podsumowywanie.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="4ffbd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ffbd-112">PARAMETERS</span></span>

### <span data-ttu-id="4ffbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffbd-113">-DefaultProfile</span></span>
<span data-ttu-id="4ffbd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ffbd-115">-Query</span><span class="sxs-lookup"><span data-stu-id="4ffbd-115">-Query</span></span>
<span data-ttu-id="4ffbd-116">Kwerenda wykresu zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffbd-117">-Subscription</span><span class="sxs-lookup"><span data-stu-id="4ffbd-117">-Subscription</span></span>
<span data-ttu-id="4ffbd-118">Abonamentów, dla których ma zostać uruchomiony program Query.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffbd-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="4ffbd-119">-Skip</span></span>
<span data-ttu-id="4ffbd-120">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffbd-121">-First</span><span class="sxs-lookup"><span data-stu-id="4ffbd-121">-First</span></span>
<span data-ttu-id="4ffbd-122">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-122">The maximum number of objects to return.</span></span> <span data-ttu-id="4ffbd-123">Dozwolone wartości: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="4ffbd-124">Wartość domyślna to 100.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffbd-125">CommonParameters</span></span>
<span data-ttu-id="4ffbd-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ffbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ffbd-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffbd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffbd-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ffbd-128">INPUTS</span></span>

### <span data-ttu-id="4ffbd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4ffbd-129">System.String</span></span>

## <span data-ttu-id="4ffbd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ffbd-130">OUTPUTS</span></span>

### <span data-ttu-id="4ffbd-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4ffbd-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4ffbd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ffbd-132">NOTES</span></span>

## <span data-ttu-id="4ffbd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ffbd-133">RELATED LINKS</span></span>
