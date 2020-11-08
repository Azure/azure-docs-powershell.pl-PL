---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049364"
---
# <span data-ttu-id="20c74-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="20c74-101">Search-AzGraph</span></span>

## <span data-ttu-id="20c74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20c74-102">SYNOPSIS</span></span>
<span data-ttu-id="20c74-103">Wysyła zapytanie dotyczące zasobów zarządzanych przez Menedżera zasobów Azure.</span><span class="sxs-lookup"><span data-stu-id="20c74-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="20c74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20c74-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c74-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20c74-105">DESCRIPTION</span></span>
<span data-ttu-id="20c74-106">Dowiedz się więcej na temat składni kwerendy: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="20c74-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="20c74-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20c74-107">EXAMPLES</span></span>

### <span data-ttu-id="20c74-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20c74-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


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

<span data-ttu-id="20c74-109">Zapytanie zasobów prostych żądających podzestawu pól zasobów.</span><span class="sxs-lookup"><span data-stu-id="20c74-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="20c74-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="20c74-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="20c74-111">Złożona kwerenda w zasobach, która zawiera zaznaczenie pól, filtrowanie i podsumowywanie.</span><span class="sxs-lookup"><span data-stu-id="20c74-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="20c74-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="20c74-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="20c74-113">Kwerenda zawierająca wszystkie maszyny wirtualne, które nie używają zarządzanych dysków i obejmuje imiona i nazwiska wyświetlania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="20c74-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="20c74-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="20c74-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="20c74-115">Kwerenda wyświetlająca liczbę zasobów według dzierżaw i nazw wyświetlanych w abonamentach.</span><span class="sxs-lookup"><span data-stu-id="20c74-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="20c74-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20c74-116">PARAMETERS</span></span>

### <span data-ttu-id="20c74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c74-117">-DefaultProfile</span></span>
<span data-ttu-id="20c74-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20c74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c74-119">-Query</span><span class="sxs-lookup"><span data-stu-id="20c74-119">-Query</span></span>
<span data-ttu-id="20c74-120">Kwerenda wykresu zasobów.</span><span class="sxs-lookup"><span data-stu-id="20c74-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="20c74-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="20c74-121">-Subscription</span></span>
<span data-ttu-id="20c74-122">Abonamentów, dla których ma zostać uruchomiony program Query.</span><span class="sxs-lookup"><span data-stu-id="20c74-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="20c74-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="20c74-123">-Skip</span></span>
<span data-ttu-id="20c74-124">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="20c74-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="20c74-125">-First</span><span class="sxs-lookup"><span data-stu-id="20c74-125">-First</span></span>
<span data-ttu-id="20c74-126">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="20c74-126">The maximum number of objects to return.</span></span> <span data-ttu-id="20c74-127">Dozwolone wartości: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="20c74-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="20c74-128">Wartość domyślna to 100.</span><span class="sxs-lookup"><span data-stu-id="20c74-128">Default value is 100.</span></span>

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

### <span data-ttu-id="20c74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c74-129">CommonParameters</span></span>
<span data-ttu-id="20c74-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c74-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c74-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c74-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20c74-132">INPUTS</span></span>

### <span data-ttu-id="20c74-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="20c74-133">None</span></span>

## <span data-ttu-id="20c74-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20c74-134">OUTPUTS</span></span>

### <span data-ttu-id="20c74-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="20c74-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="20c74-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20c74-136">NOTES</span></span>

## <span data-ttu-id="20c74-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20c74-137">RELATED LINKS</span></span>
