---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: a4ac55c3c00ba35fa53f6e9a338712d02e507ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976513"
---
# <span data-ttu-id="fa6ef-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa6ef-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="fa6ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6ef-103">Lista usuniętych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="fa6ef-103">List deleted workspaces.</span></span>

## <span data-ttu-id="fa6ef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa6ef-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa6ef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa6ef-105">DESCRIPTION</span></span>
<span data-ttu-id="fa6ef-106">Lista usuniętych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="fa6ef-106">List deleted workspaces.</span></span>

## <span data-ttu-id="fa6ef-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa6ef-107">EXAMPLES</span></span>

### <span data-ttu-id="fa6ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa6ef-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="fa6ef-109">Lista usuniętych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="fa6ef-109">List deleted workspaces.</span></span>

## <span data-ttu-id="fa6ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa6ef-110">PARAMETERS</span></span>

### <span data-ttu-id="fa6ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6ef-111">-DefaultProfile</span></span>
<span data-ttu-id="fa6ef-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa6ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa6ef-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa6ef-113">-ResourceGroupName</span></span>
<span data-ttu-id="fa6ef-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6ef-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa6ef-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6ef-115">CommonParameters</span></span>
<span data-ttu-id="fa6ef-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa6ef-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6ef-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa6ef-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6ef-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa6ef-118">INPUTS</span></span>

### <span data-ttu-id="fa6ef-119">System.String</span><span class="sxs-lookup"><span data-stu-id="fa6ef-119">System.String</span></span>

## <span data-ttu-id="fa6ef-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa6ef-120">OUTPUTS</span></span>

### <span data-ttu-id="fa6ef-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa6ef-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="fa6ef-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa6ef-122">NOTES</span></span>

## <span data-ttu-id="fa6ef-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa6ef-123">RELATED LINKS</span></span>
