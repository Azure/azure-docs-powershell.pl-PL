---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184114"
---
# <span data-ttu-id="b5e55-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="b5e55-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="b5e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e55-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e55-103">Uzyskiwanie usługi połączonej lub listy dla obszaru roboczego programu Groove</span><span class="sxs-lookup"><span data-stu-id="b5e55-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="b5e55-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5e55-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5e55-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5e55-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e55-106">Uzyskiwanie lub lista połączonych usług dla obszaru roboczego, lista, gdy nie podano nazwy "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="b5e55-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="b5e55-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5e55-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e55-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5e55-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="b5e55-109">Uzyskiwanie usługi połączonej dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b5e55-109">Get linked service for workspace</span></span>

## <span data-ttu-id="b5e55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5e55-110">PARAMETERS</span></span>

### <span data-ttu-id="b5e55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e55-111">-DefaultProfile</span></span>
<span data-ttu-id="b5e55-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5e55-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b5e55-113">-LinkedServiceName</span></span>
<span data-ttu-id="b5e55-114">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="b5e55-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e55-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e55-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5e55-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5e55-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e55-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5e55-117">-WorkspaceName</span></span>
<span data-ttu-id="b5e55-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b5e55-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e55-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e55-119">CommonParameters</span></span>
<span data-ttu-id="b5e55-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e55-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e55-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5e55-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e55-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5e55-122">INPUTS</span></span>

### <span data-ttu-id="b5e55-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b5e55-123">System.String</span></span>

## <span data-ttu-id="b5e55-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5e55-124">OUTPUTS</span></span>

### <span data-ttu-id="b5e55-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b5e55-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="b5e55-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5e55-126">NOTES</span></span>

## <span data-ttu-id="b5e55-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5e55-127">RELATED LINKS</span></span>
