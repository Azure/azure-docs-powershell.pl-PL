---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223697"
---
# <span data-ttu-id="06da4-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="06da4-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="06da4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06da4-102">SYNOPSIS</span></span>
<span data-ttu-id="06da4-103">Zbiera dzienniki zdarzeń na komputerach z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="06da4-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="06da4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06da4-104">SYNTAX</span></span>

### <span data-ttu-id="06da4-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06da4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06da4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06da4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06da4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="06da4-107">DESCRIPTION</span></span>
<span data-ttu-id="06da4-108">Polecenie cmdlet **New-AzOperationalInsightsWindowsEventDataSource** umożliwia dodanie źródła danych zbierającego dzienniki zdarzeń systemu Windows z połączonych komputerów, na których jest uruchomiony system operacyjny Windows w usłudze Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="06da4-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="06da4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06da4-109">EXAMPLES</span></span>

### <span data-ttu-id="06da4-110">Przykład 1. Tworzenie systemowych źródeł danych zdarzeń systemu Windows</span><span class="sxs-lookup"><span data-stu-id="06da4-110">Example 1: Create system Windows event data source</span></span>
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

## <span data-ttu-id="06da4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06da4-111">PARAMETERS</span></span>

### <span data-ttu-id="06da4-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="06da4-112">-CollectErrors</span></span>
<span data-ttu-id="06da4-113">Wskazuje, że usługa Insights gromadzi komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="06da4-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="06da4-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="06da4-114">-CollectInformation</span></span>
<span data-ttu-id="06da4-115">Wskazuje, że komunikaty informacyjne są zbierane.</span><span class="sxs-lookup"><span data-stu-id="06da4-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="06da4-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="06da4-116">-CollectWarnings</span></span>
<span data-ttu-id="06da4-117">Wskazuje, że usługa Insights gromadzi komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="06da4-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="06da4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06da4-118">-DefaultProfile</span></span>
<span data-ttu-id="06da4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="06da4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06da4-120">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="06da4-120">-EventLogName</span></span>
<span data-ttu-id="06da4-121">Określa nazwę dziennika zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="06da4-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="06da4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="06da4-122">-Force</span></span>
<span data-ttu-id="06da4-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="06da4-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06da4-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06da4-124">-Name</span></span>
<span data-ttu-id="06da4-125">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="06da4-125">Specifies a name for the data source.</span></span> <span data-ttu-id="06da4-126">Nazwa nie jest uwidaczniana w portalu Azure, a dowolny ciąg może być wykorzystywany tak długo, jak jest unikatowy.</span><span class="sxs-lookup"><span data-stu-id="06da4-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="06da4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06da4-127">-ResourceGroupName</span></span>
<span data-ttu-id="06da4-128">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="06da4-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="06da4-129">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="06da4-129">-Workspace</span></span>
<span data-ttu-id="06da4-130">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06da4-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="06da4-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="06da4-131">-WorkspaceName</span></span>
<span data-ttu-id="06da4-132">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06da4-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="06da4-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06da4-133">-Confirm</span></span>
<span data-ttu-id="06da4-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06da4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06da4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06da4-135">-WhatIf</span></span>
<span data-ttu-id="06da4-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06da4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06da4-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06da4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06da4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06da4-138">CommonParameters</span></span>
<span data-ttu-id="06da4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06da4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06da4-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06da4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06da4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06da4-141">INPUTS</span></span>

### <span data-ttu-id="06da4-142">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="06da4-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="06da4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="06da4-143">System.String</span></span>

## <span data-ttu-id="06da4-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06da4-144">OUTPUTS</span></span>

### <span data-ttu-id="06da4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="06da4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="06da4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06da4-146">NOTES</span></span>

## <span data-ttu-id="06da4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06da4-147">RELATED LINKS</span></span>
