---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e96d4fa13dc1b479c37b56cb3887b6d519df24f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000106"
---
# <span data-ttu-id="9ef38-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="9ef38-101">Search-AzGraph</span></span>

## <span data-ttu-id="9ef38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef38-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef38-103">Wysyła zapytania do zasobów zarządzanych przez usługę Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9ef38-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="9ef38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9ef38-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ef38-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9ef38-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef38-106">Więcej informacji o składni zapytania można uzyskać tutaj: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="9ef38-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="9ef38-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9ef38-107">EXAMPLES</span></span>

### <span data-ttu-id="9ef38-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ef38-108">Example 1</span></span>
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

<span data-ttu-id="9ef38-109">Kwerenda z prostymi zasobami z żądaniem podzbioru pól zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ef38-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="9ef38-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9ef38-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="9ef38-111">Złożone zapytanie dotyczące zasobów zawierające wybór pól, filtrowanie i podsumowywanie.</span><span class="sxs-lookup"><span data-stu-id="9ef38-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="9ef38-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9ef38-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="9ef38-113">Zapytanie zawierające wszystkie maszyny wirtualne, które nie są używające zarządzanych dysków i zawiera nazwy wyświetlane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9ef38-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="9ef38-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="9ef38-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="9ef38-115">Kwerenda wyświetlająca liczbę zasobów według dzierżawy i subskrypcji, wyświetlające nazwy.</span><span class="sxs-lookup"><span data-stu-id="9ef38-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="9ef38-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ef38-116">PARAMETERS</span></span>

### <span data-ttu-id="9ef38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef38-117">-DefaultProfile</span></span>
<span data-ttu-id="9ef38-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef38-119">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="9ef38-119">-Query</span></span>
<span data-ttu-id="9ef38-120">Zapytanie Wykres zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ef38-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="9ef38-121">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="9ef38-121">-Subscription</span></span>
<span data-ttu-id="9ef38-122">Subskrypcje, dla których ma być uruchamiane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="9ef38-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="9ef38-123">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="9ef38-123">-Skip</span></span>
<span data-ttu-id="9ef38-124">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="9ef38-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="9ef38-125">— najpierw</span><span class="sxs-lookup"><span data-stu-id="9ef38-125">-First</span></span>
<span data-ttu-id="9ef38-126">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="9ef38-126">The maximum number of objects to return.</span></span> <span data-ttu-id="9ef38-127">Dozwolone wartości: 1–5000.</span><span class="sxs-lookup"><span data-stu-id="9ef38-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="9ef38-128">Wartość domyślna to 100.</span><span class="sxs-lookup"><span data-stu-id="9ef38-128">Default value is 100.</span></span>

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

### <span data-ttu-id="9ef38-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef38-129">CommonParameters</span></span>
<span data-ttu-id="9ef38-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef38-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef38-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef38-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef38-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ef38-132">INPUTS</span></span>

### <span data-ttu-id="9ef38-133">Brak</span><span class="sxs-lookup"><span data-stu-id="9ef38-133">None</span></span>

## <span data-ttu-id="9ef38-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ef38-134">OUTPUTS</span></span>

### <span data-ttu-id="9ef38-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="9ef38-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9ef38-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9ef38-136">NOTES</span></span>

## <span data-ttu-id="9ef38-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ef38-137">RELATED LINKS</span></span>
