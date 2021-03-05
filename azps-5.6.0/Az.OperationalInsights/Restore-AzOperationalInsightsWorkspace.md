---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1035d918870a15000be066fd59cc72913d8d8cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989752"
---
# <span data-ttu-id="a29a3-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a29a3-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a29a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a29a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a29a3-103">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a29a3-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="a29a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a29a3-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a29a3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a29a3-105">DESCRIPTION</span></span>
<span data-ttu-id="a29a3-106">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a29a3-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="a29a3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a29a3-107">EXAMPLES</span></span>

### <span data-ttu-id="a29a3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a29a3-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="a29a3-109">Przywracanie usuniętego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a29a3-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="a29a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a29a3-110">PARAMETERS</span></span>

### <span data-ttu-id="a29a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29a3-111">-DefaultProfile</span></span>
<span data-ttu-id="a29a3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a29a3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a29a3-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a29a3-113">-Force</span></span>
<span data-ttu-id="a29a3-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a29a3-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29a3-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a29a3-115">-Location</span></span>
<span data-ttu-id="a29a3-116">Region geograficzny, w których zostanie utworzony obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="a29a3-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29a3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a29a3-117">-Name</span></span>
<span data-ttu-id="a29a3-118">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a29a3-118">The workspace name.</span></span>

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

### <span data-ttu-id="a29a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a29a3-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a29a3-120">The resource group name.</span></span>

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

### <span data-ttu-id="a29a3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a29a3-121">-Confirm</span></span>
<span data-ttu-id="a29a3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a29a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a29a3-123">-WhatIf</span></span>
<span data-ttu-id="a29a3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a29a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a29a3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a29a3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29a3-126">CommonParameters</span></span>
<span data-ttu-id="a29a3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a29a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29a3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a29a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29a3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a29a3-129">INPUTS</span></span>

### <span data-ttu-id="a29a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a29a3-130">System.String</span></span>

## <span data-ttu-id="a29a3-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a29a3-131">OUTPUTS</span></span>

### <span data-ttu-id="a29a3-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a29a3-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a29a3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a29a3-133">NOTES</span></span>

## <span data-ttu-id="a29a3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a29a3-134">RELATED LINKS</span></span>
