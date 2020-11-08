---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232046"
---
# <span data-ttu-id="0497b-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="0497b-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="0497b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0497b-102">SYNOPSIS</span></span>
<span data-ttu-id="0497b-103">Uzyskiwanie lub wyświetlanie listy połączonych usług dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="0497b-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="0497b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0497b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0497b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0497b-105">DESCRIPTION</span></span>
<span data-ttu-id="0497b-106">Uzyskiwanie lub wyświetlanie listy połączonych usług dla obszaru roboczego, wyświetlanie listy nie podano "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="0497b-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="0497b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0497b-107">EXAMPLES</span></span>

### <span data-ttu-id="0497b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0497b-108">Example 1</span></span>
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

<span data-ttu-id="0497b-109">Uzyskiwanie połączonej usługi dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="0497b-109">Get linked service for workspace</span></span>

## <span data-ttu-id="0497b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0497b-110">PARAMETERS</span></span>

### <span data-ttu-id="0497b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0497b-111">-DefaultProfile</span></span>
<span data-ttu-id="0497b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0497b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0497b-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="0497b-113">-LinkedServiceName</span></span>
<span data-ttu-id="0497b-114">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="0497b-114">The linked service name.</span></span>

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

### <span data-ttu-id="0497b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0497b-115">-ResourceGroupName</span></span>
<span data-ttu-id="0497b-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0497b-116">The resource group name.</span></span>

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

### <span data-ttu-id="0497b-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="0497b-117">-WorkspaceName</span></span>
<span data-ttu-id="0497b-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0497b-118">The workspace name.</span></span>

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

### <span data-ttu-id="0497b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0497b-119">CommonParameters</span></span>
<span data-ttu-id="0497b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0497b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0497b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0497b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0497b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0497b-122">INPUTS</span></span>

### <span data-ttu-id="0497b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0497b-123">System.String</span></span>

## <span data-ttu-id="0497b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0497b-124">OUTPUTS</span></span>

### <span data-ttu-id="0497b-125">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0497b-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="0497b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0497b-126">NOTES</span></span>

## <span data-ttu-id="0497b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0497b-127">RELATED LINKS</span></span>
