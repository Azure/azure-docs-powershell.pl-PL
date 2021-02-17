---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240426"
---
# <span data-ttu-id="64cf2-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="64cf2-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="64cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="64cf2-103">Pobiera dane dotyczące użycia dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="64cf2-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="64cf2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64cf2-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64cf2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="64cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="64cf2-106">Polecenie **cmdlet Get-AzOperationalInsightsWorkspaceUsage** pobiera dane użycia dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="64cf2-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="64cf2-107">Udostępnia to informacje o tym, jaka część danych była analizowana przez obszar roboczy w określonym okresie.</span><span class="sxs-lookup"><span data-stu-id="64cf2-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="64cf2-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64cf2-108">EXAMPLES</span></span>

### <span data-ttu-id="64cf2-109">Przykład 1. Uzyskiwanie danych dotyczących użycia według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="64cf2-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="64cf2-110">To polecenie pobiera szczegóły użycia dla obszaru roboczego o nazwie MyWorkspace w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="64cf2-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="64cf2-111">Przykład 2. Uzyskiwanie danych dotyczących użycia przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="64cf2-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="64cf2-112">To polecenie pobiera obszar roboczy o nazwie MyWorkSpace za Get-AzOperationalInsightsWorkspace cmdlet, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64cf2-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="64cf2-113">Polecenie pobiera szczegóły użycia dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="64cf2-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="64cf2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64cf2-114">PARAMETERS</span></span>

### <span data-ttu-id="64cf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64cf2-115">-DefaultProfile</span></span>
<span data-ttu-id="64cf2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="64cf2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64cf2-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64cf2-117">-Name</span></span>
<span data-ttu-id="64cf2-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="64cf2-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="64cf2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64cf2-119">-ResourceGroupName</span></span>
<span data-ttu-id="64cf2-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64cf2-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="64cf2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64cf2-121">CommonParameters</span></span>
<span data-ttu-id="64cf2-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64cf2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64cf2-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64cf2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64cf2-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64cf2-124">INPUTS</span></span>

### <span data-ttu-id="64cf2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="64cf2-125">System.String</span></span>

## <span data-ttu-id="64cf2-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64cf2-126">OUTPUTS</span></span>

### <span data-ttu-id="64cf2-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="64cf2-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="64cf2-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64cf2-128">NOTES</span></span>

## <span data-ttu-id="64cf2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64cf2-129">RELATED LINKS</span></span>

[<span data-ttu-id="64cf2-130">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="64cf2-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="64cf2-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="64cf2-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


