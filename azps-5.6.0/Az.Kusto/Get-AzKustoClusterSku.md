---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 4b72dde837122329a4761fc0c2c1a0120914e60f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964465"
---
# <span data-ttu-id="8ee9b-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="8ee9b-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="8ee9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee9b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee9b-103">Wyświetla listę kwalifikujących się jednostki SKU dla dostawcy zasobów Kusto.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="8ee9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ee9b-104">SYNTAX</span></span>

### <span data-ttu-id="8ee9b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8ee9b-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8ee9b-106">Lista1</span><span class="sxs-lookup"><span data-stu-id="8ee9b-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8ee9b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ee9b-107">DESCRIPTION</span></span>
<span data-ttu-id="8ee9b-108">Wyświetla listę kwalifikujących się jednostki SKU dla dostawcy zasobów Kusto.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="8ee9b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ee9b-109">EXAMPLES</span></span>

### <span data-ttu-id="8ee9b-110">Przykład 1. Lista kwalifikujących się jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="8ee9b-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="8ee9b-111">Powyższe polecenie wyświetla listę uprawnionych jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="8ee9b-112">Przykład 2. Lista kwalifikujących się jednostki SKU dla określonego klastra</span><span class="sxs-lookup"><span data-stu-id="8ee9b-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="8ee9b-113">Powyższe polecenie wyświetla listę kwalifikujących się jednostki SKU dla określonego klastra</span><span class="sxs-lookup"><span data-stu-id="8ee9b-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="8ee9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee9b-114">PARAMETERS</span></span>

### <span data-ttu-id="8ee9b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8ee9b-115">-ClusterName</span></span>
<span data-ttu-id="8ee9b-116">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee9b-117">-DefaultProfile</span></span>
<span data-ttu-id="8ee9b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee9b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee9b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8ee9b-120">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee9b-121">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ee9b-121">-SubscriptionId</span></span>
<span data-ttu-id="8ee9b-122">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8ee9b-123">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8ee9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee9b-124">CommonParameters</span></span>
<span data-ttu-id="8ee9b-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee9b-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee9b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee9b-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee9b-127">INPUTS</span></span>

## <span data-ttu-id="8ee9b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee9b-128">OUTPUTS</span></span>

### <span data-ttu-id="8ee9b-129">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="8ee9b-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="8ee9b-130">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="8ee9b-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="8ee9b-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ee9b-131">NOTES</span></span>

<span data-ttu-id="8ee9b-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8ee9b-132">ALIASES</span></span>

## <span data-ttu-id="8ee9b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ee9b-133">RELATED LINKS</span></span>

