---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547652"
---
# <span data-ttu-id="20686-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="20686-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="20686-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20686-102">SYNOPSIS</span></span>
<span data-ttu-id="20686-103">Tworzy zaplanowaną konfigurację aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="20686-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20686-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20686-104">SYNTAX</span></span>

### <span data-ttu-id="20686-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="20686-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20686-106">Linux</span><span class="sxs-lookup"><span data-stu-id="20686-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20686-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20686-107">DESCRIPTION</span></span>
<span data-ttu-id="20686-108">Umożliwia utworzenie konfiguracji aktualizacji oprogramowania działającej według harmonogramu w celu zaktualizowania listy komputerów.</span><span class="sxs-lookup"><span data-stu-id="20686-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="20686-109">Komputery obejmują zarówno maszyny wirtualne platformy Azure, jak i komputery spoza platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="20686-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="20686-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20686-110">EXAMPLES</span></span>

### <span data-ttu-id="20686-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20686-111">Example 1</span></span>
<span data-ttu-id="20686-112">Umożliwia utworzenie konfiguracji aktualizacji oprogramowania w celu zainstalowania aktualizacji krytycznych na dwóch maszynach wirtualnych z systemem Windows Azure po każdej soboty 9PM.</span><span class="sxs-lookup"><span data-stu-id="20686-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="20686-113">W tym przykładzie jako czas trwania aktualizacji jest ustawiona wartość 2 godzin.</span><span class="sxs-lookup"><span data-stu-id="20686-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="20686-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20686-114">PARAMETERS</span></span>

### <span data-ttu-id="20686-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20686-115">-AutomationAccountName</span></span>
<span data-ttu-id="20686-116">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="20686-116">The automation account name.</span></span>

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

### <span data-ttu-id="20686-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="20686-117">-AzureVMResourceId</span></span>
<span data-ttu-id="20686-118">Identyfikatory zasobów dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="20686-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="20686-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20686-119">-DefaultProfile</span></span>
<span data-ttu-id="20686-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20686-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20686-121">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="20686-121">-Duration</span></span>
<span data-ttu-id="20686-122">Maksymalny czas trwania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="20686-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="20686-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="20686-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="20686-124">Liczba KB wykluczonych aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="20686-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="20686-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="20686-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="20686-126">Wykluczone maski pakietów systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="20686-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="20686-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="20686-127">-IncludedKbNumber</span></span>
<span data-ttu-id="20686-128">Liczba uwzględnionych aktualizacji: KB.</span><span class="sxs-lookup"><span data-stu-id="20686-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="20686-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="20686-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="20686-130">Uwzględniono klasyfikacje pakietów Linux.</span><span class="sxs-lookup"><span data-stu-id="20686-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="20686-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="20686-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="20686-132">Dołączono maski pakietów systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="20686-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="20686-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="20686-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="20686-134">Uwzględnione klasyfikacje aktualizacji systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="20686-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="20686-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="20686-135">-Linux</span></span>
<span data-ttu-id="20686-136">Wskazuje, że konfiguracja aktualizacji oprogramowania przekierowania komputerów systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="20686-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="20686-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="20686-137">-NonAzureComputer</span></span>
<span data-ttu-id="20686-138">Nazwy komputerów, które nie są oparte na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="20686-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="20686-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20686-139">-ResourceGroupName</span></span>
<span data-ttu-id="20686-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="20686-140">The resource group name.</span></span>

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

### <span data-ttu-id="20686-141">-Schedule</span><span class="sxs-lookup"><span data-stu-id="20686-141">-Schedule</span></span>
<span data-ttu-id="20686-142">Obiekt harmonogramu służący do konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="20686-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="20686-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="20686-143">-Windows</span></span>
<span data-ttu-id="20686-144">Wskazuje, że konfiguracja aktualizacji oprogramowania ukierunkowana na komputery z systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="20686-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="20686-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20686-145">-Confirm</span></span>
<span data-ttu-id="20686-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20686-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20686-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20686-147">-WhatIf</span></span>
<span data-ttu-id="20686-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20686-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20686-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20686-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20686-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20686-150">CommonParameters</span></span>
<span data-ttu-id="20686-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20686-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20686-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20686-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20686-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20686-153">INPUTS</span></span>

### <span data-ttu-id="20686-154">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="20686-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="20686-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20686-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="20686-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="20686-156">System.String[]</span></span>

### <span data-ttu-id="20686-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="20686-157">System.TimeSpan</span></span>

### <span data-ttu-id="20686-158">Microsoft. Azure. Commands. Automation. model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="20686-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="20686-159">Microsoft. Azure. Commands. Automation. model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="20686-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="20686-160">System. String</span><span class="sxs-lookup"><span data-stu-id="20686-160">System.String</span></span>

## <span data-ttu-id="20686-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20686-161">OUTPUTS</span></span>

### <span data-ttu-id="20686-162">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="20686-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="20686-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20686-163">NOTES</span></span>

## <span data-ttu-id="20686-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20686-164">RELATED LINKS</span></span>
