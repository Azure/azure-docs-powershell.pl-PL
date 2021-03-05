---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 29f109e0e4f063a72e188a908da8bc65723f5065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989892"
---
# <span data-ttu-id="af49a-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="af49a-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="af49a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af49a-102">SYNOPSIS</span></span>
<span data-ttu-id="af49a-103">Dzienniki zdarzeń są zbierane z komputerów z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="af49a-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="af49a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af49a-104">SYNTAX</span></span>

### <span data-ttu-id="af49a-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="af49a-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af49a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="af49a-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af49a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="af49a-107">DESCRIPTION</span></span>
<span data-ttu-id="af49a-108">Polecenie cmdlet **New-AzOperationalInsightsWindowsEventDataSource** dodaje źródło danych, które zbiera dzienniki zdarzeń systemu Windows z połączonych komputerów z systemem operacyjnym Windows w usłudze Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="af49a-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="af49a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af49a-109">EXAMPLES</span></span>

### <span data-ttu-id="af49a-110">Przykład 1. Tworzenie źródła danych zdarzeń systemu Windows</span><span class="sxs-lookup"><span data-stu-id="af49a-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="af49a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af49a-111">PARAMETERS</span></span>

### <span data-ttu-id="af49a-112">- CollectErrors</span><span class="sxs-lookup"><span data-stu-id="af49a-112">-CollectErrors</span></span>
<span data-ttu-id="af49a-113">Wskazuje, że w szczegółowych informacjach operacyjnych są zbierane komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="af49a-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="af49a-114">- CollectInformation</span><span class="sxs-lookup"><span data-stu-id="af49a-114">-CollectInformation</span></span>
<span data-ttu-id="af49a-115">Wskazuje, że szczegółowe informacje operacyjne zbierają komunikaty informacyjne.</span><span class="sxs-lookup"><span data-stu-id="af49a-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="af49a-116">- CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="af49a-116">-CollectWarnings</span></span>
<span data-ttu-id="af49a-117">Wskazuje, że informacje operacyjne zbierają komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="af49a-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="af49a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af49a-118">-DefaultProfile</span></span>
<span data-ttu-id="af49a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="af49a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af49a-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="af49a-120">-EventLogName</span></span>
<span data-ttu-id="af49a-121">Określa nazwę dziennika zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="af49a-121">Specifies the name of the event log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af49a-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="af49a-122">-Force</span></span>
<span data-ttu-id="af49a-123">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="af49a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af49a-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="af49a-124">-Name</span></span>
<span data-ttu-id="af49a-125">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="af49a-125">Specifies a name for the data source.</span></span> <span data-ttu-id="af49a-126">Nazwa nie jest ujawniona w portalu Azure Portal i można jej używać, jeśli jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="af49a-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af49a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af49a-127">-ResourceGroupName</span></span>
<span data-ttu-id="af49a-128">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="af49a-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="af49a-129">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="af49a-129">-Workspace</span></span>
<span data-ttu-id="af49a-130">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af49a-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="af49a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af49a-131">-WorkspaceName</span></span>
<span data-ttu-id="af49a-132">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af49a-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="af49a-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af49a-133">-Confirm</span></span>
<span data-ttu-id="af49a-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="af49a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af49a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af49a-135">-WhatIf</span></span>
<span data-ttu-id="af49a-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af49a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af49a-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="af49a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af49a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af49a-138">CommonParameters</span></span>
<span data-ttu-id="af49a-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af49a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af49a-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af49a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af49a-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af49a-141">INPUTS</span></span>

### <span data-ttu-id="af49a-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="af49a-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="af49a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="af49a-143">System.String</span></span>

## <span data-ttu-id="af49a-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af49a-144">OUTPUTS</span></span>

### <span data-ttu-id="af49a-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="af49a-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="af49a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af49a-146">NOTES</span></span>

## <span data-ttu-id="af49a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af49a-147">RELATED LINKS</span></span>
