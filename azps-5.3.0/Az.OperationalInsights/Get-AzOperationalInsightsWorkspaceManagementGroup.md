---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504326"
---
# <span data-ttu-id="fcf81-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fcf81-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="fcf81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcf81-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf81-103">Umożliwia pobieranie szczegółów dotyczących grup zarządzania połączonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="fcf81-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="fcf81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcf81-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcf81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcf81-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf81-106">Polecenie cmdlet **Get-AzOperationalInsightsWorkspaceManagementGroup** zawiera listę grup zarządzania, które są połączone z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="fcf81-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="fcf81-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcf81-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf81-108">Przykład 1: Uzyskaj grupy zarządzania według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="fcf81-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="fcf81-109">To polecenie umożliwia pobieranie grup zarządzania dla obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fcf81-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fcf81-110">Przykład 2: uzyskiwanie grup zarządzania przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="fcf81-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="fcf81-111">To polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać obszar roboczy do bieżącego polecenia cmdlet, który pobiera grupy zarządzania dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fcf81-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="fcf81-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcf81-112">PARAMETERS</span></span>

### <span data-ttu-id="fcf81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf81-113">-DefaultProfile</span></span>
<span data-ttu-id="fcf81-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fcf81-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcf81-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fcf81-115">-Name</span></span>
<span data-ttu-id="fcf81-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fcf81-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="fcf81-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf81-117">-ResourceGroupName</span></span>
<span data-ttu-id="fcf81-118">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf81-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="fcf81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf81-119">CommonParameters</span></span>
<span data-ttu-id="fcf81-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf81-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf81-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf81-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcf81-122">INPUTS</span></span>

### <span data-ttu-id="fcf81-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fcf81-123">System.String</span></span>

## <span data-ttu-id="fcf81-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcf81-124">OUTPUTS</span></span>

### <span data-ttu-id="fcf81-125">Microsoft. Azure. Commands. OperationalInsights. models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fcf81-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="fcf81-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcf81-126">NOTES</span></span>

## <span data-ttu-id="fcf81-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcf81-127">RELATED LINKS</span></span>

[<span data-ttu-id="fcf81-128">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="fcf81-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="fcf81-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fcf81-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


