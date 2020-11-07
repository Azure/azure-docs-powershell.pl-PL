---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f441df5be99764f9582939d4c4d5d422ea88c97f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706761"
---
# <span data-ttu-id="de8d9-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8d9-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="de8d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="de8d9-103">Tworzy zaplanowaną konfigurację aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="de8d9-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="de8d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de8d9-104">SYNTAX</span></span>

### <span data-ttu-id="de8d9-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="de8d9-105">Windows (Default)</span></span>
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

### <span data-ttu-id="de8d9-106">Linux</span><span class="sxs-lookup"><span data-stu-id="de8d9-106">Linux</span></span>
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

## <span data-ttu-id="de8d9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de8d9-107">DESCRIPTION</span></span>
<span data-ttu-id="de8d9-108">Umożliwia utworzenie konfiguracji aktualizacji oprogramowania działającej według harmonogramu w celu zaktualizowania listy komputerów.</span><span class="sxs-lookup"><span data-stu-id="de8d9-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="de8d9-109">Komputery obejmują zarówno maszyny wirtualne platformy Azure, jak i niedrukowalne komputery.</span><span class="sxs-lookup"><span data-stu-id="de8d9-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="de8d9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de8d9-110">EXAMPLES</span></span>

### <span data-ttu-id="de8d9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de8d9-111">Example 1</span></span>
<span data-ttu-id="de8d9-112">Umożliwia utworzenie konfiguracji aktualizacji oprogramowania w celu zainstalowania aktualizacji krytycznych na dwóch maszynach wirtualnych z systemem Windows Azure po każdej soboty 9PM.</span><span class="sxs-lookup"><span data-stu-id="de8d9-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="de8d9-113">W tym przykładzie jako czas trwania aktualizacji jest ustawiona wartość 2 godzin.</span><span class="sxs-lookup"><span data-stu-id="de8d9-113">Update duration is set to 2 hours in this example.</span></span>

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
                                                 -AzVMResourceId $targetMachines `
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

## <span data-ttu-id="de8d9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de8d9-114">PARAMETERS</span></span>

### <span data-ttu-id="de8d9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de8d9-115">-AutomationAccountName</span></span>
<span data-ttu-id="de8d9-116">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="de8d9-116">The automation account name.</span></span>

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

### <span data-ttu-id="de8d9-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="de8d9-117">-AzureQuery</span></span>
<span data-ttu-id="de8d9-118">Dynamiczna kwerenda grupowa Azure.</span><span class="sxs-lookup"><span data-stu-id="de8d9-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="de8d9-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="de8d9-119">-AzureVMResourceId</span></span>
<span data-ttu-id="de8d9-120">Identyfikatory zasobów dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de8d9-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="de8d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8d9-121">-DefaultProfile</span></span>
<span data-ttu-id="de8d9-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de8d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8d9-123">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="de8d9-123">-Duration</span></span>
<span data-ttu-id="de8d9-124">Maksymalny czas trwania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="de8d9-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="de8d9-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="de8d9-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="de8d9-126">Liczba KB wykluczonych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="de8d9-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="de8d9-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="de8d9-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="de8d9-128">Wykluczone maski pakietów systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="de8d9-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="de8d9-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="de8d9-129">-IncludedKbNumber</span></span>
<span data-ttu-id="de8d9-130">Liczba uwzględnionych aktualizacji: KB.</span><span class="sxs-lookup"><span data-stu-id="de8d9-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="de8d9-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="de8d9-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="de8d9-132">Uwzględniono klasyfikacje pakietów Linux.</span><span class="sxs-lookup"><span data-stu-id="de8d9-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="de8d9-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="de8d9-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="de8d9-134">Dołączono maski pakietów systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="de8d9-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="de8d9-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="de8d9-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="de8d9-136">Uwzględnione klasyfikacje aktualizacji systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="de8d9-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="de8d9-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="de8d9-137">-Linux</span></span>
<span data-ttu-id="de8d9-138">Wskazuje, że konfiguracja aktualizacji oprogramowania przekierowania komputerów systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="de8d9-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="de8d9-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="de8d9-139">-NonAzureComputer</span></span>
<span data-ttu-id="de8d9-140">Nazwy komputerów, które nie są przez nią AZ.</span><span class="sxs-lookup"><span data-stu-id="de8d9-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="de8d9-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="de8d9-141">-NonAzureQuery</span></span>
<span data-ttu-id="de8d9-142">Grupa dynamiczna bez usługi Azure Query.</span><span class="sxs-lookup"><span data-stu-id="de8d9-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="de8d9-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="de8d9-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="de8d9-144">Publikowanie zadania.</span><span class="sxs-lookup"><span data-stu-id="de8d9-144">Post task.</span></span>

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

### <span data-ttu-id="de8d9-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="de8d9-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="de8d9-146">Parametr po zadaniu.</span><span class="sxs-lookup"><span data-stu-id="de8d9-146">Post task parameter.</span></span>

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

### <span data-ttu-id="de8d9-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="de8d9-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="de8d9-148">Przed zadaniem.</span><span class="sxs-lookup"><span data-stu-id="de8d9-148">Pre task.</span></span>

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

### <span data-ttu-id="de8d9-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="de8d9-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="de8d9-150">Parametr przed zadaniem.</span><span class="sxs-lookup"><span data-stu-id="de8d9-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="de8d9-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="de8d9-151">-RebootOnly</span></span>
<span data-ttu-id="de8d9-152">Wskazuje, że konfiguracja aktualizacji oprogramowania spowoduje tylko ponowne uruchomienie komputera.</span><span class="sxs-lookup"><span data-stu-id="de8d9-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="de8d9-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="de8d9-153">-RebootSetting</span></span>
<span data-ttu-id="de8d9-154">Ustawienie Uruchom ponownie.</span><span class="sxs-lookup"><span data-stu-id="de8d9-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="de8d9-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8d9-155">-ResourceGroupName</span></span>
<span data-ttu-id="de8d9-156">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de8d9-156">The resource group name.</span></span>

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

### <span data-ttu-id="de8d9-157">-Schedule</span><span class="sxs-lookup"><span data-stu-id="de8d9-157">-Schedule</span></span>
<span data-ttu-id="de8d9-158">Obiekt harmonogramu służący do konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="de8d9-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="de8d9-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="de8d9-159">-Windows</span></span>
<span data-ttu-id="de8d9-160">Wskazuje, że konfiguracja aktualizacji oprogramowania ukierunkowana na komputery z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="de8d9-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="de8d9-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de8d9-161">-Confirm</span></span>
<span data-ttu-id="de8d9-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de8d9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de8d9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8d9-163">-WhatIf</span></span>
<span data-ttu-id="de8d9-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de8d9-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8d9-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de8d9-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de8d9-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8d9-166">CommonParameters</span></span>
<span data-ttu-id="de8d9-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8d9-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8d9-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8d9-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8d9-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8d9-169">INPUTS</span></span>

### <span data-ttu-id="de8d9-170">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="de8d9-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="de8d9-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="de8d9-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="de8d9-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="de8d9-172">System.String[]</span></span>

### <span data-ttu-id="de8d9-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="de8d9-173">System.TimeSpan</span></span>

### <span data-ttu-id="de8d9-174">Microsoft. Azure. Commands. Automation. model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="de8d9-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="de8d9-175">Microsoft. Azure. Commands. Automation. model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="de8d9-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="de8d9-176">System. String</span><span class="sxs-lookup"><span data-stu-id="de8d9-176">System.String</span></span>

## <span data-ttu-id="de8d9-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de8d9-177">OUTPUTS</span></span>

### <span data-ttu-id="de8d9-178">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8d9-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="de8d9-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de8d9-179">NOTES</span></span>

## <span data-ttu-id="de8d9-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de8d9-180">RELATED LINKS</span></span>