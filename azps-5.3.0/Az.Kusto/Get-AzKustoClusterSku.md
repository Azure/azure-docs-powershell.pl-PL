---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490222"
---
# <span data-ttu-id="375c3-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="375c3-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="375c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="375c3-102">SYNOPSIS</span></span>
<span data-ttu-id="375c3-103">Wyświetla listę kwalifikujących się jednostek SKU dla Kusto dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="375c3-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="375c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="375c3-104">SYNTAX</span></span>

### <span data-ttu-id="375c3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="375c3-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="375c3-106">List1</span><span class="sxs-lookup"><span data-stu-id="375c3-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="375c3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="375c3-107">DESCRIPTION</span></span>
<span data-ttu-id="375c3-108">Wyświetla listę kwalifikujących się jednostek SKU dla Kusto dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="375c3-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="375c3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="375c3-109">EXAMPLES</span></span>

### <span data-ttu-id="375c3-110">Przykład 1: Lista kwalifikujących się jednostek SKU</span><span class="sxs-lookup"><span data-stu-id="375c3-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="375c3-111">Powyższe polecenie wyświetla listę kwalifikowanych jednostek SKU.</span><span class="sxs-lookup"><span data-stu-id="375c3-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="375c3-112">Przykład 2: Wyświetla listę kwalifikowanych jednostek SKU dla określonego klastra</span><span class="sxs-lookup"><span data-stu-id="375c3-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="375c3-113">Powyższe polecenie wyświetla listę kwalifikowanych jednostek SKU dla określonego klastra</span><span class="sxs-lookup"><span data-stu-id="375c3-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="375c3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="375c3-114">PARAMETERS</span></span>

### <span data-ttu-id="375c3-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="375c3-115">-ClusterName</span></span>
<span data-ttu-id="375c3-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="375c3-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="375c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375c3-117">-DefaultProfile</span></span>
<span data-ttu-id="375c3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="375c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="375c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="375c3-120">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="375c3-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="375c3-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="375c3-121">-SubscriptionId</span></span>
<span data-ttu-id="375c3-122">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="375c3-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="375c3-123">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="375c3-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="375c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375c3-124">CommonParameters</span></span>
<span data-ttu-id="375c3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375c3-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="375c3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375c3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="375c3-127">INPUTS</span></span>

## <span data-ttu-id="375c3-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="375c3-128">OUTPUTS</span></span>

### <span data-ttu-id="375c3-129">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="375c3-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="375c3-130">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="375c3-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="375c3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="375c3-131">NOTES</span></span>

<span data-ttu-id="375c3-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="375c3-132">ALIASES</span></span>

## <span data-ttu-id="375c3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="375c3-133">RELATED LINKS</span></span>

