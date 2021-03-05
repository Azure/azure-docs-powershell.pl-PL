---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 4082e7fc36228953ea33f8f3252bab642ca50e2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001009"
---
# <span data-ttu-id="b42c0-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b42c0-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="b42c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b42c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b42c0-103">Pobiera informacje o obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b42c0-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="b42c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b42c0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b42c0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b42c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b42c0-106">Polecenie **cmdlet Get-AzOperationalInsightsWorkspace** pobiera informacje o istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b42c0-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="b42c0-107">Po określeniu nazwy obszaru roboczego to polecenie cmdlet pobiera informacje o tym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b42c0-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="b42c0-108">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich obszarach roboczych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b42c0-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="b42c0-109">Jeśli nie określisz grupy nazw i zasobów, to polecenie cmdlet pobiera informacje o wszystkich obszarach roboczych w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b42c0-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="b42c0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b42c0-110">EXAMPLES</span></span>

### <span data-ttu-id="b42c0-111">Przykład 1. Uzyskiwanie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="b42c0-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="b42c0-112">To polecenie pobiera obszar roboczy o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b42c0-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="b42c0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b42c0-113">PARAMETERS</span></span>

### <span data-ttu-id="b42c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b42c0-114">-DefaultProfile</span></span>
<span data-ttu-id="b42c0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b42c0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b42c0-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b42c0-116">-Name</span></span>
<span data-ttu-id="b42c0-117">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b42c0-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b42c0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b42c0-118">-ResourceGroupName</span></span>
<span data-ttu-id="b42c0-119">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b42c0-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b42c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b42c0-120">CommonParameters</span></span>
<span data-ttu-id="b42c0-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b42c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b42c0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b42c0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b42c0-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b42c0-123">INPUTS</span></span>

### <span data-ttu-id="b42c0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b42c0-124">System.String</span></span>

## <span data-ttu-id="b42c0-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b42c0-125">OUTPUTS</span></span>

### <span data-ttu-id="b42c0-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b42c0-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="b42c0-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b42c0-127">NOTES</span></span>

## <span data-ttu-id="b42c0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b42c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="b42c0-129">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="b42c0-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


