---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179226"
---
# <span data-ttu-id="cf025-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf025-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="cf025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf025-102">SYNOPSIS</span></span>
<span data-ttu-id="cf025-103">Pobiera informacje o obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cf025-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="cf025-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf025-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf025-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf025-105">DESCRIPTION</span></span>
<span data-ttu-id="cf025-106">Polecenie **cmdlet Get-AzOperationalInsightsWorkspace** pobiera informacje o istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cf025-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="cf025-107">Po określeniu nazwy obszaru roboczego to polecenie cmdlet pobiera informacje o tym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cf025-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="cf025-108">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich obszarach roboczych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf025-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="cf025-109">Jeśli nie określisz grupy nazw i zasobów, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cf025-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="cf025-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf025-110">EXAMPLES</span></span>

### <span data-ttu-id="cf025-111">Przykład 1. Uzyskiwanie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="cf025-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="cf025-112">To polecenie pobiera obszar roboczy o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cf025-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="cf025-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf025-113">PARAMETERS</span></span>

### <span data-ttu-id="cf025-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf025-114">-DefaultProfile</span></span>
<span data-ttu-id="cf025-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cf025-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf025-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf025-116">-Name</span></span>
<span data-ttu-id="cf025-117">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="cf025-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf025-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf025-118">-ResourceGroupName</span></span>
<span data-ttu-id="cf025-119">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf025-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf025-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf025-120">CommonParameters</span></span>
<span data-ttu-id="cf025-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf025-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf025-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf025-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf025-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf025-123">INPUTS</span></span>

### <span data-ttu-id="cf025-124">System.String</span><span class="sxs-lookup"><span data-stu-id="cf025-124">System.String</span></span>

## <span data-ttu-id="cf025-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf025-125">OUTPUTS</span></span>

### <span data-ttu-id="cf025-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf025-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="cf025-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf025-127">NOTES</span></span>

## <span data-ttu-id="cf025-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf025-128">RELATED LINKS</span></span>

[<span data-ttu-id="cf025-129">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="cf025-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


