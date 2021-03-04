---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 505156f1c6303b8a3fa699b5528ed3ca2ff690de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990886"
---
# <span data-ttu-id="9e47c-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e47c-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="9e47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e47c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e47c-103">Pobiera szczegółowe informacje o grupach zarządzania połączonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="9e47c-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="9e47c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e47c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e47c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e47c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e47c-106">Polecenie **cmdlet Get-AzOperationalInsightsWorkspaceManagementGroup** wyświetla listę grup zarządzania połączonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="9e47c-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="9e47c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e47c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e47c-108">Przykład 1. Uzyskiwanie grup zarządzania według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="9e47c-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="9e47c-109">To polecenie pobiera grupy zarządzania dla obszaru roboczego o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9e47c-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="9e47c-110">Przykład 2. Uzyskiwanie grup zarządzania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="9e47c-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="9e47c-111">To polecenie używa Get-AzOperationalInsightsWorkspace cmdlet w celu uzyskania obszaru roboczego o nazwie MyWorkspace, a następnie przekazuje go do bieżącego polecenia cmdlet, które pobiera grupy zarządzania dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9e47c-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="9e47c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e47c-112">PARAMETERS</span></span>

### <span data-ttu-id="9e47c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e47c-113">-DefaultProfile</span></span>
<span data-ttu-id="9e47c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9e47c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e47c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e47c-115">-Name</span></span>
<span data-ttu-id="9e47c-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9e47c-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e47c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e47c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9e47c-118">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e47c-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e47c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e47c-119">CommonParameters</span></span>
<span data-ttu-id="9e47c-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e47c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e47c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e47c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e47c-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e47c-122">INPUTS</span></span>

### <span data-ttu-id="9e47c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9e47c-123">System.String</span></span>

## <span data-ttu-id="9e47c-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e47c-124">OUTPUTS</span></span>

### <span data-ttu-id="9e47c-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e47c-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="9e47c-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e47c-126">NOTES</span></span>

## <span data-ttu-id="9e47c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e47c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e47c-128">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="9e47c-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="9e47c-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e47c-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


