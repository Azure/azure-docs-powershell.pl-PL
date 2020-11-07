---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 4230eadc005ca53600feb2e6bc7ee2e001d7b209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708808"
---
# <span data-ttu-id="38498-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="38498-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="38498-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38498-102">SYNOPSIS</span></span>
<span data-ttu-id="38498-103">Zbiera dzienniki zdarzeń na komputerach z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="38498-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="38498-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38498-104">SYNTAX</span></span>

### <span data-ttu-id="38498-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38498-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38498-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="38498-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38498-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38498-107">DESCRIPTION</span></span>
<span data-ttu-id="38498-108">Polecenie cmdlet **New-AzOperationalInsightsWindowsEventDataSource** umożliwia dodanie źródła danych zbierającego dzienniki zdarzeń systemu Windows z połączonych komputerów, na których jest uruchomiony system operacyjny Windows w usłudze Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="38498-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="38498-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38498-109">EXAMPLES</span></span>

## <span data-ttu-id="38498-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38498-110">PARAMETERS</span></span>

### <span data-ttu-id="38498-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="38498-111">-CollectErrors</span></span>
<span data-ttu-id="38498-112">Wskazuje, że usługa Insights gromadzi komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="38498-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="38498-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="38498-113">-CollectInformation</span></span>
<span data-ttu-id="38498-114">Wskazuje, że komunikaty informacyjne są zbierane.</span><span class="sxs-lookup"><span data-stu-id="38498-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="38498-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="38498-115">-CollectWarnings</span></span>
<span data-ttu-id="38498-116">Wskazuje, że usługa Insights gromadzi komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="38498-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="38498-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38498-117">-DefaultProfile</span></span>
<span data-ttu-id="38498-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="38498-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38498-119">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="38498-119">-EventLogName</span></span>
<span data-ttu-id="38498-120">Określa nazwę dziennika zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="38498-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="38498-121">-Force</span><span class="sxs-lookup"><span data-stu-id="38498-121">-Force</span></span>
<span data-ttu-id="38498-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="38498-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38498-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38498-123">-Name</span></span>
<span data-ttu-id="38498-124">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="38498-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="38498-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38498-125">-ResourceGroupName</span></span>
<span data-ttu-id="38498-126">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="38498-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="38498-127">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="38498-127">-Workspace</span></span>
<span data-ttu-id="38498-128">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38498-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="38498-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="38498-129">-WorkspaceName</span></span>
<span data-ttu-id="38498-130">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38498-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="38498-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38498-131">-Confirm</span></span>
<span data-ttu-id="38498-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38498-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38498-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38498-133">-WhatIf</span></span>
<span data-ttu-id="38498-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38498-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38498-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38498-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38498-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38498-136">CommonParameters</span></span>
<span data-ttu-id="38498-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38498-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38498-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38498-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38498-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38498-139">INPUTS</span></span>

### <span data-ttu-id="38498-140">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="38498-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="38498-141">System. String</span><span class="sxs-lookup"><span data-stu-id="38498-141">System.String</span></span>

## <span data-ttu-id="38498-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38498-142">OUTPUTS</span></span>

### <span data-ttu-id="38498-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="38498-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="38498-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38498-144">NOTES</span></span>

## <span data-ttu-id="38498-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38498-145">RELATED LINKS</span></span>
