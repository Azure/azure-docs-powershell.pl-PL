---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225005"
---
# <span data-ttu-id="b5063-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="b5063-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="b5063-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5063-102">SYNOPSIS</span></span>
<span data-ttu-id="b5063-103">Dodaje źródło danych liczników wydajności systemu Windows dla połączonych komputerów, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="b5063-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="b5063-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5063-104">SYNTAX</span></span>

### <span data-ttu-id="b5063-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5063-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5063-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b5063-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5063-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b5063-107">DESCRIPTION</span></span>
<span data-ttu-id="b5063-108">Polecenie cmdlet **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** umożliwia dodanie źródła danych liczników wydajności systemu Windows dla połączonych komputerów, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="b5063-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="b5063-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5063-109">EXAMPLES</span></span>

## <span data-ttu-id="b5063-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5063-110">PARAMETERS</span></span>

### <span data-ttu-id="b5063-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="b5063-111">-CounterName</span></span>
<span data-ttu-id="b5063-112">Określa nazwę licznika.</span><span class="sxs-lookup"><span data-stu-id="b5063-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="b5063-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5063-113">-DefaultProfile</span></span>
<span data-ttu-id="b5063-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b5063-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5063-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5063-115">-Force</span></span>
<span data-ttu-id="b5063-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b5063-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5063-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b5063-117">-InstanceName</span></span>
<span data-ttu-id="b5063-118">Określa nazwę wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b5063-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="b5063-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="b5063-119">-IntervalSeconds</span></span>
<span data-ttu-id="b5063-120">Określa interwał kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b5063-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="b5063-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5063-121">-Name</span></span>
<span data-ttu-id="b5063-122">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="b5063-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="b5063-123">-NazwaObiektu</span><span class="sxs-lookup"><span data-stu-id="b5063-123">-ObjectName</span></span>
<span data-ttu-id="b5063-124">Określa nazwę obiektu.</span><span class="sxs-lookup"><span data-stu-id="b5063-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="b5063-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5063-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5063-126">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="b5063-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="b5063-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="b5063-127">-UseLegacyCollector</span></span>
<span data-ttu-id="b5063-128">Użyj starszego modułu zbierającego lub domyślnego modułu zbierającego.</span><span class="sxs-lookup"><span data-stu-id="b5063-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="b5063-129">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="b5063-129">-Workspace</span></span>
<span data-ttu-id="b5063-130">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5063-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b5063-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b5063-131">-WorkspaceName</span></span>
<span data-ttu-id="b5063-132">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5063-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b5063-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5063-133">-Confirm</span></span>
<span data-ttu-id="b5063-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5063-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5063-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5063-135">-WhatIf</span></span>
<span data-ttu-id="b5063-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5063-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5063-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5063-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5063-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5063-138">CommonParameters</span></span>
<span data-ttu-id="b5063-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5063-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5063-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5063-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5063-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5063-141">INPUTS</span></span>

### <span data-ttu-id="b5063-142">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5063-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b5063-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b5063-143">System.String</span></span>

### <span data-ttu-id="b5063-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b5063-144">System.Int32</span></span>

## <span data-ttu-id="b5063-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5063-145">OUTPUTS</span></span>

### <span data-ttu-id="b5063-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b5063-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b5063-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5063-147">NOTES</span></span>

## <span data-ttu-id="b5063-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5063-148">RELATED LINKS</span></span>
