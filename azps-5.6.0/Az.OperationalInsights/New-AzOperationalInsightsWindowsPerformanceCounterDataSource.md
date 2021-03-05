---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 2e3cd573c337d7ff13401939aaf127fa64a6c765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989885"
---
# <span data-ttu-id="615fa-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="615fa-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="615fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="615fa-102">SYNOPSIS</span></span>
<span data-ttu-id="615fa-103">Dodaje źródło danych licznika wydajności systemu Windows dla połączonych komputerów z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="615fa-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="615fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="615fa-104">SYNTAX</span></span>

### <span data-ttu-id="615fa-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="615fa-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="615fa-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="615fa-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="615fa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="615fa-107">DESCRIPTION</span></span>
<span data-ttu-id="615fa-108">Polecenie cmdlet **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** dodaje źródło danych licznika wydajności systemu Windows dla komputerów połączonych z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="615fa-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="615fa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="615fa-109">EXAMPLES</span></span>

## <span data-ttu-id="615fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="615fa-110">PARAMETERS</span></span>

### <span data-ttu-id="615fa-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="615fa-111">-CounterName</span></span>
<span data-ttu-id="615fa-112">Określa nazwę licznika.</span><span class="sxs-lookup"><span data-stu-id="615fa-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="615fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615fa-113">-DefaultProfile</span></span>
<span data-ttu-id="615fa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="615fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="615fa-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="615fa-115">-Force</span></span>
<span data-ttu-id="615fa-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="615fa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="615fa-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="615fa-117">-InstanceName</span></span>
<span data-ttu-id="615fa-118">Określa nazwę wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="615fa-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="615fa-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="615fa-119">-IntervalSeconds</span></span>
<span data-ttu-id="615fa-120">Określa interwał kolekcji.</span><span class="sxs-lookup"><span data-stu-id="615fa-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="615fa-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="615fa-121">-Name</span></span>
<span data-ttu-id="615fa-122">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="615fa-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="615fa-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="615fa-123">-ObjectName</span></span>
<span data-ttu-id="615fa-124">Określa nazwę obiektu.</span><span class="sxs-lookup"><span data-stu-id="615fa-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="615fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="615fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="615fa-126">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="615fa-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="615fa-127">—UseLegacyColloll</span><span class="sxs-lookup"><span data-stu-id="615fa-127">-UseLegacyCollector</span></span>
<span data-ttu-id="615fa-128">Użyj starszej wersji lub domyślnej wersji.</span><span class="sxs-lookup"><span data-stu-id="615fa-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="615fa-129">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="615fa-129">-Workspace</span></span>
<span data-ttu-id="615fa-130">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="615fa-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="615fa-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="615fa-131">-WorkspaceName</span></span>
<span data-ttu-id="615fa-132">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="615fa-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="615fa-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="615fa-133">-Confirm</span></span>
<span data-ttu-id="615fa-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="615fa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="615fa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="615fa-135">-WhatIf</span></span>
<span data-ttu-id="615fa-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="615fa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="615fa-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="615fa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="615fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615fa-138">CommonParameters</span></span>
<span data-ttu-id="615fa-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="615fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615fa-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="615fa-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615fa-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="615fa-141">INPUTS</span></span>

### <span data-ttu-id="615fa-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="615fa-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="615fa-143">System.String</span><span class="sxs-lookup"><span data-stu-id="615fa-143">System.String</span></span>

### <span data-ttu-id="615fa-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="615fa-144">System.Int32</span></span>

## <span data-ttu-id="615fa-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="615fa-145">OUTPUTS</span></span>

### <span data-ttu-id="615fa-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="615fa-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="615fa-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="615fa-147">NOTES</span></span>

## <span data-ttu-id="615fa-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="615fa-148">RELATED LINKS</span></span>
