---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231700"
---
# <span data-ttu-id="7f8b4-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="7f8b4-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="7f8b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8b4-103">Dodaje źródło danych do komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="7f8b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f8b4-104">SYNTAX</span></span>

### <span data-ttu-id="7f8b4-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f8b4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8b4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7f8b4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f8b4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7f8b4-107">DESCRIPTION</span></span>
<span data-ttu-id="7f8b4-108">Polecenie cmdlet **New-AzOperationalInsightsLinuxSyslogDataSource** umożliwia dodanie źródła danych dziennika systemowego do połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="7f8b4-109">Usługa Azure Operational Insights może zbierać dane dziennika systemowego.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="7f8b4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f8b4-110">EXAMPLES</span></span>

### <span data-ttu-id="7f8b4-111">Przykład 1. Tworzenie źródeł danych dziennika systemowego</span><span class="sxs-lookup"><span data-stu-id="7f8b4-111">Example 1: Create syslog data sources</span></span>
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

## <span data-ttu-id="7f8b4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f8b4-112">PARAMETERS</span></span>

### <span data-ttu-id="7f8b4-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="7f8b4-113">-CollectAlert</span></span>
<span data-ttu-id="7f8b4-114">Wskazuje, że komunikaty ostrzegawcze dotyczące obserwacji są zbierane.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="7f8b4-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="7f8b4-115">-CollectCritical</span></span>
<span data-ttu-id="7f8b4-116">Wskazuje, że usługa Insights gromadzi wiadomości krytyczne.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="7f8b4-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="7f8b4-117">-CollectDebug</span></span>
<span data-ttu-id="7f8b4-118">Wskazuje, że wiadomości debugowania w usłudze Insights są zbierane.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="7f8b4-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="7f8b4-119">-CollectEmergency</span></span>
<span data-ttu-id="7f8b4-120">Wskazuje, że usługa Insights gromadzi wiadomości z awaryjnymi.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="7f8b4-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="7f8b4-121">-CollectError</span></span>
<span data-ttu-id="7f8b4-122">Wskazuje, że usługa Insights gromadzi komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="7f8b4-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="7f8b4-123">-CollectInformational</span></span>
<span data-ttu-id="7f8b4-124">Wskazuje, że usługa Insights gromadzi wiadomości informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="7f8b4-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="7f8b4-125">-CollectNotice</span></span>
<span data-ttu-id="7f8b4-126">Wskazuje, że komunikaty o błędach działania są zbierane.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="7f8b4-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="7f8b4-127">-CollectWarning</span></span>
<span data-ttu-id="7f8b4-128">Wskazuje, że dziennik systemowy zawiera komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="7f8b4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8b4-129">-DefaultProfile</span></span>
<span data-ttu-id="7f8b4-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7f8b4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f8b4-131">-Obiekt</span><span class="sxs-lookup"><span data-stu-id="7f8b4-131">-Facility</span></span>
<span data-ttu-id="7f8b4-132">Określa kod instrumentu.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="7f8b4-133">-Force</span><span class="sxs-lookup"><span data-stu-id="7f8b4-133">-Force</span></span>
<span data-ttu-id="7f8b4-134">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f8b4-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f8b4-135">-Name</span></span>
<span data-ttu-id="7f8b4-136">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-136">Specifies a name for the data source.</span></span> <span data-ttu-id="7f8b4-137">Nazwa nie jest uwidaczniana w portalu Azure, a dowolny ciąg może być wykorzystywany tak długo, jak jest unikatowy.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="7f8b4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f8b4-138">-ResourceGroupName</span></span>
<span data-ttu-id="7f8b4-139">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="7f8b4-140">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="7f8b4-140">-Workspace</span></span>
<span data-ttu-id="7f8b4-141">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7f8b4-142">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7f8b4-142">-WorkspaceName</span></span>
<span data-ttu-id="7f8b4-143">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7f8b4-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f8b4-144">-Confirm</span></span>
<span data-ttu-id="7f8b4-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8b4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8b4-146">-WhatIf</span></span>
<span data-ttu-id="7f8b4-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f8b4-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8b4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8b4-149">CommonParameters</span></span>
<span data-ttu-id="7f8b4-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8b4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8b4-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f8b4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8b4-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f8b4-152">INPUTS</span></span>

### <span data-ttu-id="7f8b4-153">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7f8b4-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7f8b4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7f8b4-154">System.String</span></span>

## <span data-ttu-id="7f8b4-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f8b4-155">OUTPUTS</span></span>

### <span data-ttu-id="7f8b4-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7f8b4-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7f8b4-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f8b4-157">NOTES</span></span>

## <span data-ttu-id="7f8b4-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f8b4-158">RELATED LINKS</span></span>

[<span data-ttu-id="7f8b4-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="7f8b4-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="7f8b4-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="7f8b4-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


