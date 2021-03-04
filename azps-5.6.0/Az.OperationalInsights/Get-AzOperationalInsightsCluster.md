---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: bc78b7d791d0988ee692c12537aed3207066ba26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997529"
---
# <span data-ttu-id="39f47-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="39f47-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="39f47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39f47-102">SYNOPSIS</span></span>
<span data-ttu-id="39f47-103">Uzyskiwanie lub lista klastrów</span><span class="sxs-lookup"><span data-stu-id="39f47-103">Get or list clusters</span></span>

## <span data-ttu-id="39f47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39f47-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39f47-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39f47-105">DESCRIPTION</span></span>
<span data-ttu-id="39f47-106">Uzyskiwanie lub lista klastrów, klastry list w grupie zasobów, gdy nie podano nazwy "-ClusterName", klastry list w ramach subskrypcji, gdy nie zostały podane wartości "-ClusterName" i "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="39f47-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="39f47-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39f47-107">EXAMPLES</span></span>

### <span data-ttu-id="39f47-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39f47-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="39f47-109">Uzyskiwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="39f47-109">Get cluster</span></span>

## <span data-ttu-id="39f47-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39f47-110">PARAMETERS</span></span>

### <span data-ttu-id="39f47-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39f47-111">-ClusterName</span></span>
<span data-ttu-id="39f47-112">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="39f47-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f47-113">-DefaultProfile</span></span>
<span data-ttu-id="39f47-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39f47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f47-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f47-115">-ResourceGroupName</span></span>
<span data-ttu-id="39f47-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39f47-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f47-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f47-117">CommonParameters</span></span>
<span data-ttu-id="39f47-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f47-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f47-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39f47-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f47-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39f47-120">INPUTS</span></span>

### <span data-ttu-id="39f47-121">System.String</span><span class="sxs-lookup"><span data-stu-id="39f47-121">System.String</span></span>

## <span data-ttu-id="39f47-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39f47-122">OUTPUTS</span></span>

### <span data-ttu-id="39f47-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="39f47-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="39f47-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39f47-124">NOTES</span></span>

## <span data-ttu-id="39f47-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39f47-125">RELATED LINKS</span></span>
