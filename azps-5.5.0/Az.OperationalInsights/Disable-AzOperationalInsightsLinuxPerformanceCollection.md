---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179258"
---
# <span data-ttu-id="3d7d2-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3d7d2-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="3d7d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3d7d2-103">Zatrzymuje zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="3d7d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d7d2-104">SYNTAX</span></span>

### <span data-ttu-id="3d7d2-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d7d2-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d7d2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3d7d2-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d7d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d7d2-107">DESCRIPTION</span></span>
<span data-ttu-id="3d7d2-108">Polecenie cmdlet **Disable-AzOperationalInsightsLinuxPerformanceCollection** zatrzymuje kolekcję liczników wydajności z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="3d7d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d7d2-109">EXAMPLES</span></span>

## <span data-ttu-id="3d7d2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d7d2-110">PARAMETERS</span></span>

### <span data-ttu-id="3d7d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d7d2-111">-DefaultProfile</span></span>
<span data-ttu-id="3d7d2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3d7d2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d7d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d7d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="3d7d2-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d7d2-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="3d7d2-115">-Workspace</span></span>
<span data-ttu-id="3d7d2-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d7d2-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3d7d2-117">-WorkspaceName</span></span>
<span data-ttu-id="3d7d2-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d7d2-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d7d2-119">-Confirm</span></span>
<span data-ttu-id="3d7d2-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7d2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d7d2-121">-WhatIf</span></span>
<span data-ttu-id="3d7d2-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d7d2-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d7d2-124">CommonParameters</span></span>
<span data-ttu-id="3d7d2-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d7d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d7d2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d7d2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d7d2-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d7d2-127">INPUTS</span></span>

### <span data-ttu-id="3d7d2-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3d7d2-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3d7d2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3d7d2-129">System.String</span></span>

## <span data-ttu-id="3d7d2-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d7d2-130">OUTPUTS</span></span>

### <span data-ttu-id="3d7d2-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3d7d2-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3d7d2-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d7d2-132">NOTES</span></span>
* <span data-ttu-id="3d7d2-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="3d7d2-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3d7d2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d7d2-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d7d2-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3d7d2-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="3d7d2-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="3d7d2-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


