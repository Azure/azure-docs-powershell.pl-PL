---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064436"
---
# <span data-ttu-id="a0ef5-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="a0ef5-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="a0ef5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ef5-103">Wyświetla listę kwalifikujących się jednostek SKU dla Kusto dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="a0ef5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0ef5-104">SYNTAX</span></span>

### <span data-ttu-id="a0ef5-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a0ef5-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0ef5-106">List1</span><span class="sxs-lookup"><span data-stu-id="a0ef5-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a0ef5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a0ef5-107">DESCRIPTION</span></span>
<span data-ttu-id="a0ef5-108">Wyświetla listę kwalifikujących się jednostek SKU dla Kusto dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="a0ef5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0ef5-109">EXAMPLES</span></span>

### <span data-ttu-id="a0ef5-110">Przykład 1: Lista kwalifikujących się jednostek SKU</span><span class="sxs-lookup"><span data-stu-id="a0ef5-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="a0ef5-111">Powyższe polecenie wyświetla listę kwalifikowanych jednostek SKU.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="a0ef5-112">Przykład 2: Wyświetla listę kwalifikowanych jednostek SKU dla określonego klastra</span><span class="sxs-lookup"><span data-stu-id="a0ef5-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="a0ef5-113">Powyższe polecenie wyświetla listę kwalifikowanych jednostek SKU dla określonego klastra</span><span class="sxs-lookup"><span data-stu-id="a0ef5-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="a0ef5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0ef5-114">PARAMETERS</span></span>

### <span data-ttu-id="a0ef5-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="a0ef5-115">-ClusterName</span></span>
<span data-ttu-id="a0ef5-116">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a0ef5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ef5-117">-DefaultProfile</span></span>
<span data-ttu-id="a0ef5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ef5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ef5-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0ef5-120">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a0ef5-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a0ef5-121">-SubscriptionId</span></span>
<span data-ttu-id="a0ef5-122">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0ef5-123">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0ef5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ef5-124">CommonParameters</span></span>
<span data-ttu-id="a0ef5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ef5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ef5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0ef5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ef5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0ef5-127">INPUTS</span></span>

## <span data-ttu-id="a0ef5-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0ef5-128">OUTPUTS</span></span>

### <span data-ttu-id="a0ef5-129">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="a0ef5-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="a0ef5-130">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="a0ef5-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="a0ef5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0ef5-131">NOTES</span></span>

<span data-ttu-id="a0ef5-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a0ef5-132">ALIASES</span></span>

## <span data-ttu-id="a0ef5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0ef5-133">RELATED LINKS</span></span>

