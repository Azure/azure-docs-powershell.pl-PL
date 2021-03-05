---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 71a715386a4d5646f1c9015244ad8a096313bb64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965601"
---
# <span data-ttu-id="b0317-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="b0317-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="b0317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0317-102">SYNOPSIS</span></span>
<span data-ttu-id="b0317-103">Uzyskiwanie lub lista połączonych usług dla obszaru roboczego programu Groove</span><span class="sxs-lookup"><span data-stu-id="b0317-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="b0317-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0317-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0317-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0317-105">DESCRIPTION</span></span>
<span data-ttu-id="b0317-106">Uzyskiwanie lub lista połączonych usług dla obszaru roboczego, lista, gdy nie podano nazwy "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="b0317-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="b0317-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0317-107">EXAMPLES</span></span>

### <span data-ttu-id="b0317-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0317-108">Example 1</span></span>
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

<span data-ttu-id="b0317-109">Uzyskiwanie usługi połączonej dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b0317-109">Get linked service for workspace</span></span>

## <span data-ttu-id="b0317-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0317-110">PARAMETERS</span></span>

### <span data-ttu-id="b0317-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0317-111">-DefaultProfile</span></span>
<span data-ttu-id="b0317-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0317-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0317-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b0317-113">-LinkedServiceName</span></span>
<span data-ttu-id="b0317-114">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="b0317-114">The linked service name.</span></span>

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

### <span data-ttu-id="b0317-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0317-115">-ResourceGroupName</span></span>
<span data-ttu-id="b0317-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0317-116">The resource group name.</span></span>

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

### <span data-ttu-id="b0317-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0317-117">-WorkspaceName</span></span>
<span data-ttu-id="b0317-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0317-118">The workspace name.</span></span>

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

### <span data-ttu-id="b0317-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0317-119">CommonParameters</span></span>
<span data-ttu-id="b0317-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0317-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0317-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0317-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0317-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0317-122">INPUTS</span></span>

### <span data-ttu-id="b0317-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b0317-123">System.String</span></span>

## <span data-ttu-id="b0317-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0317-124">OUTPUTS</span></span>

### <span data-ttu-id="b0317-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b0317-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="b0317-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0317-126">NOTES</span></span>

## <span data-ttu-id="b0317-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0317-127">RELATED LINKS</span></span>
