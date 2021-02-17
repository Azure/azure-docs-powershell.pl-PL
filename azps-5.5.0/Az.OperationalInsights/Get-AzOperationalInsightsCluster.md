---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191483"
---
# <span data-ttu-id="f01ec-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="f01ec-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="f01ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f01ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f01ec-103">Uzyskiwanie lub lista klastrów</span><span class="sxs-lookup"><span data-stu-id="f01ec-103">Get or list clusters</span></span>

## <span data-ttu-id="f01ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f01ec-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f01ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f01ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f01ec-106">Uzyskiwanie lub lista klastrów, klastry list w grupie zasobów, gdy nie podano "-ClusterName", klastry list w ramach subskrypcji, gdy nie zostały podane wartości "-ClusterName" i "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="f01ec-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="f01ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f01ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f01ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f01ec-108">Example 1</span></span>
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

<span data-ttu-id="f01ec-109">Uzyskiwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="f01ec-109">Get cluster</span></span>

## <span data-ttu-id="f01ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f01ec-110">PARAMETERS</span></span>

### <span data-ttu-id="f01ec-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f01ec-111">-ClusterName</span></span>
<span data-ttu-id="f01ec-112">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="f01ec-112">The cluster name.</span></span>

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

### <span data-ttu-id="f01ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01ec-113">-DefaultProfile</span></span>
<span data-ttu-id="f01ec-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f01ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f01ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f01ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="f01ec-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f01ec-116">The resource group name.</span></span>

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

### <span data-ttu-id="f01ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01ec-117">CommonParameters</span></span>
<span data-ttu-id="f01ec-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f01ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01ec-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f01ec-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01ec-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f01ec-120">INPUTS</span></span>

### <span data-ttu-id="f01ec-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f01ec-121">System.String</span></span>

## <span data-ttu-id="f01ec-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f01ec-122">OUTPUTS</span></span>

### <span data-ttu-id="f01ec-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f01ec-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="f01ec-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f01ec-124">NOTES</span></span>

## <span data-ttu-id="f01ec-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f01ec-125">RELATED LINKS</span></span>
