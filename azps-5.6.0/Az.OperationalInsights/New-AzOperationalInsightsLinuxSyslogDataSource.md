---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: ab11fcb47550603e23871730ed8779baa6cf7740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989920"
---
# <span data-ttu-id="6afd8-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="6afd8-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="6afd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afd8-102">SYNOPSIS</span></span>
<span data-ttu-id="6afd8-103">Dodaje źródło danych do komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="6afd8-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="6afd8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6afd8-104">SYNTAX</span></span>

### <span data-ttu-id="6afd8-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="6afd8-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6afd8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6afd8-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6afd8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6afd8-107">DESCRIPTION</span></span>
<span data-ttu-id="6afd8-108">Polecenie **cmdlet New-AzOperationalInsightsLinuxSyslogDataSource** dodaje źródło danych syslog do połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="6afd8-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="6afd8-109">Usługa Azure Operational Insights może zbierać dane syslogu.</span><span class="sxs-lookup"><span data-stu-id="6afd8-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="6afd8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6afd8-110">EXAMPLES</span></span>

### <span data-ttu-id="6afd8-111">Przykład 1. Tworzenie źródeł danych syslogu</span><span class="sxs-lookup"><span data-stu-id="6afd8-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="6afd8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6afd8-112">PARAMETERS</span></span>

### <span data-ttu-id="6afd8-113">- CollectAlert</span><span class="sxs-lookup"><span data-stu-id="6afd8-113">-CollectAlert</span></span>
<span data-ttu-id="6afd8-114">Wskazuje, że informacje operacyjne zbierają komunikaty alertów.</span><span class="sxs-lookup"><span data-stu-id="6afd8-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="6afd8-115">- CollectCritical</span><span class="sxs-lookup"><span data-stu-id="6afd8-115">-CollectCritical</span></span>
<span data-ttu-id="6afd8-116">Wskazuje, że szczegółowe informacje operacyjne zbierają krytyczne wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6afd8-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="6afd8-117">- CollectDebug</span><span class="sxs-lookup"><span data-stu-id="6afd8-117">-CollectDebug</span></span>
<span data-ttu-id="6afd8-118">Wskazuje, że szczegółowe informacje operacyjne zbierają komunikaty debugowania.</span><span class="sxs-lookup"><span data-stu-id="6afd8-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="6afd8-119">- CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="6afd8-119">-CollectEmergency</span></span>
<span data-ttu-id="6afd8-120">Wskazuje, że informacje operacyjne zbierają wiadomości alarmowe.</span><span class="sxs-lookup"><span data-stu-id="6afd8-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="6afd8-121">- CollectError</span><span class="sxs-lookup"><span data-stu-id="6afd8-121">-CollectError</span></span>
<span data-ttu-id="6afd8-122">Wskazuje, że w szczegółowych informacjach operacyjnych są zbierane komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="6afd8-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="6afd8-123">- CollectInformational</span><span class="sxs-lookup"><span data-stu-id="6afd8-123">-CollectInformational</span></span>
<span data-ttu-id="6afd8-124">Wskazuje, że szczegółowe informacje operacyjne zbierają komunikaty informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6afd8-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="6afd8-125">- CollectNotice</span><span class="sxs-lookup"><span data-stu-id="6afd8-125">-CollectNotice</span></span>
<span data-ttu-id="6afd8-126">Wskazuje, że informacje operacyjne zbierają komunikaty o powiadomieniach.</span><span class="sxs-lookup"><span data-stu-id="6afd8-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="6afd8-127">- CollectWarning</span><span class="sxs-lookup"><span data-stu-id="6afd8-127">-CollectWarning</span></span>
<span data-ttu-id="6afd8-128">Wskazuje, że syslog zawiera komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="6afd8-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="6afd8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afd8-129">-DefaultProfile</span></span>
<span data-ttu-id="6afd8-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6afd8-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6afd8-131">-Wiad.</span><span class="sxs-lookup"><span data-stu-id="6afd8-131">-Facility</span></span>
<span data-ttu-id="6afd8-132">Określa kod obiektu.</span><span class="sxs-lookup"><span data-stu-id="6afd8-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="6afd8-133">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6afd8-133">-Force</span></span>
<span data-ttu-id="6afd8-134">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6afd8-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6afd8-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6afd8-135">-Name</span></span>
<span data-ttu-id="6afd8-136">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="6afd8-136">Specifies a name for the data source.</span></span> <span data-ttu-id="6afd8-137">Nazwa nie jest ujawniona w portalu Azure Portal i można jej używać, jeśli jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="6afd8-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="6afd8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6afd8-138">-ResourceGroupName</span></span>
<span data-ttu-id="6afd8-139">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="6afd8-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="6afd8-140">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="6afd8-140">-Workspace</span></span>
<span data-ttu-id="6afd8-141">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6afd8-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6afd8-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6afd8-142">-WorkspaceName</span></span>
<span data-ttu-id="6afd8-143">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6afd8-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6afd8-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6afd8-144">-Confirm</span></span>
<span data-ttu-id="6afd8-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6afd8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6afd8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6afd8-146">-WhatIf</span></span>
<span data-ttu-id="6afd8-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6afd8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6afd8-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6afd8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6afd8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afd8-149">CommonParameters</span></span>
<span data-ttu-id="6afd8-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afd8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afd8-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6afd8-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afd8-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6afd8-152">INPUTS</span></span>

### <span data-ttu-id="6afd8-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6afd8-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6afd8-154">System.String</span><span class="sxs-lookup"><span data-stu-id="6afd8-154">System.String</span></span>

## <span data-ttu-id="6afd8-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6afd8-155">OUTPUTS</span></span>

### <span data-ttu-id="6afd8-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6afd8-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6afd8-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6afd8-157">NOTES</span></span>

## <span data-ttu-id="6afd8-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6afd8-158">RELATED LINKS</span></span>

[<span data-ttu-id="6afd8-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6afd8-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="6afd8-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6afd8-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


