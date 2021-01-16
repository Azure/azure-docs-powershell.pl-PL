---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341638"
---
# <span data-ttu-id="80b89-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="80b89-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="80b89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80b89-102">SYNOPSIS</span></span>
<span data-ttu-id="80b89-103">Dodaje liczniki wydajności do wszystkich komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="80b89-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="80b89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80b89-104">SYNTAX</span></span>

### <span data-ttu-id="80b89-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80b89-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b89-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="80b89-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b89-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80b89-107">DESCRIPTION</span></span>
<span data-ttu-id="80b89-108">Polecenie cmdlet **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** umożliwia dodanie liczników wydajności, z których usługa Azure Operational Insights gromadzi dane na wszystkich komputerach z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="80b89-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="80b89-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80b89-109">EXAMPLES</span></span>

## <span data-ttu-id="80b89-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80b89-110">PARAMETERS</span></span>

### <span data-ttu-id="80b89-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="80b89-111">-CounterNames</span></span>
<span data-ttu-id="80b89-112">Określa tablicę nazw liczników.</span><span class="sxs-lookup"><span data-stu-id="80b89-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b89-113">-DefaultProfile</span></span>
<span data-ttu-id="80b89-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="80b89-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80b89-115">-Force</span><span class="sxs-lookup"><span data-stu-id="80b89-115">-Force</span></span>
<span data-ttu-id="80b89-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="80b89-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80b89-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="80b89-117">-InstanceName</span></span>
<span data-ttu-id="80b89-118">Określa nazwę wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="80b89-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="80b89-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="80b89-119">-IntervalSeconds</span></span>
<span data-ttu-id="80b89-120">Określa interwał kolekcji.</span><span class="sxs-lookup"><span data-stu-id="80b89-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="80b89-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80b89-121">-Name</span></span>
<span data-ttu-id="80b89-122">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="80b89-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="80b89-123">-NazwaObiektu</span><span class="sxs-lookup"><span data-stu-id="80b89-123">-ObjectName</span></span>
<span data-ttu-id="80b89-124">Określa nazwę obiektu.</span><span class="sxs-lookup"><span data-stu-id="80b89-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="80b89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b89-125">-ResourceGroupName</span></span>
<span data-ttu-id="80b89-126">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="80b89-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="80b89-127">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="80b89-127">-Workspace</span></span>
<span data-ttu-id="80b89-128">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80b89-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="80b89-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="80b89-129">-WorkspaceName</span></span>
<span data-ttu-id="80b89-130">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80b89-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="80b89-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80b89-131">-Confirm</span></span>
<span data-ttu-id="80b89-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80b89-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b89-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b89-133">-WhatIf</span></span>
<span data-ttu-id="80b89-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80b89-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b89-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80b89-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b89-136">CommonParameters</span></span>
<span data-ttu-id="80b89-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b89-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b89-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b89-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80b89-139">INPUTS</span></span>

### <span data-ttu-id="80b89-140">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="80b89-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="80b89-141">System. String</span><span class="sxs-lookup"><span data-stu-id="80b89-141">System.String</span></span>

### <span data-ttu-id="80b89-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="80b89-142">System.String[]</span></span>

### <span data-ttu-id="80b89-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="80b89-143">System.Int32</span></span>

## <span data-ttu-id="80b89-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80b89-144">OUTPUTS</span></span>

### <span data-ttu-id="80b89-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="80b89-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="80b89-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80b89-146">NOTES</span></span>

## <span data-ttu-id="80b89-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80b89-147">RELATED LINKS</span></span>

[<span data-ttu-id="80b89-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="80b89-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="80b89-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="80b89-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


