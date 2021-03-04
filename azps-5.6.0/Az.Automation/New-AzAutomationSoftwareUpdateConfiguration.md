---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 4b62b04b0b394c590cd04ab30201575bb98d90b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952906"
---
# <span data-ttu-id="c90c2-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c90c2-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="c90c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c90c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c90c2-103">Tworzy zaplanowaną konfigurację aktualizacji oprogramowania azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c90c2-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="c90c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c90c2-104">SYNTAX</span></span>

### <span data-ttu-id="c90c2-105">Windows (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c90c2-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c90c2-106">Linux</span><span class="sxs-lookup"><span data-stu-id="c90c2-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c90c2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c90c2-107">DESCRIPTION</span></span>
<span data-ttu-id="c90c2-108">Tworzy konfigurację aktualizacji oprogramowania uruchamianą zgodnie z harmonogramem w celu zaktualizowania listy komputerów.</span><span class="sxs-lookup"><span data-stu-id="c90c2-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="c90c2-109">Komputery zawierają zarówno maszyny wirtualne azure, jak i komputery inne niż az.</span><span class="sxs-lookup"><span data-stu-id="c90c2-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="c90c2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c90c2-110">EXAMPLES</span></span>

### <span data-ttu-id="c90c2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c90c2-111">Example 1</span></span>
<span data-ttu-id="c90c2-112">Tworzy konfigurację aktualizacji oprogramowania w celu instalowania krytycznych aktualizacji na dwóch komputerach wirtualnych platformy Windows Azure raz w sobotę o 9:00.</span><span class="sxs-lookup"><span data-stu-id="c90c2-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="c90c2-113">W tym przykładzie czas trwania aktualizacji jest ustawiony na 2 godziny.</span><span class="sxs-lookup"><span data-stu-id="c90c2-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="c90c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c90c2-114">PARAMETERS</span></span>

### <span data-ttu-id="c90c2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c90c2-115">-AutomationAccountName</span></span>
<span data-ttu-id="c90c2-116">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c90c2-116">The automation account name.</span></span>

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

### <span data-ttu-id="c90c2-117">— AzureQuery</span><span class="sxs-lookup"><span data-stu-id="c90c2-117">-AzureQuery</span></span>
<span data-ttu-id="c90c2-118">Zapytanie azure grupy dynamicznej.</span><span class="sxs-lookup"><span data-stu-id="c90c2-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="c90c2-119">-AzureVMResourceId</span></span>
<span data-ttu-id="c90c2-120">Identyfikatory zasobów dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c90c2-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90c2-121">-DefaultProfile</span></span>
<span data-ttu-id="c90c2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c90c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-123">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="c90c2-123">-Duration</span></span>
<span data-ttu-id="c90c2-124">Maksymalny czas trwania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c90c2-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="c90c2-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="c90c2-126">Numery KB wykluczonych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c90c2-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="c90c2-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="c90c2-128">Excluded Linux package masks.</span><span class="sxs-lookup"><span data-stu-id="c90c2-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="c90c2-129">-IncludedKbNumber</span></span>
<span data-ttu-id="c90c2-130">Numery KB uwzględnionych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c90c2-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="c90c2-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="c90c2-132">Uwzględniono klasyfikacje pakietów dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c90c2-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="c90c2-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="c90c2-134">Dołączone maski pakietów dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c90c2-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="c90c2-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="c90c2-136">Uwzględniono klasyfikacje usługi Windows Update.</span><span class="sxs-lookup"><span data-stu-id="c90c2-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-137">— Linux</span><span class="sxs-lookup"><span data-stu-id="c90c2-137">-Linux</span></span>
<span data-ttu-id="c90c2-138">Wskazuje, że konfiguracja aktualizacji oprogramowania skierowana na komputery z systemem operacyjnym Linux.</span><span class="sxs-lookup"><span data-stu-id="c90c2-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="c90c2-139">-NonAzureComputer</span></span>
<span data-ttu-id="c90c2-140">Nazwy komputerów innych niż az.</span><span class="sxs-lookup"><span data-stu-id="c90c2-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="c90c2-141">-NonAzureQuery</span></span>
<span data-ttu-id="c90c2-142">Zapytanie grupy dynamicznej niezwiązywącej z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c90c2-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="c90c2-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="c90c2-144">Opublikuj zadanie.</span><span class="sxs-lookup"><span data-stu-id="c90c2-144">Post task.</span></span>

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

### <span data-ttu-id="c90c2-145">-PostTaskRunbookParameters</span><span class="sxs-lookup"><span data-stu-id="c90c2-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="c90c2-146">Parametr opublikuj zadanie.</span><span class="sxs-lookup"><span data-stu-id="c90c2-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="c90c2-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="c90c2-148">Wstępne zadanie.</span><span class="sxs-lookup"><span data-stu-id="c90c2-148">Pre task.</span></span>

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

### <span data-ttu-id="c90c2-149">-PreTaskRunbookParameters</span><span class="sxs-lookup"><span data-stu-id="c90c2-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="c90c2-150">Parametr zadania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="c90c2-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-151">- RebootOnly</span><span class="sxs-lookup"><span data-stu-id="c90c2-151">-RebootOnly</span></span>
<span data-ttu-id="c90c2-152">Wskazuje, że konfiguracja aktualizacji oprogramowania spowoduje tylko ponowne uruchomienie komputera.</span><span class="sxs-lookup"><span data-stu-id="c90c2-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-153">- RebootSetting</span><span class="sxs-lookup"><span data-stu-id="c90c2-153">-RebootSetting</span></span>
<span data-ttu-id="c90c2-154">Ustawienie ponownego rozruchu.</span><span class="sxs-lookup"><span data-stu-id="c90c2-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c90c2-155">-ResourceGroupName</span></span>
<span data-ttu-id="c90c2-156">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c90c2-156">The resource group name.</span></span>

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

### <span data-ttu-id="c90c2-157">— Planowanie</span><span class="sxs-lookup"><span data-stu-id="c90c2-157">-Schedule</span></span>
<span data-ttu-id="c90c2-158">Zaplanuj obiekt używany do konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="c90c2-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-159">— Windows</span><span class="sxs-lookup"><span data-stu-id="c90c2-159">-Windows</span></span>
<span data-ttu-id="c90c2-160">Wskazuje, że konfiguracja aktualizacji oprogramowania skierowana na komputery z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="c90c2-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c90c2-161">-Confirm</span></span>
<span data-ttu-id="c90c2-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c90c2-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c90c2-163">-WhatIf</span></span>
<span data-ttu-id="c90c2-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c90c2-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c90c2-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c90c2-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c2-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90c2-166">CommonParameters</span></span>
<span data-ttu-id="c90c2-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c90c2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90c2-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c90c2-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90c2-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c90c2-169">INPUTS</span></span>

### <span data-ttu-id="c90c2-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="c90c2-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="c90c2-171">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c90c2-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c90c2-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c90c2-172">System.String[]</span></span>

### <span data-ttu-id="c90c2-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c90c2-173">System.TimeSpan</span></span>

### <span data-ttu-id="c90c2-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="c90c2-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="c90c2-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="c90c2-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="c90c2-176">System.String</span><span class="sxs-lookup"><span data-stu-id="c90c2-176">System.String</span></span>

## <span data-ttu-id="c90c2-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c90c2-177">OUTPUTS</span></span>

### <span data-ttu-id="c90c2-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c90c2-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="c90c2-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c90c2-179">NOTES</span></span>

## <span data-ttu-id="c90c2-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c90c2-180">RELATED LINKS</span></span>
